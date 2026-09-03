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

3. **Aprobación entrenamiento:** Todo entrenamiento/aplicación de aprendizaje sobre agentes, subagentes y skills requiere **aprobación explícita del autor antes de aplicar lo entrenado**. No entrenar hasta su "OK".
4. **Protocolo de validación de cambios:** Resumen de cambios → aprobación explícita → `file_write` → registro en MEMORY → verificación.

---

## 4. Pendientes Activos (Seguimiento)

| ID | Proceso | Pendiente | Fecha solicitud | Nota |
| :--- | :--- | :--- | :--- | :--- |
| P01 | SOP-FINANZAS-003 O2C (§10) | Valores de KPIs (DSO, Lead Time, %Cut-off) | 02/09/2026 | Solicitud reenviada a stakeholder, esperando respuesta |
