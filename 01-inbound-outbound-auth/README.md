# Entra ID Inbound and Outbound Authentication

This sample demonstrates Agent and MCP Server on AgentCore Runtime with:
- **Inbound Auth**: User authenticates with Entra ID JWT
- **Outbound Auth**: Agent uses M2M token (via Credential Provider) to call MCP

## Architecture

```
User ──[ID Token]──► Agent Runtime ──[M2M Token]──► MCP Runtime
```

## Quick Start

```bash
pip install -r requirements.txt
jupyter notebook Step_by_Step_Entra_ID_Inbound_Outbound_Auth.ipynb
```
