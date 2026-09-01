---
name: bpe-matrix-gap
description: Matriz Brechas Gap Analysis v3.1 (8 cols + Lean 5 pilares + Roadmap P1/P2/P3). Usar cuando SOP As-Is está listo para diagnosticar brechas y priorizar mejoras.
---

# Skill: Matriz Brechas (Gap Analysis) v3.1

---

# Matriz Brechas — [CODIGO - Nombre]

> **Proceso:** `[CODIGO - Nombre]` **SOP Ref:** `[SOP-XXX v2.2]` **Versión:** `v1.0` **Fecha:** `[DD/MM/AAAA]` **Autor:** `Farias, Gastón David`

## 1. Ficha
* **Proceso:** [Nombre largo]
* **SOP Ref:** `SOP-XXX v2.2`
* **Versión:** `v1.0`
* **Fecha:** `DD/MM/AAAA`
* **Autor:** `Equipo BPE`

## 2. Descripción
`[2-3l: Trigger, flujo E2E Excel/Macro/CSV, actores, cierre BDO/Finanzas]`

## 3. Cómo Leer
* Ficha+Descripción: alcance evaluado. Glosario: BPE/CeCo/WBS/FTR/SLA. Resumen: riesgos/cuellos. Matriz: As-Is vs To-Be. Lean: 5 pilares. Roadmap: P1/P2/P3.

## 4. Resumen Hallazgos
`[Bullets: Excel, mail, inter-sistemas, ajustes + Conclusión Alta + Portal centralizado]`

## 5. Glosario
* **BPE/CeCo/WBS/FTR/SLA:** defs.

## 6. Matriz 8c
* **ID:** `GAP-01`
* **Paso SOP:** paso As-Is
* **Situación:** cómo hoy
* **Brecha:** problema
* **Causa Raíz:** `Falta validación origen`, `Macros locales`, `Sin workflow`
* **Estado To-Be:** solución
* **Tipo Impacto ENUM:** `Calidad, Operativo, Tiempo/Retrabajo, Gobernanza/Riesgo, Técnico/Automatización`
* **Criticidad:** `Alta/Media/Baja`

| ID | Paso | Situación | Brecha | Causa | To-Be | Impacto | Criticidad |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| GAP-01 | [Fase] | [As-Is] | [Dolor] | [Causa] | [Solución] | [Tipo] | Alta |

## 7. Lean 5 Pilares
* **Rework:** [formato 0.5h, solapamiento, retroactivos]
* **Waiting:** [mail Líder/Referente/Head]
* **Over-processing:** [unificación x torre/línea]
* **Transporte Datos:** [Excel→CSV→BDO→TXT]
* **Talento:** [hs revisión celdas vs análisis]

## 8. Roadmap
* **P1 Quick Win:** alto impacto/bajo esfuerzo — Etapa1 Portal
* **P2 Mediano:** — Etapa2 Licencias / Etapa3 BDO
* **P3 Largo:** — API/SAP/BDO

| # | Iniciativa | Alcance | Esf | Imp | Pri |
| :-: | :--- | :--- | :-: | :-: | :-: |
| IN-01 | [Portal Carga/Validación] | [0.5h/solap] | M | Crítico | P1 |
| IN-02 | [Licencias] | [Nessie Portal] | M | Alto | P2 |
| IN-03 | [Export BDO] | [CSV/TXT auto] | B | Alto | P2 |
| IN-04 | [API BDO/SAP] | [máquina a máquina] | A | Medio | P3 |

## Reglas aplicación
- Ficha+Desc 2-3l + Cómo Leer 6 bullets + Resumen 4 bullets + Glosario + Matriz 8 cols + Lean 5 pilares + Roadmap P1/P2/P3. Sin Cómo Leer/Glosario → `🔴`.
- Preguntar volumen/horas/frecuencia si falta dimensionamiento
- Entrega: `GAP-SOP-XXX-v1.0.md` en `02_process_diagnosis/` con workdir
