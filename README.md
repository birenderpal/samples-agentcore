# Amazon Bedrock AgentCore Samples with Microsoft Entra ID

This folder contains sample notebooks demonstrating various authentication patterns for Amazon Bedrock AgentCore with Microsoft Entra ID (Azure AD).

## Samples Overview

| Sample | Description | Auth Pattern |
|--------|-------------|--------------|
| [01-inbound-outbound-auth](./01-inbound-outbound-auth) | Agent and MCP on Runtime with Entra ID | Inbound: User JWT, Outbound: M2M |
| [02-3lo-mcp-tool](./02-3lo-mcp-tool) | MCP tool requiring user consent | 3-Legged OAuth (URL Elicitation) |
| [03-3lo-gateway](./03-3lo-gateway) | Agent connecting to Gateway with 3LO | Gateway-managed 3LO |

## Architecture Patterns

### Pattern 1: Inbound + Outbound M2M Authentication

```
User ──[ID Token]──► Agent Runtime ──[M2M Token]──► MCP Runtime
```

### Pattern 2: 3-Legged OAuth for MCP Tools

```
User ──[ID Token]──► Agent ──[M2M]──► MCP ──[URL Elicitation]──► User consents ──► Protected API
```

### Pattern 3: Gateway with 3LO

```
User ──[ID Token]──► Agent ──► Gateway ──[3LO]──► External API
```

## Prerequisites

- AWS Account with Bedrock AgentCore access
- Microsoft Entra ID tenant with admin access
- Python 3.11+
- Docker (for local builds)

## Related Resources

- [Amazon Bedrock AgentCore Documentation](https://docs.aws.amazon.com/bedrock-agentcore/)
- [Strands Agents SDK](https://strandsagents.com/)
- [Microsoft Entra ID Documentation](https://learn.microsoft.com/en-us/entra/identity/)
