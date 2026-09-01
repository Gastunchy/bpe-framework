# 🧠 MEMORY: Contexto de Negocio, Estándares y Memoria de Proyecto BPE

> **Propósito:** Registro centralizado de contexto de negocio, diccionario de sistemas, reglas de formato del autor y estado de avance de los procesos relevados. Todos los agentes deben consultar y respetar esta memoria antes de procesar o generar documentación.

---

## 1. Perfil del Autor y Preferencias de Entrega (Gastón Farías)

* **Rol del Autor:** Senior Business Process Engineer (BPE) / Analyst (BPA).
* **Tono de Redacción:** Profesional, directo, corporativo, técnico y orientado a la excelencia operativa. Sin introducciones vacías ni respuestas conversacionales superfluas.
* **Estándar Visual:**
  * Documentos estructurados exclusivamente en **Markdown** limpios.
  * Uso de divisores horizontales `---` entre secciones principales.
  * Uso intensivo de tablas y viñetas para maximizar la lectura rápida (*scannability*).
  * Estructura de encabezados jerárquicos formal (`#`, `##`, `###`).
* **Requisito de Anexos Técnicos:** Los esquemas de datos de entrada/salida (Excel, CSV, TXT, interfaces de SAP) deben especificarse **celda por celda o columna por columna**, indicando tipo de dato, formato y reglas de validación.

---

## 2. Contexto de Negocio y Diccionario de Sistemas Corporativos

| Sistema / Término | Definición / Uso en la Organización |
| :--- | :--- |
| **MyAtos / NextGen** | Portal web de autogestión para carga de rendiciones de gastos (*Expenses*), módulos de solicitud y aprobación. |
| **SAP T&E** | Módulo de Travel & Expenses de SAP ERP. Transacciones clave: `PR05` (auditoría/carga de gastos), `FB01` (contabilización manual/contingencia). |
| **SAP FI-AP** | Módulo de Cuentas por Pagar. Transacciones clave: `FBL1N` (partidas abiertas de acreedores), `F110` (corrida automática de pagos). |
| **Nessie** | Módulo/sistema de autogestión para la administración y control de licencias médicas, vacaciones y ausentismos de RRHH. |
| **Conduent** | Proveedor de servicios operativos a cargo de la auditoría documental de Expenses y la ejecución de corridas de pago contables. |
| **Interbanking** | Plataforma bancaria corporativa utilizada para la dispersión masiva de pagos (reembolsos y liquidación de haberes/nómina). |
| **BDO Payroll Events** | Plataforma externa de la consultora de liquidación de sueldos donde se cargan las novedades procesadas. |
| **WBS (Work Breakdown Structure)** | Código de imputación para proyectos o servicios facturables a clientes. |
| **CeCo (Centro de Costo)** | Unidad de imputación contable para gastos administrativos/internos de la estructura. |
| **SAP SD/CO — Semantix Argentina (O2C)** | Mapeo local validado 31/08/2026: `VA01`= Creación Sales Order + creación Nota Débito/Crédito, `VA02`= Creación de Factura, `VF03`= Descarga de factura PDF, `CJ20N`= Creación proyecto/WBS, `j1amonitor`= Validación fiscal AFIP/ARCA. `VF01` y `J_1B3N` **no existen** en este landscape. |

---

## 3. Reglas Normativas del Framework BPE

1. **Aislamiento de Entorno (Sandboxing):** Los agentes operan **exclusivamente dentro de la carpeta local del proyecto actual**.
2. **Estructura de Carpetas Local Obligatoria (Optimizada para tokens - Opción A):**
   ```text
   ./ [Sistema BPE]
     ├── .opencode/                  <-- Agentes, Skills y MEMORY.md (global)
     ├── para revision/              <-- Bandeja de entrada staging, no estructura final
     └── SOP-XXX/                    <-- Proyecto aislado por código SOP (ej. SOP-RRHH-002, SOP-FINANZAS-003)
           ├── 00_draft/                   <-- Notas de campo, evidencias y borradores crudos
           ├── 01_process_survey_as-is/    <-- SOP As-Is v2.0
           ├── 02_process_diagnosis/       <-- Matriz de Brechas GAP-XXX
           └── 03_process_future_state_to-be/ <-- Propuesta de Mejora y SOP To-Be v3.0
   ```
   * **Regla de Optimización:** Cada SOP es un sandbox independiente. Agentes deben usar `workdir="/SOP-XXX"` para minimizar escaneo y tokens. Prohibido crear `02_process_diagnosis/` plano en raíz sin contenedor SOP-XXX.

---

## 4. Aprendizajes y Preferencias Registradas (Continuous Learning) — v3.2 (01/09/2026)

> Reglas generales migradas a skills/agents. Actualizado con reentrenamiento SOP-RRHH-001.

* **Gobernanza:** SOPs sin bloque de Aprobaciones. Auditoría valora solo Ficha + Historial. `auditor-checklist.md:25`
* **Carpetización Opción A (tokens):** Cada SOP es sandbox `SOP-XXX/00-01-02-03`, `para revision/` solo staging. `sop-agent.md:18`, `gap-agent.md:18`, `MEMORY.md:40`
* **Plantilla Híbrida v3.1:** SOP As-Is/To-Be unificados sin "Cómo Leer"; GAP y Business Case sí llevan "Cómo Leer". Ficha bullet 6 campos (`Código/Versión/Owner/Actualización DD/MM/AAAA/Estado/Autor`), RN tabla `ID|Regla|Aplicación`, Paso `Actor/Sistema/Acción/Estado` (Estado opcional As-Is, obligatorio To-Be), KPIs tabla 4 cols `KPI|Fórmula|Meta|Frecuencia` con LaTeX. `template-sop.md:14`, `sop-tobe-v3.md:1` — reforzado 01/09/2026.
* **Estados En Pausa:** KPIs y instructivos `[SOLICITADO]`/`[SOLICITAR]` se marcan `🟡 En Pausa` sin penalizar hasta reunión/delivery. `sop-agent.md:32`, `auditor-checklist.md:30`
* **Diccionario Validado:** `SAP SD/CO O2C: VA01=SO+ND/NC, VA02=Factura, VF03=Descarga, j1amonitor=Validación` — No inventar `VF01/J_1B3N`. `MEMORY.md:33`
* **Alcance:** BPE transversal para todos los procesos. Ejemplos RRHH/Finanzas solo entrenamiento, mantener templates genéricos.
* **Protocolo de Validación (31/08/2026):** Antes de modificar/entrenar cualquier agente o skill, presentar SI O SI resumen de cambios propuestos para validación del autor. No aplicar sin aprobación. _Cumplido 01/09/2026 con aprobación explícita._

### 4.1 Reentrenamiento 01/09/2026 — SOP-RRHH-001 (Aprendizaje de Paquete To-Be)

* **Origen:** Auditoría `SOP-RRHH-001 v2.2` + `Gap v1.0` + `Business Case` + `SOP To-Be v3.0` en `para revision/` — 8 gaps de formato detectados.
* **Correcciones aplicadas (11 archivos):**
  * `discovery-agent.md`: anexo celda x celda obligatorio `MEMORY.md:16`, dict SAP `VA01/VA02/VF03/j1amonitor`, `workdir="/SOP-XXX"`
  * `sop-agent.md`: Ficha bullet 6 campos `DD/MM/AAAA`, RACI 1xA único (corrección 7x `A/R` duplicado), RN tabla, Estado, `auditor-checklist.md:30`
  * `gap-agent.md`: `Cómo Leer` 6 bullets + `Glosario` obligatorios, Tipo Impacto ENUM normalizado, Roadmap P1/P2/P3
  * `redesign-agent.md`: Business Case header 5 campos + Ficha/Cómo Leer/Glosario + KPIs tabla 5 filas + Firma 4 roles + SOP To-Be RACI 1xA + `workdir="/SOP-XXX"` Opción A
  * `auditor-agent.md`: Check 1xA bloqueante, En Pausa, sin Aprobaciones, 9 dimensiones, `MEMORY.md:33`
  * `continuous-learning-agent.md`: Protocolo reforzado con verificación post-aplicación
  * `template-sop.md`: RACI ejemplo `R/A` → `R`+`A` separados
  * `auditor-checklist.md`: RACI 1xA único
  * `matrix-gap-rules.md`: Tipo Impacto ENUM
  * `tobe-business-case.md`: KPIs 4 cols con Frecuencia
* **Evidencia:** `SOP-RRHH-001/02_process_diagnosis/GAP-SOP-RRHH-001-v1.0.md` + `03_process_future_state_to-be/Business-Case-v1.0.md` + `SOP-RRHH-001-ToBe-v3.0.md` normalizados y verificados `🟢`.
* **Próximo uso:** Aplicar plantilla corregida a `SOP-RRHH-002`, `SOP-FINANZAS-003` sin repetir gaps.
