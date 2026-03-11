# Lab: Prompt Engineering Across Tools
**Time: 75 Minutes**

## Overview
A prompt that works perfectly in a chat interface (like ChatGPT) might fail completely when handed to an autonomous agent (like Antigravity) or a spec-driven tool (like Kiro). You will test the portability of your prompt patterns.

## Instructions
Choose your 3 best prompt patterns from the morning workshop.

### Phase 1: The Portability Test
Run those exact same 3 prompts through the three core tools in your stack:
1.  **Claude Code CLI:** A conversational, terminal-native environment with global context.
2.  **Kiro:** A spec-driven environment that breaks prompts into Requirements -> Design -> Tasks.
3.  **Antigravity:** An agentic environment where the AI has autonomy to orchestrate its own tools to solve the request.

### Phase 2: Documentation
Answer these questions in your portfolio repository wiki based on your experiments:
*   Does the same prompt produce the same quality across all three tools? Why or why not?
*   Which tool benefits the *most* from a highly structured, 5-layer prompt?
*   Which tool compensates the best for a *vague* prompt by introducing its own structure (e.g., Kiro's spec workflow)?
*   How did the context window size difference affect the prompt strategy?

## Pair Exercise: Prompt Review (45 Minutes)
1. Exchange your prompt playbooks with a partner.
2. Use their prompts on a brand new, empty codebase.
3. Do their prompts work for you, or did they rely on unstated context that only they possessed?
4. **Insight:** Prompts that only work for the author are not team-scalable. The Renaissance Developer builds tools for the team.
