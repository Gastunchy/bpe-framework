---
name: bpe-matrix-gap
description: Matriz Brechas Gap Analysis v3.2 (8 secciones + Glosario 2 partes + Roadmap P1/P2/P3). Usar cuando SOP As-Is está listo para diagnosticar brechas y priorizar mejoras.
---

# Skill: Matriz Brechas (Gap Analysis) v3.2

---

# Matriz Brechas — [CODIGO - Nombre]

> **Proceso:** `[CODIGO - Nombre]` **SOP Ref:** `[SOP-XXX v2.2]` **Versión:** `v1.0` **Fecha:** `[DD/MM/AAAA]` **Autor:** `Farias, Gastón David`

## Estructura Obligatoria (8 secciones + Glosario)

### 1. Ficha Técnica
* **Proceso:** [Nombre largo]
* **SOP Ref:** `SOP-XXX v2.2`
* **Versión:** `v1.0`
* **Fecha:** `DD/MM/AAAA`
* **Elaborado por:** `Arquitecto de Procesos BPE`

### 2. Cómo Leer Este Documento
Redacción narrativa en párrafos (NO bullets). Explicar:
- Qué es el documento (diagnóstico formal del proceso)
- Qué contiene (estructura de 8 secciones)
- Propósito del documento

**Reglas de redacción:**
- NO usar símbolo §
- NO usar "—" (guiones largos), usar comas
- NO mencionar Lean/BPM ni ISO 31000 (a menos que el autor indique explícitamente)
- Texto fluido y profesional

### 3. Breve Descripción del Proceso
`[2-3 párrafos: Trigger, flujo E2E Excel/Macro/CSV, actores, cierre BDO/Finanzas]`

### 4. KPIs Línea Base (As-Is)
Tabla con métricas estimadas por BPE (NO KPIs formales del proceso).

**Importante:** El SOP As-Is generalmente NO define KPIs formalmente. Aclarar en la introducción que estas métricas son estimaciones del análisis BPE.

| Métrica | Valor Actual | Fuente de Información |
| :--- | :--- | :--- |
| Lead Time del ciclo | ~X días hábiles | SOP As-Is - Sección X |
| Archivos manipulados | X+ | SOP As-Is - Sección X |
| Consolidaciones manuales | X | SOP As-Is - Sección X |
| Aprobaciones manuales | X | SOP As-Is - Sección X |
| Intervenciones carga/descarga | X+ | SOP As-Is - Sección X |

### 5. Matriz de Brechas (As-Is vs. To-Be)
Breve introducción + tabla de 8 columnas.

| ID | Paso / Fase | Situación Actual | Brecha / Dolor | Causa Raíz | Estado Deseado | Tipo de Impacto | Criticidad |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| GAP-01 | [Fase] | [As-Is] | [Dolor] | [Causa] | [Solución] | [Tipo] | Alta/Media/Baja |

### 6. Categorización de Desperdicios Operativos
Breve introducción + lista de 5 tipos de ineficiencias.

* **Defectos y Retrabajos:** [descripción]
* **Esperas y Tiempos Muertos:** [descripción]
* **Sobreprocesamiento:** [descripción]
* **Movimiento / Transporte de Datos:** [descripción]
* **Talento no Utilizado:** [descripción]

### 7. Riesgos Operativos del Proceso Actual
Breve introducción + tabla de riesgos.

| ID | Riesgo Identificado | Probabilidad | Impacto | Control Actual |
| :--- | :--- | :---: | :---: | :--- |
| R01 | [riesgo] | Alta/Media/Baja | Crítico/Alto/Medio/Bajo | [control] |

### 8. Priorización y Roadmap de Oportunidades
Breve introducción + tabla con Responsible y Fecha Estimada.

| # | Iniciativa | Alcance | Esfuerzo | Impacto | Prioridad | Responsible | Fecha Estimada |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| IN-01 | [nombre] | [alcance] | Medio | Crítico | P1 Inmediata | [responsable] | TBD |

**Reglas Roadmap:**
- NO usar "Etapa X" en nombres de iniciativas
- Responsible: equipo ejecutor (ej: P&E, P&E + RRHH)
- Fecha Estimada: TBD si no se conoce

### Glosario (2 partes)

#### Abreviaturas y Siglas
| Sigla | Definición |
| :--- | :--- |
| SOP | Procedimiento Operativo Estándar |
| BPE | Business Process Engineering |
| RRHH | Recursos Humanos |
| [siglas específicas del proceso] | [definición] |

#### Términos del Documento
| Término | Definición |
| :--- | :--- |
| As-Is | Estado actual del proceso |
| To-Be | Estado futuro deseado |
| Gap / Brecha | Diferencia entre As-Is y To-Be |
| [términos específicos] | [definición] |

---

## Reglas de Aplicación

1. **Estructura obligatoria:** 8 secciones + Glosario (2 partes). Sin "Cómo Leer" o Glosario = `🔴`.
2. **Redacción:** Narrativa en párrafos para introducciones. NO bullets en "Cómo Leer". NO § ni "—".
3. **KPIs:** Aclarar que son estimaciones BPE, no KPIs formales del proceso.
4. **Roadmap:** Incluir columns Responsible y Fecha Estimada. NO usar "Etapa X".
5. **Glosario:** Dos partes: Abreviaturas y Siglas + Términos del Documento.
6. **Preguntar:** volumen/horas/frecuencia si falta dimensionamiento.
7. **Entrega:** `GAP-SOP-XXX-v1.0.md` en `02_process_diagnosis/` con workdir.
