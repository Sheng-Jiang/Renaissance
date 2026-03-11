# Workshop: Build Your Prompt Playbook
**Time: 90 Minutes**

## Overview
Move from ad-hoc prompting to systematic, repeatable prompt patterns. You will build a personal repository of battle-tested prompts for common engineering tasks.

## Instructions
Create a `prompts/` directory in your personal portfolio repository. Inside it, create Markdown files for these 5 core patterns. Test them using Claude Code CLI or Kiro.

### Pattern 1: Scaffolding
Generate a new module/service/component with full structure.
*   **Practice:** Scaffold a REST API service with routes, controllers, models, and tests.
*   **Must Include:** Project context, module purpose, standard file naming convention, standard error handling approach, and preferred test framework.

### Pattern 2: Test Generation
Produce comprehensive tests for existing code.
*   **Practice:** Give the AI the custom skill logic you built for your Nanobot in Module 1 and ask for tests.
*   **Verification Check:** Did the AI test behavior, or did it just write a tautology (mocking everything so the test passes no matter what)? Are error edge cases caught?

### Pattern 3: Refactoring
Transform working code into better code without changing its behavior.
*   **Practice:** Take a messy, long function from a past project. Ask the AI to refactor it.
*   **Must Include:** Specific refactoring goals (e.g., "improve readability by extracting nested conditionals", "reduce time complexity", or "make it highly testable via dependency injection").

### Pattern 4: Debugging
Use AI to diagnose and fix issues.
*   **Practice:** Intentionally break a piece of code so a test fails. Give the code and the test output to the AI.
*   **Anti-Pattern Alert:** Watch out for the AI "fixing" the bug by simply changing the assertions in the test so it passes!

### Pattern 5: Documentation
Generate docs, READMEs, and inline comments from code.
*   **Practice:** Ask the AI to generate full API documentation or a technical README for your Day 4 application from Module 1.
*   **Must Include:** Target audience constraint (e.g., "Write this for a junior frontend developer consuming this API").
