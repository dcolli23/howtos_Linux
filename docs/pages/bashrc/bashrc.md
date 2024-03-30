---
title: bashrc
nav_order: 2
---

# bashrc Customizations

These are some of the changes I like to make to my ~/.bashrc.

## Aliases

- `alias hist='history | ag'`
  - This allows for a search of all commands in history that use a keywoard:
  - Usage:
    - If I wanted to search for all commands I've executed in history that contain the word "bash", I would execute:
      ```
      hist bash
      ```
- `alias conda-activate-dir='conda activate ${PWD##*/}'`
  - Activate the Anaconda environment with the same name as the current directory.
  - Yes, this is pretty lazy!