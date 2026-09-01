# 🛡️ SKILL: Matriz de Control de Calidad y Checklist de Auditoría de SOPs BPE

Este skill establece los criterios obligatorios para auditar cualquier documento SOP y generar la devolución de calidad.

---

# 🛠️ Reporte de Auditoría y Control de Calidad BPE

> **Documento Auditado:** `[Nombre del Archivo auditado, ej: SOP-FINANZAS-001 v1.7.md]`  
> **Fecha de Auditoría:** `[DD/MM/AAAA]`  
> **Auditor:** `Subagente Auditor BPE`  

---

## 1. Resumen Ejecutivo de Auditoría

`[Síntesis de 1 o 2 párrafos sobre el estado general del documento, destacando su grado de madurez técnica y si cumple las condiciones para ser publicado o utilizado como base de desarrollo].`

---

## 2. Tabla Matriz de Evaluación por Dimensión

| Dimensión BPE | Criterios Mínimos Obligatorios v3.1 Híbrida (sin Cómo Leer) | Estado (`🟢 OK` / `🟡 Parcial` / `🔴 Ausente`) | Observaciones y Gaps Detectados |
| :--- | :--- | :---: | :--- |
| **1. Control y Gobernanza** | Ficha bullet (Código/Versión/Owner/Estado/Autor) + Historial condensado. Sin bloque Aprobadores per `MEMORY.md:58`. | `[Estado]` | `[Comentario]` |
| **2. Propósito y Límites** | Objetivo + Trigger + Alcance E2E + Exclusiones + Calendario 4 cols (Hito/Responsable/Frecuencia/Detalle). | `[Estado]` | `[Comentario]` |
| **3. Matriz Humana (RACI)** | Roles definidos + RACI con **1xA único por fila** (rechazar `A/R`/`R/A` duplicado — 7 filas fallaron 01/09/2026), uso de `—` si no aplica, quórum explícito. | `[Estado]` | `[Comentario]` |
| **4. Entorno Tecnológico** | Tabla 3 cols (Sistema/Función/Acceso) con transacciones SAP reales (`VA01/VA02/VF03/j1amonitor`) `MEMORY.md:33`. | `[Estado]` | `[Comentario]` |
| **5. Reglas de Negocio (RN)** | Tabla `ID | Regla | Aplicación` con validaciones duras (0.5h, medianoche 00:00/23:59, solapamiento). | `[Estado]` | `[Comentario]` |
| **6. Paso a Paso Operativo** | FASE A-E con `Actor/Sistema/Acción/Cambio Estado` (Estado obligatorio To-Be, opcional As-Is). Sin `[SOLICITADO]` salvo En Pausa. | `[Estado]` | `[Comentario]` |
| **7. Gestión de Riesgos** | Matriz 3 cols `Riesgo/Control/Evidencia` (ISO 31000) + Tipo Impacto opcional As-Is. | `[Estado]` | `[Comentario]` |
| **8. Medición y Desempeño** | KPIs con `Fórmula + Meta + Frecuencia` o `[En Pausa]` si pendiente reunión. | `[Estado]` | `[Comentario]` |
| **9. Modelado y Anexos** | SIPOC 4 cols + Diagrama MIRO con link + Anexos Master Data (Campo/Tipo/Descripción/Ejemplo) e Interfaz. | `[Estado]` | `[Comentario]` |

---

## 3. Plan de Acción y Recomendaciones (Gaps a Subsanar)

Para llevar el documento a nivel de excelencia (`10/10`), se deben ejecutar los siguientes ajustes:

1. **`[Punto de Mejora 1]`:** `[Acción concreta a modificar en el texto]`.
2. **`[Punto de Mejora 2]`:** `[Acción concreta a modificar en la estructura]`.
