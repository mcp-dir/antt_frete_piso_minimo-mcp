# Instalação rápida

ANTT: Calcular Piso Mínimo de Frete é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_antt_frete_piso_minimo`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

A auth acontece em runtime: clientes com **OAuth 2.1** (Claude Desktop, Cursor, VS Code recentes) abrem o browser na 1ª chamada (magic-link). Clientes sem OAuth recebem a tool `authenticate` — abra `https://app.mcp.ai/agent-auth`, faça login, copie o JWT e cole no chat.

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → `ANTT: Calcular Piso Mínimo de Frete` / `https://api.mcp.ai/p_antt_frete_piso_minimo`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "antt_frete_piso_minimo": { "type": "http", "url": "https://api.mcp.ai/p_antt_frete_piso_minimo" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=antt_frete_piso_minimo&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9hbnR0X2ZyZXRlX3Bpc29fbWluaW1vIn0=)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "antt_frete_piso_minimo": { "url": "https://api.mcp.ai/p_antt_frete_piso_minimo" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=antt_frete_piso_minimo&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_antt_frete_piso_minimo%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "antt_frete_piso_minimo": { "type": "http", "url": "https://api.mcp.ai/p_antt_frete_piso_minimo" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_antt_frete_piso_minimo
```

Dúvidas? [antt_frete_piso_minimo@mcp.ai](mailto:antt_frete_piso_minimo@mcp.ai)
