# Sistema BPE — Framework de Ingeniería de Procesos

> **Business Process Engineering (BPE) Framework v3.2** — Célula de 6 subagentes + 7 skills para relevamiento → SOP As-Is → GAP → Business Case → SOP To-Be

## Estructura (Opción A - Optimizada Tokens)

```
Sistema BPE/
 ├── .opencode/                  # Framework (versionado en GitHub)
 │    ├── AGENTS.md              # Orquestador Leader BPE
 │    ├── MEMORY.md              # Diccionario SAP/Nessie, reglas v3.2
 │    ├── opencode.json          # MCP GitHub
 │    ├── agents/ (7)            # discovery, sop, gap, redesign, auditor, continuous-learning, github-sync
 │    └── skills/ (7)            # template-sop, auditor-checklist, matrix-gap-rules, tobe-business-case, sop-tobe-v3, etc.
 ├── SOP-XXX/                    # Proyectos aislados (NO versionar datos nómina)
 │    ├── 00_draft/
 │    ├── 01_process_survey_as-is/
 │    ├── 02_process_diagnosis/
 │    └── 03_process_future_state_to-be/
 └── para revision/              # Staging (NO versionar)
```

## Instalación

```bash
git clone https://github.com/<owner>/bpe-framework.git "Sistema BPE"
cd "Sistema BPE"
npm install # instala @opencode-ai/plugin
export GITHUB_TOKEN=ghp_xxx # para github-sync-agent
opencode
```

## Subagentes

1. **discovery-agent** — Relevamiento, `guia-relevamiento`, anexo celda x celda
2. **sop-agent** — SOP As-Is v3.1 híbrida (Ficha 6 campos, RN tabla, RACI 1xA, KPIs)
3. **gap-agent** — Matriz Brechas (Cómo Leer + Glosario + 5 pilares Lean + Roadmap P1/P2/P3)
4. **redesign-agent** — Business Case + SOP To-Be v3.0 (KPIs 5 filas, Firma 4 roles)
5. **auditor-agent** — Auditoría 9 dimensiones, check 1xA bloqueante
6. **continuous-learning-agent** — Reentrenamiento con protocolo validación 31/08/2026
7. **github-sync-agent** — Sync framework a GitHub via MCP `@modelcontextprotocol/server-github`

## MCP GitHub

Config en `.opencode/opencode.json`:
```json
"mcp": { "github": { "command": ["npx","-y","@modelcontextprotocol/server-github"], "environment": {"GITHUB_PERSONAL_ACCESS_TOKEN":"{env:GITHUB_TOKEN}"} } }
```
Reiniciar opencode tras editar config.

## Versionado

* **Framework:** versionar solo `.opencode/` + `README.md` + `.gitignore`
* **Excluir:** `SOP-*/`, `para revision/`, `node_modules/`, `*.xlsx/csv/txt/pdf`, `.env`
* Ver `.gitignore` en raíz

## Changelog

* **v3.2 (01/09/2026):** Reentrenamiento SOP-RRHH-001 — RACI 1xA, KPIs 4 cols, Cómo Leer/Glosario obligatorios, MCP GitHub
* **v3.1 (31/08/2026):** Plantilla híbrida sin Cómo Leer en SOP, En Pausa, diccionario SAP validado

## Autor

Farias, Gastón David — Senior BPE/BPA
