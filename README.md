# Claude API — Learning Notebooks

Hands-on notebooks exploring the Anthropic Claude API — from basic prompting to tool use and automated prompt evaluation.

## Notebooks

### Prompting & Evaluation

| Notebook | What it covers |
|---|---|
| `001_prompting.ipynb` | Multi-turn conversations, system prompts, stop sequences, temperature |
| `001_prompt_evals.ipynb` | Prompt evaluation pipeline — dataset generation + LLM-as-judge scoring |
| `001_prompt_evals_fns.ipynb` | Functional evaluation helpers — dataset gen, grading, scoring |
| `001_prompt_evals_grader.ipynb` | Full grader implementation with syntax validation (Python, JSON, Regex) |

### Tool Use / Agentic Patterns

| Notebook | What it covers |
|---|---|
| `001_tools.ipynb` | Introduction to tool use — schemas, tool execution loop |
| `001_tools_007.ipynb` | Multi-tool setup — datetime tools, reminder tool, batch tool |
| `001_tools_008.ipynb` | Complete agentic conversation loop with error handling |

## Key Concepts Covered

- **Multi-turn conversation management** — maintaining message history correctly
- **Tool use (function calling)** — defining schemas, running tools, feeding results back
- **Agentic loop** — handling `stop_reason: tool_use`, running tools, continuing conversation
- **LLM-as-judge evaluation** — using Claude to grade Claude's outputs
- **Prompt evaluation pipeline** — generate dataset → run prompt → grade → score
- **Concurrent evaluation** — running multiple test cases in parallel with `asyncio`

## Setup

```bash
pip install anthropic python-dotenv

# Add your Anthropic API key
echo "ANTHROPIC_API_KEY=your_key_here" > .env
```

## Stack
- **Python 3.11+**
- **Anthropic Claude API** (claude-haiku-4-5)
- **Jupyter Notebook**
