# Instalação detalhada

CVM: Processos Sancionadores Julgados é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_cvm_sancionadores`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_cvm_sancionadores` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_cvm_sancionadores` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_cvm_sancionadores` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.cvm_sancionadores` (ou `servers.cvm_sancionadores` no VS Code) do config do cliente e reinicie.
