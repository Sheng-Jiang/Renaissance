# Exercise: Claude Code CLI Deep Dive
**Time: 75 Minutes**

## Overview
Claude Code CLI is your terminal-native, Unix-composable assistant. It’s excellent for daily coding tasks and CI/CD integration. In this exercise, you will practice using it, focusing heavily on manually verifying its output.

## Pre-requisites
1. Verify installation: `claude --version`
2. Check configuration: `claude config show`
3. Ensure you are in your portfolio repository.

## Part 1: Your First Session
**Task:** Open your terminal and run Claude Code. Prompt it with:
> "Add a utility function that validates email addresses with comprehensive tests."

**Verification Step (Crucial):**
Do not blindly accept the code. Review every single line for:
*   Correctness
*   Edge cases (e.g., extremely long emails, weird but valid characters)
*   Test quality (did it test the edge cases?)
*   Security implications (ReDoS vulnerabilities in regex?)

*Practice:* Accept, reject, or modify each proposed change.

## Part 2: Unix Composability
Try piping data into Claude Code. For example:
`echo "fix linting errors" | claude`
or chain it with shell commands based on your workflow.

*(Note: Be aware of token costs when piping large context files.)*

## Part 3: Generating Infrastructure Code
**Task:** Use Claude Code to generate a GitHub Actions workflow that runs your newly created email validation tests on Push and Pull Request events.

**Verification Step (Crucial):**
Manually review the generated YAML. Did it choose the right runner (`ubuntu-latest`)? Are the steps logical? Improve it manually if necessary before committing.

## Reflection Question
*What did the AI get right? What was subtly wrong? What would you never have caught without looking closely?*
