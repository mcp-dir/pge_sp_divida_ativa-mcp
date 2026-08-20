---
name: pge_sp_divida_ativa-mcp
description: Skill da REST API do Procuradoria Geral do Estado SP: Dívida Ativa na MCP.AI: 1 endpoint em /api/pge_sp_divida_ativa. Procuradoria Geral do Estado SP: Dívida Ativa, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Procuradoria Geral do Estado SP: Dívida Ativa — REST API skill

Você tem acesso à **Procuradoria Geral do Estado SP: Dívida Ativa** REST API na MCP.AI.

> Procuradoria Geral do Estado SP: Dívida Ativa, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/pge_sp_divida_ativa
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
curl -X POST https://api.mcp.ai/api/pge_sp_divida_ativa/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/pge_sp_divida_ativa/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `pge_sp_divida_ativa_consultar`

Procuradoria Geral do Estado SP: Dívida Ativa, consulta em fonte oficial. _(POST /api/pge_sp_divida_ativa/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `cda` | string | Não | Parâmetro de consulta "cda". |
| `cnpj` | string | Não | Parâmetro de consulta "cnpj". |
| `cnpj_base` | string | Não | Parâmetro de consulta "cnpj_base". |
| `cpf` | string | Não | Parâmetro de consulta "cpf". |
| `ie` | string | Não | Parâmetro de consulta "ie". |
| `renavam` | string | Não | Parâmetro de consulta "renavam". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_pge_sp_divida_ativa` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
