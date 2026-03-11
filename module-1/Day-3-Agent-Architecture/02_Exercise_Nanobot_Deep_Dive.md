# Exercise: Nanobot Deep Dive & Architecture Map
**Time: 90 Minutes**

## Overview
Nanobot is a ~4,000 line Python agent. It is small enough to hold completely in your head. In this exercise, you must **read** the code before running it.

## Part 1: Read and Map
1.  Fork and clone the Nanobot repository from GitHub.
2.  Read the codebase.
3.  **Map the Architecture:** 
    *   Trace the exact flow: How does a message flow from the user $\rightarrow$ the agent $\rightarrow$ the LLM $\rightarrow$ back to the user?
    *   Identify the key abstractions. Where is tool use handled? Where is memory handled? Conversation management? The LLM provider integrations?
4.  Write a short architectural summary. Commit this write-up to your portfolio repository.

## Part 2: Run Nanobot Locally
1. Configure it with a local LLM (e.g., Ollama + Qwen3 8B) OR an API Key (Anthropic/OpenAI).
2. Connect it to a messaging platform (Discord or Telegram).
3. Send it messages. Observe its behavior and logs.
4. Locate its local database (look for local Markdown or JSON memory files). Read what the agent "remembers" about you.

## Part 3: Teach It
Find a partner. Explain the Nanobot architecture to them *without looking at the code*. If you can teach it, you understand it.
