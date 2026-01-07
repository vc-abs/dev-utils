---
name: list-prompts
description: Scan and display available custom prompts from multiple locations (⚠️ workspace scope limited)
last-updated: 2025-12-25
---

# List Available Prompts (⚠️ Workspace Scope Limited)

**🚨 IMPORTANT LIMITATION:** When invoked from within a workspace, this prompt may only be able to scan files within the current workspace scope and cannot access global user prompts outside the workspace directory.

## Overview

Scan for available custom prompts from multiple locations and display them in an organized table format.

## Output Format

Display discovered prompts in the following table:

| Command             | Location          | Description         |
| ------------------- | ----------------- | ------------------- |
| (scan and populate) | (source location) | (from front-matter) |

## Scan Locations

**Priority order for scanning:**
1. `<project-root>/.github/prompts/` - Repository-specific custom prompts
2. `~/.config/Code/User/prompts/` - VS Code user prompts directory (includes this prompt's siblings)
3. User VS Code settings directory - Other user-defined global prompts  
4. VS Code extensions - Extension-provided prompts

## Implementation Notes

**Important:** This prompt should only scan and display information. Do not modify, create, or delete any files.

**🚨 WORKSPACE LIMITATION:** When invoked from within a workspace, this prompt may only be able to scan files within the current workspace scope and cannot access global user prompts outside the workspace directory.

For each prompt file found:
- Extract the `name` and `description` from YAML front-matter
- Format command as: `/<name>`
- Include the source location for reference
- Handle missing front-matter gracefully
