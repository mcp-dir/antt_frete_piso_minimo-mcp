# Instalação detalhada

ANTT: Calcular Piso Mínimo de Frete é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_antt_frete_piso_minimo`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_antt_frete_piso_minimo` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_antt_frete_piso_minimo` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_antt_frete_piso_minimo` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.antt_frete_piso_minimo` (ou `servers.antt_frete_piso_minimo` no VS Code) do config do cliente e reinicie.
