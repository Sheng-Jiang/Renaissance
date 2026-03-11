# Build Sprint: Memory System Integration
**Time: 60 Minutes**

## Overview
Design a persistent memory architecture for your Nanobot that goes beyond a flat conversation log.

## Instructions
Implement a file-based storage system that allows your agent to recall structured knowledge. Using Nanobot's local file system capabilities, create logic to read and write to standard memory structures.

### Required Memory Structures:
1.  **`memory/profile.md`**: Store user facts, preferences, and expertise levels.
2.  **`memory/projects/`**: A directory for tracking per-project state files (current tasks, blockers, decisions).
3.  **`memory/corrections.md`**: Track things the agent got wrong in the past and the fix the user provided (Learning Memory).

## Workflow Integration
*   Update your agent's system prompt so that it knows *how* and *when* to read from these memory files during a conversation.
*   **Testing:** Have a multi-turn conversation where you tell the agent a preference. Restart the agent process. Verify that it remembers the context in the new session.

## Discussion Point (Privacy by Design)
*What should the agent remember, and what should it intentionally forget? How do you prevent sensitive secrets or PII from being permanently logged into its memory arrays?*
