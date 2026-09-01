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

1. **Sandbox:** Agentes operan solo en `Procesos/SOP-XXX - Nombre/`.
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
   *Cada SOP es sandbox `Procesos/SOP-XXX - Nombre`. Usar `workdir="/Procesos/SOP-XXX - Nombre"`.*

---

## 4. Aprendizajes v3.3 (01/09/2026)

* **Gobernanza:** Sin bloque Aprobaciones, solo Ficha+Historial. `auditor-checklist.md:25`
* **Plantilla Híbrida v3.1:** Sin Cómo Leer en SOP (sí en GAP/Business Case). Ficha bullet 6 campos `Código/Versión/Owner/Actualización DD/MM/AAAA/Estado/Autor`, RN `ID|Regla|Aplicación`, Paso `Actor/Sistema/Acción/Estado` (Estado opt As-Is, oblig To-Be), KPIs `KPI|Fórmula|Meta|Frecuencia` LaTeX. `template-sop.md:14`
* **En Pausa:** KPIs/instructivos `[SOLICITADO]/[SOLICITAR]` → `🟡 En Pausa` sin penalizar. `auditor-checklist.md:30`
* **RACI 1xA:** Único A por fila, `—` si no aplica. `Auditoría SOP-RRHH-001: 7x A/R→🔴`
* **Protocolo Validación 31/08/2026:** Resumen cambios → aprobación explícita → `file_write` → `MEMORY.md:55` → verificación auditor.
* **Alcance:** BPE transversal, ejemplos RRHH/Finanzas solo entrenamiento.

### 4.1 Reentrenamiento 01/09/2026

* **Origen:** Auditoría `SOP-RRHH-001 v2.2/Gap/Business Case/To-Be v3.0` — 8 gaps formato.
* **Fix 11 archivos:** `discovery: celda x celda`, `sop: Ficha 6 campos/RACI 1xA`, `gap: Cómo Leer+Glosario`, `redesign: Business Case 5 campos+Firma 4 roles`, `auditor: 1xA bloqueante`, `template/matrixtobe` normalizados. Verificado `🟢`.
* **Backup proceso-específico:** `/tmp/backup_BPE_20260901` (SAP Semantix, etc.) — no global.
