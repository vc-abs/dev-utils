---
name: abs.l3
description: Powerful versatile agent for complex tasks using Claude Sonnet
model: Claude Sonnet 4.5 (copilot)
argument-hint: Describe the complex task to execute
---

# L3 Agent

Execute complex, multi-step tasks using Claude Sonnet 4.5, optimized for agents, coding, and computer use. Ideal for production coding workflows, long-running agents, and sophisticated analysis.

## Model Configuration

- **Primary Model:** Claude Sonnet 4.5
- **Context:** 200K input / 64K output
- **Capabilities:** Tools, Vision, Extended thinking, Computer use
- **Optimization:** Balance of intelligence and efficiency

## Use Cases

### ✅ Recommended For
- Long-running agentic workflows
- Production code generation and refactoring
- Browser and computer use automation
- Cybersecurity analysis and red teaming
- Financial analysis and risk assessment
- Multi-step research and synthesis
- Content generation and analysis
- Business document creation (slides, docs, spreadsheets)
- Code review and debugging
- Architecture planning

### ⚠️ Not Recommended For
- Simple routine tasks (use L2 instead)
- Commit message generation (use L2 instead)
- Tasks requiring absolute frontier intelligence (use L4 instead)
- Multi-day development projects (use L4 instead)

## Workflow

1. Receive task request with detailed requirements
2. Plan approach using extended thinking when beneficial
3. Execute multi-step operations with tool use
4. Validate results and iterate as needed
5. Return comprehensive results

## Optimization Strategy

To maximize effectiveness with this versatile model:

- **Provide context:** Include relevant background and constraints
- **Use extended thinking:** Enable for complex reasoning tasks
- **Leverage tools:** Take advantage of computer use and browser automation
- **Iterate:** Allow multiple passes for refinement
- **Be specific:** Clear requirements improve output quality

## Integration with Custom Prompts

Reference this agent in custom prompts using the `agent` field:

```yaml
---
name: my-prompt
agent: abs.l3
---
```

## Tool Policy Compliance

This agent follows `.github/copilot-instructions.md` — see the **Tool Policy** section for:
- Terminal-only git operations (no MCP git tools)
- Prohibited actions (no auto-commit, no auto-push)
- Allowlisted commands

## Rationale

Using Claude Sonnet 4.5 for complex tasks provides:

1. **Balance:** Superior intelligence with practical efficiency
2. **Versatility:** Excels across coding, analysis, and content generation
3. **Reliability:** Consistent performance on demanding workflows
4. **Cost-effective:** More affordable than Opus for most complex tasks

## Performance Notes

Claude Sonnet 4.5 excels at:
- Agentic coding with 30+ hours of autonomous operation
- Multi-step reasoning and planning
- Error correction and instruction following
- Tool selection and orchestration
- Long-context understanding

Best suited for:
- Production-ready code development
- Complex analysis requiring deep reasoning
- Tasks benefiting from extended thinking
- High-volume, sophisticated workflows
