# Guide: The Conflict Gauntlet
**Time: 30 Minutes**

## Overview
Merge conflicts are a normal part of collaborating. You cannot avoid them, so you must learn to resolve them calmly.

## Instructions
1.  **Fork:** Your instructor will provide a link to a repository containing intentionally conflicting files. Fork it and clone it locally.
2.  **Branch:** Create a branch (`feature/your-name`).
3.  **Conflict Creation:** In the `main` branch, the instructor will push an update to an `index.html` file. You will concurrently make changes to the same lines in the `index.html` file on your branch.
4.  **Merge & Conflict:** Try to merge main into your branch, or create a PR to merge your branch into main. 
5.  **Resolution:** 
    *   Open the file in your IDE.
    *   Examine the `<<<<<<< HEAD` and `=======` markers.
    *   Choose the correct code (or combine them).
    *   Delete the Git conflict markers manually.
    *   Add, commit, and push the resolved file to complete the merge.
