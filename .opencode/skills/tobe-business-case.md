# 🚀 SKILL: Guía y Estructura de la Propuesta de Mejora (Business Case To-Be)

Este skill define la plantilla ejecutiva obligatoria para vender el rediseño del proceso al negocio y la dirección.

---

# 🚀 Propuesta de Mejora de Proceso (Business Case To-Be)

> **Proceso:** `[CÓDIGO-PROCESO - Nombre del Proceso]`  
> **SOP To-Be de Referencia:** `[SOP-CÓDIGO v3.0]`  
> **Fecha de Emisión:** `[DD/MM/AAAA]`  
> **Sponsor / Owner:** `[Nombre del Process Owner / Área]`  
> **Elaborado por:** `Farias, Gastón David / Equipo BPE`  

---

## 1. Ficha Técnica y Breve Descripción del Documento

* **Proceso Evaluado:** `[SOP-XXX - Nombre]`
* **Documento de Referencia:** `Matriz de Brechas v1.0 / SOP As-Is v2.2`
* **Aprobadores Objetivo:** `[CFO, Operaciones, RRHH, CEO]`
`[2-3 líneas: finalidad del Business Case — justificar transformación digital, habilitadores OCR/IA, workflow, ROI.]`

## 2. Cómo Leer este Documento

* **Resumen Ejecutivo:** Estrategia y pilares tecnológicos + síntesis de beneficio.
* **Diagnóstico de Brechas:** Matriz 5 dimensiones (Gobernanza/Categorización/Validación/Interfaz/Control) con impacto.
* **Objetivos por Fase:** Metas cuantificables ciclo E2E (Carga/Aprobación/Integración/Preliq/Pago).
* **Viabilidad y ROI:** Factibilidad técnica, ahorros por sustitución terceros y capacidad.
* **KPIs:** Cuadro de mando 5 métricas post-implementación.
* **Próximos Pasos y Firma:** Hoja de ruta y conformidad.

## 3. Glosario

* **API/Batch/FBL1N/ROI/SLA:** `[Definiciones según proceso]` 

---

## 4. Resumen Ejecutivo

`[Visión Portal Centralizado + 4 habilitadores: 1) Auto-servicio y aprobaciones, 2) Motor de reglas en origen (tramos, recargos 50/100, medianoche), 3) Módulo licencias SAP/Nessie, 4) Interfaz autogestionada BDO/Finanzas. Beneficios: 95% menos errores formato, Lead Time 8→2 días, 75-85% menos hs.]`

---

## 5. Diagnóstico de Brechas (5 Dimensiones — Visión Gerencial)

| Dimensión | Situación Actual (As-Is) | Solución Propuesta (To-Be) | Impacto Esperado |
| :--- | :--- | :--- | :--- |
| **Gobernanza** | `[Aprobaciones mail sin aval]` | `[Workflow con firma digital]` | `[100% audit trail]` |
| **Categorización** | `[Clasificación manual Excel]` | `[Cálculo auto 50/100/nocturno]` | `[0 recargos mal liquidados]` |
| **Validación** | `[Revisión visual diferida]` | `[Validaciones activas 0.5h, solapamiento]` | `[-95% retrabajo]` |
| **Interfaz / Carga** | `[3 Excel + Macro + carga manual BDO]` | `[Consolidación auto + CSV en 1 clic]` | `[Hs → minutos]` |
| **Control Calidad** | `[Auditoría manual Excel]` | `[Matriz control tiempo real]` | `[FTR ≥98%]` |

---

## 6. Objetivos Estratégicos por Fase (A-E)

* **Fase A: Carga / Apertura (Etapa 1 Portal):** `[Automatizar apertura padrón/feriados, carga empleado/PM con imputación CeCo/WBS]`
* **Fase B: Aprobación / Gobernanza (Etapa 1):** `[Tableros PM/SDM + aprobación Head 1 clic, Referente asigna plus]`
* **Fase C: Integración (Etapa 2):** `[Módulo licencias SAP/Nessie, unificación HHEE+plus+licencias, elimina RESUMEN y AOA]`
* **Fase D: Pre-liquidación (Etapa 3):** `[Motor validación RN01-07 + interfaz macro_AAAA.csv → BDO]`
* **Fase E: Cierre / Pago:** `[Export AOA-ACREDITACION.txt → Interbanking]`

---

## 7. Análisis de Viabilidad y ROI

* **Factibilidad Técnica:** `[Alta/Media — stack Python/Web, BD relacional, APIs SAP/BDO]`
* **Ahorro Financiero:** `[Elimina sobrepagos solapados, penalizaciones gremiales, reproceso BDO]`
* **Eficiencia Capacidad:** `[75-85% reducción hs en consolidación/validación — Referentes/PMs/RRHH]`

## 8. Indicadores Clave (KPIs To-Be) — Reforzado 01/09/2026: tabla 4 cols obligatoria

| KPI | Fórmula / Definición | Meta | Frecuencia |
| :--- | :--- | :--- | :--- |
| **Lead Time** | `Fecha Pago - Fecha Apertura` | `8→2 días hábiles (≤48h)` | Mensual |
| **FTR** | `(Registros OK / Total)*100` | `≥98%` | Mensual |
| **Reversiones** | `Ajustes retroactivos / Total` | `<1%` | Mensual |
| **% Automatización** | `Campos auto / Total interfaz` | `100%` | Mensual |
| **Cumplimiento SLA** | `Cierres a tiempo / Total` | `100%` | Mensual |

---

## 9. Próximos Pasos y Plan de Implementación

1. **Aprobación Formal:** Validación de la propuesta por parte del *Process Owner* y la Dirección.
2. **Publicación Normativa:** Emisión y difusión del **SOP To-Be Final (v3.0)**.
3. **Pase a Desarrollo / Producto:** Transferencia de requerimientos a los equipos de tecnología/producto (si aplica).
4. **Capacitación y Despliegue:** Entrenamiento a usuarios operativos e implementación del nuevo estándar.

---

## 10. Firma y Conformidad

| Rol | Nombre y Apellido | Firma / Estado | Fecha |
| :--- | :--- | :---: | :---: |
| **Process Owner** | `[Nombre del Responsable]` | `[ Pendiente / Aprobado ]` | `DD/MM/AAAA` |
| **BPE Engineer** | Farias, Gastón David | `[ Elaborado ]` | `DD/MM/AAAA` |
