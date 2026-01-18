---
name: copilot-assistant.assist
description: Create and refine GitHub Copilot prompts, agents, and instruction files
argument-hint: Describe what type of prompt, agent, or instruction you want to create
agent: abs.l3
---

# Copilot Helper

Create, refine, and improve GitHub Copilot custom prompts, agent definitions, and instruction files following established conventions and best practices.

## What

**Input:** Description of desired prompt/agent/instruction functionality, or existing file to improve

**Output:** Complete, well-structured markdown file with proper front-matter, sections, and conventions

## File Types

### Prompts (`.prompt.md`)
Custom commands that users invoke with `/command-name`
- **Naming:** Imperative verbs (e.g., `git.commit`, `abs.list-prompts`)
- **Structure:** Front-matter + sections describing behavior
- **Purpose:** Define specific tasks or workflows

### Agents (`.agent.md`)
Model configurations for different complexity levels
- **Naming:** Nouns describing role (e.g., `abs.l2`, `abs.l3`)
- **Structure:** Front-matter + capabilities + use cases
- **Purpose:** Define which model and when to use it

### Instructions (`.md`)
Global guidelines that apply to all interactions
- **Naming:** Present-continuous or descriptive (e.g., `copilot-instructions`)
- **Structure:** Front-matter + policy sections
- **Purpose:** Define rules, conventions, and policies

## Conventions

### Front-matter Requirements

**For Prompts:**
```yaml
---
name: domain.action              # Domain-prefixed name (git.*, abs.*)
description: Brief description   # What the prompt does
argument-hint: Usage hint       # Optional: what arguments it expects
agent: abs.l2                   # Optional: recommended agent to use
---
```

**For Agents:**
```yaml
---
name: abs.l{1-4}                # Agent tier (l1=cheapest, l4=most capable)
description: Brief description   # What the agent is for
model: Model Name               # The underlying model
argument-hint: Usage hint       # What tasks to give this agent
---
```

**For Instructions:**
```yaml
---
name: instruction-name          # Descriptive name
---
```

### File Naming

- **Domain prefixes:** `git.*` for git operations, `abs.*` for system/meta operations
- **kebab-case:** All lowercase with hyphens (e.g., `copilot-helper`, `list-prompts`)
- **Extensions:** `.prompt.md`, `.agent.md`, or `.md`

### Content Structure

1. **Title (H1):** Clear, descriptive heading
2. **Overview:** Brief explanation of purpose
3. **Sections (H2):** Organized by logical groupings
4. **Examples:** Include practical examples where helpful
5. **Rules/Guidelines:** Clear, actionable instructions
6. **Warnings:** Use emoji and bold for critical information (🚨, ⚠️, ✅, ❌)

### Writing Style

- **Imperative mood:** "Analyze changes", not "Analyzes changes"
- **Direct and concise:** No fluff or unnecessary words
- **Actionable:** Specific instructions, not vague suggestions
- **Structured:** Use lists, tables, and sections for clarity
- **Consistent:** Follow existing patterns from other prompts

## Workflow

### 1. Understand Requirements
- What is the purpose? (prompt, agent, or instruction?)
- Who is the user? (developer, AI, or both?)
- What domain? (git, abs, or other?)
- What complexity level? (simple task or complex workflow?)

### 2. Choose Appropriate Template

**Simple Prompt Template:**
```markdown
---
name: domain.action
description: Brief description
argument-hint: Usage hint
agent: abs.l2
---

# Title

Brief overview of what this prompt does.

## Input

What the prompt expects from the user.

## Output

What the prompt produces.

## How

Step-by-step instructions for the AI to follow.
```

**Agent Template:**
```markdown
---
name: abs.l{X}
description: Brief description
model: Model Name
argument-hint: Usage hint
---

# L{X} Agent

Overview of agent purpose and capabilities.

## Model Configuration

- **Primary Model:** Model name
- **Context:** Token limits
- **Capabilities:** Features available

## Use Cases

### ✅ Recommended For
- List of ideal use cases

### ⚠️ Not Recommended For
- List of unsuitable use cases

## Performance Notes

Key strengths and benchmarks.
```

### 3. Follow Conventions

- Respect `.editorconfig` settings (tabs, LF endings, UTF-8)
- Use domain prefixes (`git.*`, `abs.*`)
- Include proper front-matter
- Add emojis for warnings/success (🚨, ⚠️, ✅, ❌)
- Keep under 80 characters per line where reasonable

### 4. Validate Quality

**Before finalizing, check:**
- ✅ Front-matter is complete and valid
- ✅ Name follows domain.action pattern
- ✅ File naming matches conventions
- ✅ Structure is clear and logical
- ✅ Examples are practical and relevant
- ✅ Language is imperative and direct
- ✅ No trailing whitespace
- ✅ Ends with final newline

## Examples

### Example 1: Simple Prompt

**Request:** "Create a prompt for formatting code"

**Output:** `abs.format.prompt.md`
```yaml
---
name: abs.format
description: Format code according to project conventions
argument-hint: Optional file path or glob pattern
agent: abs.l2
---

# Format Code

Automatically format code files following project style guides and conventions.

## What

**Input:** File path(s) or current workspace

**Output:** Formatted code following .editorconfig and project conventions

## How

1. Identify files to format (from argument or workspace)
2. Read .editorconfig for formatting rules
3. Apply formatting (indentation, line endings, trailing whitespace)
4. Report summary of changes made
```

### Example 2: Agent Definition

**Request:** "Create an L5 agent for research tasks"

**Output:** `abs.l5.agent.md`
```yaml
---
name: abs.l5
description: Research and analysis agent for complex investigations
model: Claude Opus 4.5 with extended thinking
argument-hint: Describe the research task or question
---

# L5 Agent

Execute deep research and analysis tasks requiring sustained reasoning and synthesis.

## Model Configuration

- **Primary Model:** Claude Opus 4.5
- **Context:** 200K input
- **Capabilities:** Extended thinking, web search, tool use

## Use Cases

### ✅ Recommended For
- Multi-source research synthesis
- Deep technical analysis
- Complex decision-making requiring evidence
```

## Important Rules

- 🛑 **NEVER skip front-matter** — All files must have proper YAML front-matter
- ✅ **Always follow naming conventions** — Use domain prefixes and kebab-case
- 📝 **Be specific and actionable** — Provide clear, step-by-step instructions
- 🔍 **Include examples** — Show don't just tell
- ⚠️ **Reference copilot-instructions.md** — Respect tool policies and conventions
- 📖 **Read existing files** — Learn from patterns in git.commit, abs.list-prompts, etc.
