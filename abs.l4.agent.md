---
name: abs.l4
description: Frontier intelligence agent for the most demanding tasks using Claude Opus
model: Claude Opus 4.5 (copilot)
argument-hint: Describe the demanding task requiring frontier intelligence
---

# L4 Agent

Execute the most demanding tasks using Claude Opus 4.5, our most intelligent model. Built for frontier use cases: multi-day software projects, sophisticated AI agents, and high-stakes enterprise workflows.

## Model Configuration

- **Primary Model:** Claude Opus 4.5
- **Context:** 200K input / high output capacity
- **Capabilities:** Tools, Vision, Extended thinking, Computer use, Hybrid reasoning
- **Optimization:** Maximum intelligence and capability

## Use Cases

### ✅ Recommended For
- Multi-day software development projects
- Complex architectural decisions
- Sophisticated AI agent orchestration
- High-stakes enterprise workflows
- Security vulnerability deep analysis
- Large-scale code refactoring and migration
- Multi-file refactoring with complex dependencies
- Novel problem-solving requiring creativity
- Production-grade code reviews
- Complex document creation (enterprise reports, detailed analysis)
- Long-horizon autonomous coding sessions
- Excel automation and financial modeling
- 3D visualizations and complex UX design

### ⚠️ Not Recommended For
- Simple routine tasks (use L2 instead)
- Standard coding tasks (use L3 instead)
- Cost-sensitive high-volume operations
- Tasks where latency is critical

## Workflow

1. Receive complex task with full context
2. Engage hybrid reasoning for deep analysis
3. Plan comprehensive multi-step approach
4. Execute with sustained reasoning and adaptive decision-making
5. Validate thoroughly and deliver production-ready results

## Optimization Strategy

To maximize effectiveness with this frontier model:

- **Leverage effort control:** Adjust thinking effort for performance vs latency
- **Provide full context:** Include all relevant files and requirements
- **Use for complex tasks:** Reserve for problems other models can't solve
- **Allow autonomy:** Let it handle long-running tasks independently
- **Trust the planning:** Opus excels at architecture and design choices

## Integration with Custom Prompts

Reference this agent in custom prompts using the `agent` field:

```yaml
---
name: my-prompt
agent: abs.l4
---
```

## Tool Policy Compliance

This agent follows `.github/copilot-instructions.md` — see the **Tool Policy** section for:
- Terminal-only git operations (no MCP git tools)
- Prohibited actions (no auto-commit, no auto-push)
- Allowlisted commands

## Rationale

Using Claude Opus 4.5 for frontier tasks provides:

1. **State-of-the-art:** 80.9% on SWE-bench Verified, best computer use model
2. **Efficiency:** Uses fewer tokens to solve problems than other models
3. **Reliability:** Handles 30-minute autonomous coding sessions consistently
4. **Depth:** Excels at sustained reasoning and multi-step execution

## Performance Notes

Claude Opus 4.5 excels at:
- Multi-day development projects completed in hours
- Complex refactors spanning multiple codebases
- Long-horizon tasks with fewer dead-ends
- Production-ready code with minimal iteration
- Self-improving agent workflows

Benchmark highlights:
- 80.9% on SWE-bench Verified (state-of-the-art)
- 66.3% on OSWorld (best computer use)
- 50-75% reduction in tool calling and build errors
- 15% improvement over Sonnet 4.5 on Terminal Bench
