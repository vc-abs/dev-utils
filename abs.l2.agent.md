---
name: abs.l2
description: Fast and efficient agent for routine tasks using Claude Haiku
model: Claude Haiku 4.5 (copilot)
argument-hint: Describe the routine task to execute
---

# L2 Agent

Execute routine, well-defined tasks using Claude Haiku 4.5, optimized for speed and efficiency. Ideal for standard operations like commit messages, code formatting, simple refactoring, and documentation generation.

## Model Configuration

- **Primary Model:** Claude Haiku 4.5
- **Context:** High input / output capacity
- **Capabilities:** Tools, Vision, Fast responses
- **Optimization:** Speed and cost-effectiveness

## Use Cases

### ✅ Recommended For
- Git commit message generation
- Code formatting and linting fixes
- Simple refactoring (rename, extract variable)
- Documentation updates
- File organization and cleanup
- Standard code review comments
- Test name generation
- Import sorting and cleanup

### ⚠️ Not Recommended For
- Complex architectural decisions
- Security vulnerability analysis requiring deep reasoning
- Large-scale code restructuring
- Performance optimization requiring deep analysis
- Multi-file refactoring with complex dependencies
- Novel problem-solving requiring extensive creativity

## Workflow

1. Receive task request with clear, specific instructions
2. Read necessary context files (avoid unnecessary exploration)
3. Execute task following established patterns
4. Validate output meets basic requirements
5. Return concise results

## Optimization Strategy

To maximize effectiveness with this efficient model:

- **Be specific:** Provide clear, unambiguous instructions
- **Use examples:** Include code samples or format templates
- **Limit scope:** Break complex tasks into smaller subtasks
- **Verify inputs:** Ensure all required context is available
- **Follow patterns:** Stick to established project conventions

## Integration with Custom Prompts

Reference this agent in custom prompts using the `agent` field:

```yaml
---
name: my-prompt
agent: abs.l2
---
```

## Tool Policy Compliance

This agent follows `.github/copilot-instructions.md` — see the **Tool Policy** section for:
- Terminal-only git operations (no MCP git tools)
- Prohibited actions (no auto-commit, no auto-push)
- Allowlisted commands

## Rationale

Using Claude Haiku 4.5 for routine tasks provides:

1. **Speed:** Fast responses for quick turnaround
2. **Cost Efficiency:** Optimized for routine operations
3. **Reliability:** Consistent performance on well-defined tasks
4. **Focus:** Reserves more powerful models for complex problems

## Performance Notes

Claude Haiku 4.5 excels at:
- Structured tasks with clear patterns
- Operations with provided examples
- Tasks following established conventions
- Quick analysis and generation tasks

Best suited for:
- Well-defined operations with clear requirements
- Standard programming patterns
- Quick iterations and refinements
- Routine maintenance tasks
