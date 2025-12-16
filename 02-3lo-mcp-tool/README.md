# Entra ID 3LO for MCP Tool (URL Elicitation)

This sample demonstrates an MCP tool that requires user consent using MCP's URL elicitation feature.

## Architecture

```
User ──[ID Token]──► Agent ──[M2M]──► MCP ──[URL Elicitation]──► User consents ──► Microsoft Graph
```

## Quick Start

```bash
pip install -r requirements.txt
jupyter notebook Step_by_Step_Entra_ID_3LO_MCP_Tool.ipynb
```
