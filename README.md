# LangGraph Cloud Example

![](static/agent_ui.png)

This is an example agent to deploy with LangGraph Cloud.

> [!TIP]
> If you would rather use `requirements.txt` for managing dependencies in your LangGraph Cloud project, please check out [this repository](https://github.com/langchain-ai/langgraph-example).


[LangGraph](https://github.com/langchain-ai/langgraph) is a library for building stateful, multi-actor applications with LLMs. The main use cases for LangGraph are conversational agents, and long-running, multi-step LLM applications or any LLM application that would benefit from built-in support for persistent checkpoints, cycles and human-in-the-loop interactions (ie. LLM and human collaboration).

LangGraph shortens the time-to-market for developers using LangGraph, with a one-liner command to start a production-ready HTTP microservice for your LangGraph applications, with built-in persistence. This lets you focus on the logic of your LangGraph graph, and leave the scaling and API design to us. The API is inspired by the OpenAI assistants API, and is designed to fit in alongside your existing services.

## Configuration

This agent supports multiple AI providers. The model selection follows this priority order:

1. **Configurable parameter** (passed via API or dashboard)
2. **Environment variable** (`LANGGRAPH_MODEL_NAME`)
3. **Default fallback** (`openai`)

### Local Development

Create a `.env` file in the project root:
```bash
# LangGraph Configuration
LANGGRAPH_MODEL_NAME=openai

# Add your API keys
OPENAI_API_KEY=your_openai_key_here
ANTHROPIC_API_KEY=your_anthropic_key_here
```

### Platform Deployment

Set the `LANGGRAPH_MODEL_NAME` environment variable in your LangGraph Cloud dashboard:
- `openai` - Uses GPT-4o
- `anthropic` - Uses Claude-3-Sonnet

## Deployment

In order to deploy this agent to LangGraph Cloud you will want to first fork this repo. After that, you can follow the instructions [here](https://langchain-ai.github.io/langgraph/cloud/) to deploy to LangGraph Cloud.
