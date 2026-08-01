# Tool-Calling Agents

A hands-on project for building AI agents that use external tools through Amazon Bedrock's OpenAI-compatible API. The examples progress from basic function calls to LangChain/LangGraph agents with weather lookup, web search, and Model Context Protocol (MCP) integrations.

## What you'll learn

- Define Python functions as tools for language models.
- Describe tools with structured schemas.
- Build agent loops with LangChain and LangGraph.
- Connect to Gemma and Mistral models through Amazon Bedrock.
- Add live weather and DuckDuckGo web-search capabilities.
- Explore MCP and a minimal Chainlit interface.

## Project files

- `tool-calling-agents.ipynb` — core tool-calling exercises and examples.
- `ask_the_web_agent.ipynb` — expanded, guided web-agent tutorial.
- `requirements.txt` — Python dependencies.
- `environment.yaml` — reproducible Conda environment.
- `assets/` — diagrams used by the notebooks.

## Setup

Python 3.11 is recommended.

### Conda

```bash
conda env create -f environment.yaml
conda activate web_agent
jupyter notebook
```

### Virtual environment

```bash
python -m venv .venv
```

Activate the environment, then install the dependencies:

```bash
pip install -r requirements.txt
jupyter notebook
```

## Bedrock configuration

The notebooks use the following OpenAI-compatible endpoint:

```text
https://bedrock-mantle.us-east-1.api.aws/v1
```

You need an Amazon Bedrock API key and access to the models used in the examples. Keep the key in an environment variable or enter it securely at runtime. Never commit a real credential to the notebook or repository.

The included `*****` API-key value is only a placeholder.

## Run the examples

Open `tool-calling-agents.ipynb`, select the environment's Python kernel, and run the cells in order. Some examples require internet access for weather data, DuckDuckGo search, or MCP tools.

## Security

Before committing notebook changes, clear outputs that may contain local paths or sensitive responses. Keep `.env` files, credentials, logs, and notebook checkpoints out of Git.
