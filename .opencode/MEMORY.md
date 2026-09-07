# MEMORY: Contexto de Negocio y Memoria BPE

> Registro centralizado de reglas, formatos y lecciones. Consultar antes de procesar.

---

## 1. Perfil Autor (Gastón Farías)

* **Rol:** Senior BPE/BPA. **Tono:** Profesional, directo, técnico.
* **Visual:** Markdown limpio, `---` entre secciones, tablas/viñetas, headers `#,##,###`.
* **Anexos:** Esquemas I/O (Excel/CSV/TXT/SAP) celda x celda: tipo, formato, validación.

---

## 2. Diccionario Sistemas Corporativos (genérico)

| Sistema | Uso |
| :--- | :--- |
| **MyAtos / NextGen** | Portal autogestión Expenses, solicitudes/aprobaciones. |
| **SAP T&E** | `PR05` auditoría gastos, `FB01` contabilización manual. |
| **SAP FI-AP** | `FBL1N` partidas acreedores, `F110` corrida pagos. |
| **Nessie** | Autogestión licencias/vacaciones/ausentismos RRHH. |
| **Conduent** | Auditoría documental Expenses, corridas pago. |
| **Interbanking** | Dispersión masiva pagos (reembolsos/nómina). |
| **BDO Payroll Events** | Plataforma externa liquidación sueldos (carga novedades). |
| **WBS / CeCo** | WBS proyecto facturable; CeCo centro costo interno. |

> SAP específico de proceso (ej. SD/CO Semantix `VA01/VA02/VF03/j1amonitor`) → ver `Procesos/SOP-XXX - Nombre/00_draft`, no global.

---

## 3. Reglas Framework BPE

1. **Directorio de trabajo:** Agentes operan solo en `Procesos/SOP-XXX - Nombre/`.
2. **Estructura Obligatoria (Opción Procesos):**
   ```
   ./ Sistema BPE
     ├── .opencode/              # framework global
     └── Procesos/               # datos operativos (git-ignored)
         └── SOP-XXX - Nombre/
             ├── 00_draft/               # evidencias crudas
             ├── 01_process_survey_as-is/
             ├── 02_process_diagnosis/
             └── 03_process_future_state_to-be/
   ```
   *Cada SOP es directorio de trabajo `Procesos/SOP-XXX - Nombre`. Usar `workdir="/Procesos/SOP-XXX - Nombre"`.*

3. **Delegación obligatoria a subagentes:** El Orquestador **NUNCA** ejecuta tareas directamente. Debe delegar siempre al subagente correspondiente según la matriz de ruteo:
   - `@discovery` → Relevamiento, ejecución de `skill(bpe-guia-relevamiento)` y llenado de anexos.
   - `@sop` → Redacción de SOP As-Is/To-Be.
   - `@gap` → Matriz de Brechas y Roadmap.
   - `@redesign` → Business Case y SOP To-Be.
   - `@auditor` → Auditorías de calidad.
   - `@continuous-learning` → Actualización de MEMORY.md y reentrenamiento.
   - `@github-sync` → Backup a GitHub.
   *Excepción: Solo el Orquestador puede editar MEMORY.md y opencode.json.*

4. **Aprobación entrenamiento:** Todo entrenamiento/aplicación de aprendizaje sobre agentes, subagentes y skills requiere **aprobación explícita del autor antes de aplicar lo entrenado**. No entrenar hasta su "OK".
5. **Protocolo de validación de cambios:** Resumen de cambios → aprobación explícita → `file_write` → registro en MEMORY → verificación.
6. **RACI SoD:** 1xA único por fila (`—` si no aplica) + **sin doble responsabilidad en la misma celda** (prohibido `R/A`, `A/R`, `C/I` o `R/I`) — quien aprueba no ejecuta (separación de funciones / ISO 31000).

---

## 4. Pendientes Activos (Seguimiento)

| ID | Proceso | Pendiente | Fecha solicitud | Nota |
| :--- | :--- | :--- | :--- | :--- |
| P01 | SOP-FINANZAS-003 O2C (§10) | Valores de KPIs (DSO, Lead Time, %Cut-off) | 02/09/2026 | Solicitud reenviada a stakeholder, esperando respuesta |

---

## 5. Aprendizajes y Entrenamientos Recientes

| Fecha | Objetivo | Qué se entrenó | Origen | Estado |
| :--- | :--- | :--- | :--- | :--- |
| 04/09/2026 | Skill `bpe-template-sop` (117→165 líneas) | M1 Estados Workflow, M2 Restricciones Calendario, M3 Callout Práctica real, M4 Anexos D/E (Evidencias + Pendientes), M5 Riesgos Tipo Impacto, M6 KPIs candidatos, M7 SIPOC viñetas, M8 Glosario tabla 2c, M9 Interfaz 6c + color celda, M10 Roles con contexto, M11 Objetivo conceptos, M12 Procesos satélite, M13 Diagrama widget Miro, M14 RN A/B/C, M15 Ficha DD/MM/AAAA, M16 Guía de Estilo Redacción (6 reglas). | Benchmark 3 SOP As-Is de alta calidad: SOP-RRHH-001 v2.2 (Novedades), SOP-FINANZAS-001 v1.7 (Expenses), SOP-RRHH-002 v1.1 (Sanciones). Aprobación explícita del autor. | Aplicado + verificado por orquestador |
| 04/09/2026 | Validación post-entrenamiento | Verificar skill actualizado con `bpe-auditor-checklist` en el próximo SOP generado con la plantilla. | Protocolo continuous-learning | Pendiente — se ejecutará en el próximo relevamiento |
| 04/09/2026 | Skills `bpe-template-sop` + `bpe-auditor-checklist` (regla RACI SoD) | Regla RACI endurecida: 1xA único por fila + **sin células mixtas** (`R/A`, `A/R`, `C/I` → 🔴) — quien aprueba no ejecuta (separación de funciones). Aplicado en §5 RACI del template, Dimensión 3.RACI + Reglas bloqueantes del auditor. | Observación del autor sobre doble responsabilidad en celda RACI (origen: hallazgos Spotlight). | Aplicado + verificado por orquestador |
