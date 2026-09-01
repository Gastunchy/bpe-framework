# 📊 SKILL: Reglas de Diagnóstico y Matriz de Brechas (Gap Analysis BPE)

Este skill define la metodología obligatoria para categorizar desperdicios y estructurar el entregable de diagnóstico.

---

# 📄 Matriz de Brechas de Proceso (Gap Analysis) v3.1 Híbrida

> **Proceso:** `[CÓDIGO-PROCESO - Nombre del Proceso]`  
> **SOP As-Is de Referencia:** `[SOP-CÓDIGO v2.2]`  
> **Versión Actual:** `v1.0`  
> **Fecha de Análisis:** `[DD/MM/AAAA]`  
> **Elaborado por:** `Farias, Gastón David / Equipo BPE`  

---

## 1. Ficha Técnica

* **Proceso:** `[Nombre largo]`
* **SOP As-Is de Referencia:** `SOP-XXX v2.2`
* **Versión Actual:** `v1.0`
* **Fecha de Análisis:** `DD/MM/AAAA`
* **Elaborado por:** `Equipo BPE`

## 2. Breve Descripción del Proceso

`[2-3 líneas: Trigger, flujo E2E con archivos clave (Excel/Macro/CSV), actores y cierre (BDO/Finanzas).]`

## 3. Cómo Leer este Documento

* **Ficha Técnica & Descripción:** Datos normativos y alcance funcional evaluado.
* **Glosario:** Abreviaturas BPM/contable/IT (BPE, CeCo, WBS, FTR, SLA).
* **Resumen Ejecutivo:** Diagnóstico macro con riesgos, vulnerabilidades y cuellos de botella.
* **Matriz de Brechas:** Confronta paso a paso As-Is vs To-Be con causa raíz, impacto y criticidad.
* **Desperdicios Lean:** Clasificación Rework/Waiting/Over-processing/Data Transport/Unused Talent.
* **Roadmap:** Iniciativas P1/P2/P3 por Etapas para guiar transformación.

## 4. Resumen Ejecutivo de Hallazgos

`[Puntos Críticos en bullets: carga Excel, aprobaciones mail, manipulación manual inter-sistemas, ajustes retroactivos] + Conclusión Estratégica con prioridad Alta/Media y propuesta Portal centralizado.`

---

## 5. Glosario

* **BPE:** Business Process Engineering.
* **CeCo/WBS:** Centro de Costo / Work Breakdown Structure.
* **FTR/SLA:** First Time Right / Service Level Agreement.

---

## 6. Matriz de Brechas (As-Is vs. To-Be)

### Criterios de Evaluación por Columna:
* **ID:** Código secuencial (`GAP-01`, `GAP-02`, etc.).
* **Paso / Fase SOP (As-Is):** Referencia exacta al paso del manual actual donde ocurre la falla.
* **Situación Actual (As-Is):** Cómo se ejecuta hoy la tarea.
* **Brecha / Dolor Detectado:** El problema concreto (falla, demora, error de tipeo, falta de visibilidad).
* **Causa Raíz:** Por qué ocurre realmente (ej. *Falta de validaciones duras en origen, uso de macros locales, ausencia de un workflow parametrizado*).
* **Estado Deseado (Propuesta To-Be):** Solución conceptual optimizada.
* **Tipo de Impacto:** Categorías permitidas ENUM: *Calidad*, *Operativo*, *Tiempo / Retrabajo*, *Gobernanza / Riesgo*, *Técnico / Automatización* — normalizado 01/09/2026 (`Operativo/Tecnológico` → `Técnico/Automatización`).
* **Criticidad:** *Alta*, *Media* o *Baja* (fundamentada en volumen o riesgo).

| ID | Paso / Fase del SOP (As-Is) | Situación Actual (As-Is) | Brecha / Dolor Detectado | Causa Raíz (Por qué ocurre) | Estado Deseado (Propuesta To-Be) | Tipo de Impacto | Criticidad |
| :---: | :--- | :--- | :--- | :--- | :--- | :--- | :---: |
| **GAP-01** | `[Fase/Paso]` | `[Situación As-Is]` | `[Dolor / Error]` | `[Causa Raíz]` | `[Solución To-Be]` | `[Tipo Impacto]` | **`[Alta/Media/Baja]`** |

---

## 7. Categorización de Desperdicios Operativos (Lean / BPM) — 5 Pilares

* **Defectos y Retrabajos (Rework):** `[Corrección de planillas por formato 0.5h, tramos nocturnos, solapamiento, ajustes retroactivos]`.
* **Esperas y Tiempos Muertos (Waiting):** `[Respuestas mail entre Líder/Referente/Head/RRHH, cierres, consolidación]`.
* **Sobreprocesamiento (Over-processing):** `[Unificaciones múltiples: por torre, por línea Master File, consolidado RRHH, AOA]`.
* **Movimiento / Transporte de Datos Ineficiente:** `[Carga/descarga manual Excel → CSV → BDO → TXT]`.
* **Talento no Utilizado:** `[Hs de PM/Referente/RRHH en revisión de celdas vs análisis estratégico]`.

---

## 8. Priorización y Roadmap de Oportunidades por Etapas

### Criterios de Priorización:
* **P1 (Inmediata / Quick Win):** Alto impacto y esfuerzo bajo/medio — Etapa 1 Portal (Carga y Validación).
* **P2 (Mediano Plazo):** Alto/Medio impacto y esfuerzo medio/alto — Etapa 2 (Licencias) / Etapa 3 (Exportación BDO).
* **P3 (Largo Plazo):** Integración API/SAP/BDO — Esfuerzo alto.

| # | Iniciativa / Oportunidad de Mejora | Alcance de la Solución | Esfuerzo | Impacto | Prioridad |
| :-: | :--- | :--- | :-: | :-: | :-: |
| **IN-01** | `[Módulo Carga y Validación en Origen - Etapa 1]` | `[Portal web empleado/PM/Referente/Head con validaciones 0.5h, solapamiento]` | Medio | Crítico | **P1 Inmediata** |
| **IN-02** | `[Módulo Licencias - Etapa 2]` | `[Integración SAP/Nessie en Portal]` | Medio | Alto | **P2 Mediano Plazo** |
| **IN-03** | `[Motor Validación y Exportación BDO - Etapa 3]` | `[Generación auto CSV/TXT]` | Bajo | Alto | **P2 Mediano Plazo** |
| **IN-04** | `[Integración API BDO/SAP]` | `[Máquina a máquina, sin carga manual]` | Alto | Medio | **P3 Continuo** |
