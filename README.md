# Sistema BPE — Framework de Ingeniería de Procesos

> **Business Process Engineering (BPE) Framework v3.3** — Célula orquestadora + 6 subagentes + 7 skills para relevamiento → SOP As-Is → GAP → Business Case → SOP To-Be. Cumple ISO 9001/31000/27001.

---

## 1. Estructura

```
Sistema BPE/
├── .opencode/                  # Framework (versionado en GitHub)
│    ├── AGENTS.md              # Orquestador Leader BPE & BPA
│    ├── MEMORY.md              # Diccionario SAP/Nessie, reglas v3.3
│    ├── opencode.json          # MCP GitHub
│    ├── agents/ (7)            # discovery, sop, gap, redesign, auditor, continuous-learning, github-sync
│    └── skills/ (7)            # bpe-guia-relevamiento, bpe-template-sop, bpe-auditor-checklist, bpe-matrix-gap, bpe-business-case, bpe-sop-tobe, bpe-continuous-learning
├── Procesos/                   # Datos operativos (git-ignored)
│    └── SOP-XXX - Nombre/      # Directorio de trabajo por proceso
│        ├── 00_draft/                          # evidencias crudas Excel/SAP/CSV/TXT
│        ├── 01_process_survey_as-is/           # Minuta + SOP-AsIs.md v2.2
│        ├── 02_process_diagnosis/              # GAP-SOP-XXX-v1.0.md
│        └── 03_process_future_state_to-be/     # Business-Case + SOP-ToBe-v3.0.md
└── para revision/              # Staging alternativo solo si autor indica
```

**Regla oro — Directorio de trabajo (MANDATORY):** `AGENTS.md:7` + `MEMORY.md:34` — Cada agente opera **solo** en `Procesos/SOP-XXX - Nombre/` via `workdir="/Procesos/SOP-XXX - Nombre"`. Prohibido `../` o rutas externas. Violación = `🔴` bloqueante en auditoría.

---

## 2. Cómo funciona este framework

### 2.1 Principio orquestador

`AGENTS.md:1` — **Leader BPE & BPA** rutea según fase del proceso. Lee `MEMORY.md` antes de operar y registra correcciones. Indica siempre `Paso Actual` y `Siguiente Acción`. Tono profesional directo, entregas en Markdown limpio en `Procesos/SOP-XXX - Nombre/01-03`.

### 2.2 Ciclo de vida E2E

| Fase | Trigger | Agente | Skill | Input → Output |
| :--- | :--- | :--- | :--- | :--- |
| **F0-F6 Relevamiento** | `00_draft/` vacío o con notas/Excel/SAP | **discovery-agent** | `bpe-guia-relevamiento` — cuestionario F0 Empatía, F1 Gobernanza, F2 RACI/SIPOC/Tec, F3 Reglas, F4 Paso a Paso, F5-6 Riesgos/Dolores + evidencias celda x celda | `00_draft/` → `01_process_survey_as-is/Minuta_Relevamiento_[PROCESO].md` |
| **Foto As-Is** | Minuta completa | **sop-agent** | `bpe-template-sop` v3.1 — Plantilla Híbrida sin Cómo Leer, Ficha 6c `Código/Versión/Owner/Actualización/Estado/Autor`, Historial, Calendario 4c, RACI 1xA único (`—` si no aplica), RN `ID\|Regla\|Aplicación`, Paso `Actor/Sistema/Acción/Estado` (opt As-Is) | Minuta → `01/SOP-[CODIGO]-AsIs.md` v2.2 |
| **Diagnóstico** | SOP As-Is v2.2 listo | **gap-agent** | `bpe-matrix-gap` v3.1 — Ficha+Desc 2-3l, Cómo Leer 6 bullets, Glosario, Matriz 8c `ID/Paso/Situación/Brecha/Causa/To-Be/Impacto/Criticidad`, Lean 5 pilares, Roadmap P1/P2/P3 | Pregunta volumen/horas → `02/GAP-SOP-XXX-v1.0.md` |
| **Propuesta To-Be** | Gap validado | **redesign-agent** | `bpe-business-case` + `bpe-sop-tobe` — Business Case Header 5c + Diagnóstico 5D + ROI 75-85% hs + KPIs 5 filas + Firma 4 roles; SOP To-Be bump v3.0 con Estado oblig `REGISTRADO→APROBADO` y bloqueos 0.5h/00:00-23:59 | `02/` → `03/Business-Case-SOP-XXX-v1.0.md` + `03/SOP-XXX-ToBe-v3.0.md` |
| **Auditoría** | SOP propio o de tercero | **auditor-agent** | `bpe-auditor-checklist` — 9 dimensiones (Gobernanza, Límites, RACI, Tec, RN, Paso, Riesgos ISO31000, KPIs, Anexos/SIPOC) estados `🟢/🟡/🔴` | `01/02/03` → `Reporte_Auditoria_[DOC].md` |
| **Aprendizaje** | Fix formato/término o nuevo SAP | **continuous-learning-agent** | `bpe-continuous-learning` — escanea `01-03`, detecta patrones, propone diff `MEMORY.md`/skills, espera `sí` (protocolo 31/08/2026), verifica con auditor | `MEMORY.md` + `skills` actualizados |

**Transversal:** `github-sync-agent` — versiona framework (`.opencode/` + `README.md`) a GitHub via MCP, nunca `Procesos/` ni `*.xlsx`.

### 2.3 Reglas clave v3.3

* **Gobernanza:** Sin bloque Aprobaciones, solo Ficha+Historial `DD/MM/AAAA` — `MEMORY.md:52`
* **Plantilla v3.1:** Sin `Cómo Leer` en SOP (sí en Gap/Business Case) — `bpe-template-sop`
* **En Pausa:** `[SOLICITADO]/[SOLICITAR]` → `🟡 En Pausa` sin penalizar — `bpe-auditor-checklist`
* **RACI 1xA:** Único `A` por fila, `—` si no aplica. Duplicado `A/R` → `🔴`
* **Protocolo validación:** Resumen qué/por qué/diff → aprobación explícita → `file_write` → verificación auditor — `MEMORY.md:56`

---

## 3. Instalación

```bash
git clone https://github.com/<owner>/bpe-framework.git "Sistema BPE"
cd "Sistema BPE"
npm install # instala @opencode-ai/plugin
export GITHUB_TOKEN=ghp_xxx # para github-sync-agent
opencode
```

---

## 4. Uso rápido

1. Crea `Procesos/SOP-RRHH-001 - Envio Novedades/00_draft/` y deja evidencias crudas.
2. En opencode di `relevar SOP-RRHH-001` → `discovery-agent` genera minuta F0-F6.
3. Valida minuta → `sop-agent` genera `SOP-AsIs.md`.
4. Valida As-Is → `gap-agent` (te pregunta volumen/horas) → `GAP-*.md`.
5. Valida Gap → `redesign-agent` → Business Case + `SOP-ToBe-v3.0.md`.
6. En cualquier momento: `audita este SOP` → `auditor-agent`.

---

## 5. Subagentes

1. **discovery-agent** — Relevamiento, `bpe-guia-relevamiento`, anexo celda x celda
2. **sop-agent** — SOP As-Is v3.1 (Ficha 6c, RN tabla, RACI 1xA, KPIs LaTeX)
3. **gap-agent** — Matriz Brechas + Lean 5 pilares + Roadmap P1/P2/P3
4. **redesign-agent** — Business Case + SOP To-Be v3.0 (KPIs 5 filas, Firma 4 roles)
5. **auditor-agent** — Auditoría 9 dimensiones, check 1xA bloqueante
6. **continuous-learning-agent** — Reentrenamiento + `MEMORY.md` (protocolo 31/08/2026)
7. **github-sync-agent** — Sync framework a GitHub via MCP `@modelcontextprotocol/server-github`

## 6. Skills

| Skill | Uso |
| :--- | :--- |
| `bpe-guia-relevamiento` | Cuestionario F0-F6 + evidencias celda x celda |
| `bpe-template-sop` | Plantilla Híbrida SOP v3.1 As-Is/To-Be |
| `bpe-auditor-checklist` | Checklist 9D `🟢/🟡/🔴` |
| `bpe-matrix-gap` | Matriz 8c + Lean + Roadmap |
| `bpe-business-case` | Business Case ROI 75-85% |
| `bpe-sop-tobe` | Reglas transformación v3.0 |
| `bpe-continuous-learning` | Escaneo y actualización MEMORY |

---

## 7. MCP GitHub

Config en `.opencode/opencode.json`:
```json
"mcp": { "github": { "command": ["npx","-y","@modelcontextprotocol/server-github"], "environment": {"GITHUB_PERSONAL_ACCESS_TOKEN":"{env:GITHUB_TOKEN}"} } }
```
Reiniciar opencode tras editar config.

---

## 8. Versionado

* **Versionar:** `.opencode/` + `README.md` + `.gitignore`
* **Excluir:** `Procesos/`, `para revision/`, `node_modules/`, `*.xlsx/csv/txt/pdf`, `.env`
* Ver `.gitignore` en raíz.

---

## 9. Changelog

* **v3.3 (01/09/2026):** Directorio de trabajo mandatorio `Procesos/SOP-XXX - Nombre`, optimización tokens -38.7%, reentrenamiento 11 archivos (RACI 1xA, celda x celda, Cómo Leer/Glosario obligatorios), MCP GitHub — `MEMORY.md:59`
* **v3.2 (01/09/2026):** RACI 1xA, KPIs 4 cols, Cómo Leer/Glosario obligatorios
* **v3.1 (31/08/2026):** Plantilla híbrida sin Cómo Leer en SOP, En Pausa, diccionario SAP validado

---

## 10. Autor

Farias, Gastón David — Senior BPE/BPA
