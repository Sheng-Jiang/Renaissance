# Exercise: OpenClaw Architecture Treasure Hunt
**Time: Full Day**

## Phase 1: Trace 5 Critical Code Paths (120 mins)
Working in pairs, trace these paths through the OpenClaw monorepo:

| # | Path | What You're Looking For |
|---|---|---|
| 1 | **User sends a message** | CLI → Gateway → Agent → LLM → Response |
| 2 | **Skill installation** | ClawHub download → Security scan → Installation → Registry |
| 3 | **Multi-agent communication** | Agent A → Message bus → Agent B → Response |
| 4 | **Authentication flow** | Credential → Session → Permission check |
| 5 | **Error handling** | Failure → Propagation → User-facing error |

For each path, document:
- Entry point (file + function)
- Key intermediate steps
- Exit point
- Architectural pattern used
- One thing that surprised you

## Phase 2: Architecture Analysis Document (120 mins)
Write a comprehensive analysis including:

1. **System Overview:** High-level component diagram
2. **Communication Patterns:** HTTP, WebSocket, gRPC, or message bus?
3. **Data Flow:** User input → agent response (full trace)
4. **Plugin Architecture:** How skills are loaded, isolated, and executed
5. **Scalability Analysis:** Bottlenecks and what breaks at 10x scale
6. **Code Quality Observations:** Well-implemented patterns and refactoring candidates

## Phase 3: Show & Tell (60 mins)
Each pair presents one finding (5 min):
- What was the most surprising architectural decision?
- What would you change?
