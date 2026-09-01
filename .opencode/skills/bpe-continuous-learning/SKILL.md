---
name: bpe-continuous-learning
description: Aprendizaje continuo BPE - escanea entregables 01-03, detecta patrones y reentrena agents/skills. Usar para correcciones de formato o lecciones tras auditoría.
---

# Skill: Aprendizaje Continuo BPE

Protocolo para `continuous-learning-agent`:

## Flujo principal — Reentrenamiento agents/skills
1. **Escaneo:** `Procesos/SOP-XXX - Nombre/01-03` entregables finales.
2. **Detección:** Patrones recurrentes / gaps de formato en entregables (ej. GAP sin Cómo Leer, BC sin Firma/KPIs, SOP A/R duplicado).
3. **Reentrenar:** agents/skills afectados (`bpe-template-sop`, `bpe-matrix-gap`, `bpe-business-case`, `bpe-sop-tobe`).

Generar resumen qué/por qué/archivos+diff → esperar `sí` → `file_write` → verificar con `skill(bpe-auditor-checklist)`.

## Operación — Reentrenamiento agents/skills
1. **Fix recurrente:** GAP sin Cómo Leer, BC sin Firma/KPIs, SOP `A/R` duplicado → actualizar skills `bpe-template-sop`, `bpe-matrix-gap`, `bpe-business-case`, `bpe-sop-tobe` vía `skill()` o `file_write`.

## Mantenimiento MEMORY (desacoplado — flujo independiente opcional)
> Flujo separado, no contamina el reentrenamiento. Ejecutar solo si se solicita explícitamente actualizar MEMORY.

1. **Extracción:** Nuevo sistema/tx SAP/código → `MEMORY.md:2` (validar vs `00_draft` proceso).
2. **Update MEMORY:** Diccionario `MEMORY.md:2` + lecciones `MEMORY.md:4`.
3. **Historial:** Actualizar tabla procesos `Vigente/Propuesto` en `MEMORY.md`.

## Protocolo Validación 31/08/2026
Antes de `file_write` en `agents/skills` generar resumen: qué/por qué (origen ej. `SOP-RRHH-001 7x A/R→1xA`)/archivos+diff. Prohibido aplicar sin `sí/dale/aprobado`. Post: verificar con `skill(bpe-auditor-checklist)`.

## Entrega
Resumen + diff propuesto + validación auditor.
