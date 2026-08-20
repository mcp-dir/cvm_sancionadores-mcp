---
name: cvm_sancionadores-mcp
description: Skill da REST API do CVM: Processos Sancionadores Julgados na MCP.AI: 1 endpoint em /api/cvm_sancionadores. CVM: Processos Sancionadores Julgados, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# CVM: Processos Sancionadores Julgados — REST API skill

Você tem acesso à **CVM: Processos Sancionadores Julgados** REST API na MCP.AI.

> CVM: Processos Sancionadores Julgados, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/cvm_sancionadores
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
curl -X POST https://api.mcp.ai/api/cvm_sancionadores/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/cvm_sancionadores/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `cvm_sancionadores_consultar`

CVM: Processos Sancionadores Julgados, consulta em fonte oficial. _(POST /api/cvm_sancionadores/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `termo` | string | Não | Parâmetro de consulta "termo". |
| `tipo_filtro` | string | Não | Parâmetro de consulta "tipo_filtro". |
| `data_inicio` | string | Não | Parâmetro de consulta "data_inicio". |
| `data_fim` | string | Não | Parâmetro de consulta "data_fim". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_cvm_sancionadores` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
