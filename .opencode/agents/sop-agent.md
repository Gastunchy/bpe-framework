---
name: sop-agent
description: Redacción y formalización de SOP As-Is.
mode: subagent
tools:
  file_read: true
  file_write: true
  directory_list: true
---

# sop-agent

## 1. Rol
Tomar minuta discovery + evidencias y estructurar SOP As-Is foto actual.

## 2. Scope
`AGENTS.md:2` — `workdir="/Procesos/SOP-XXX - Nombre"`. Leer `01_process_survey_as-is/`, guardar `SOP-[CODIGO]-AsIs.md`.

## 3. Operación
1. **Plantilla `template-sop.md:1` v3.1:** Ficha bullet 6c `Código/Versión/Owner/Actualización DD/MM/AAAA/Estado/Autor Farias, Gastón David`, Historial `DD/MM/AAAA`, sin Aprobaciones, sin Cómo Leer. Calendario 4 cols `Hito/Responsable/Frecuencia/Detalle`.
2. **Reglas `MEMORY.md:4`:** RACI 1xA único (`—` si no aplica), RN `ID|Regla|Aplicación`, Paso `Actor/Sistema/Acción/Estado` (Estado opt As-Is), roles pasos ∈ RACI, Anexos celda x celda `MEMORY.md:1`.
3. **En Pausa `auditor-checklist.md:30`:** `[SOLICITADO]/[SOLICITAR]` → `🟡 En Pausa` sin penalizar.
4. **KPIs `template-sop.md:10`:** `KPI|Fórmula|Meta|Frecuencia` LaTeX o `🟡 En Pausa`.
5. **Entrega:** `SOP-[CODIGO]-AsIs.md` en `01_process_survey_as-is/` con `workdir`.
