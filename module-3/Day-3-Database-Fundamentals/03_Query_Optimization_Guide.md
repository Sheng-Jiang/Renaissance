# Guide: Query Optimization with AI

**Objective:** Learn how to interpret slow queries and use AI safely to suggest missing indexes and query refactors.

## The N+1 Problem Scenario

Imagine this ORM code:
```typescript
const posts = await db.post.findMany();
for (const post of posts) {
  const author = await db.user.findUnique({ where: { id: post.authorId } });
  console.log(post.title, author.name);
}
```
If there are 100 posts, this executes **101 queries**. 1 to fetch posts, 100 to fetch authors.

### Optimization Fix
Use `JOIN` or ORM `include`.
```typescript
const posts = await db.post.findMany({ include: { author: true } });
```

## AI as your DBA (Database Administrator)

When queries get slow, PostgreSQL's `EXPLAIN ANALYZE` is your best friend. But reading its output can be intimidating.

### The Workflow:
1. Identify the slow query.
2. Run `EXPLAIN ANALYZE select ...` in your SQL console.
3. Copy the raw output.
4. Feed it to an LLM.

### Example Prompt:
> "I ran EXPLAIN ANALYZE on a slow Postgres query. The output is below. Why is it slow, and what index should I add? Can you also rewrite the query if the SQL itself is inefficient?"
> 
> `[PASTE EXPLAIN OUTPUT]`

### Evaluating the AI Response:
- **Did it suggest a B-Tree index?** Standard for exact matches.
- **Did it suggest covering indexes?** `CREATE INDEX ... INCLUDE (...)`. Useful if you always fetch the same 2 fields.
- **Did it identify a Sequential Scan (`Seq Scan`)?** The AI should point this out. A sequential scan on a million-row table is a disaster.

## Warning: Human Judgment Required
AI might suggest an index for *every* slow query. **Do not blindly create indexes.**
Every index slows down `INSERT`, `UPDATE`, and `DELETE` operations. As a Renaissance Developer, you must weigh the read-speed benefits against write-speed penalties.
