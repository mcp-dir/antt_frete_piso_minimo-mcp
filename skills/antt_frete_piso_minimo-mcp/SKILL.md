---
name: antt_frete_piso_minimo-mcp
description: Skill da REST API do ANTT: Calcular Piso Mínimo de Frete na MCP.AI: 1 endpoint em /api/antt_frete_piso_minimo. ANTT: Calcular Piso Mínimo de Frete, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# ANTT: Calcular Piso Mínimo de Frete — REST API skill

Você tem acesso à **ANTT: Calcular Piso Mínimo de Frete** REST API na MCP.AI.

> ANTT: Calcular Piso Mínimo de Frete, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/antt_frete_piso_minimo
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/antt_frete_piso_minimo/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"tipo_carga":"...","eixos":"...","distancia":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/antt_frete_piso_minimo/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `antt_frete_piso_minimo_consultar`

ANTT: Calcular Piso Mínimo de Frete, consulta em fonte oficial. _(POST /api/antt_frete_piso_minimo/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `tipo_carga` | string | Sim | Parâmetro de consulta "tipo_carga". |
| `eixos` | string | Sim | Parâmetro de consulta "eixos". |
| `distancia` | string | Sim | Parâmetro de consulta "distancia". |
| `composicao_veicular` | string | Não | Parâmetro de consulta "composicao_veicular". |
| `alto_desempenho` | string | Não | Parâmetro de consulta "alto_desempenho". |
| `retorno_vazio` | string | Não | Parâmetro de consulta "retorno_vazio". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_antt_frete_piso_minimo` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
