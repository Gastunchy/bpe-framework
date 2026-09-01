# 📄 SKILL: Plantilla Estándar Híbrida SOP BPE (v3.1 As-Is / To-Be) — Sin "Cómo Leer"

Esta plantilla unifica As-Is (v2.x) y To-Be (v3.0) en una sola estructura híbrida. Es el modelo obligatorio para formalizar **SOP As-Is y SOP To-Be**. No incluye sección "Cómo Leer este Documento" por decisión del autor (31/08/2026).

> **Aprendizaje 01/09/2026 (SOP-RRHH-001):** Reforzado RACI 1xA único por fila (corregido `R/A` → filas separadas), Ficha bullet 6 campos `DD/MM/AAAA`, KPIs tabla con `Frecuencia` y validación `MEMORY.md:33` (`VA01/VA02/VF03/j1amonitor`).

---

# SOP-[AREA]-[CODIGO]: [Nombre del Proceso]

> **[Tag 1] · [Tag 2] · [Tag 3]**

---

## Ficha Técnica

* **Código / ID:** `SOP-[AREA]-[CODIGO]`
* **Versión Actual:** `v2.2 As-Is` / `v3.0 To-Be`
* **Propietario del Proceso (Owner):** `[Área / Rol Responsable]`
* **Última Actualización:** `DD/MM/AAAA`
* **Estado:** `Vigente` / `En Revisión` / `Propuesto`
* **Autor:** `Farias, Gastón David / Equipo BPE`

---

## 1. Historial de Versiones

| Versión | Fecha | Descripción del Cambio | Autor |
| :---: | :---: | :--- | :--- |
| **v1.0** | DD/MM/AAAA | Documentación inicial E2E. | Equipo BPE |
| **v2.0-v2.2** | DD/MM/AAAA | Estructuración As-Is, anexos y matriz de riesgos. | Farias Gastón David |
| **v3.0** | DD/MM/AAAA | Rediseño To-Be: digitalización, controles en origen y workflow. | Equipo BPE |

---

## 2. Objetivo Principal

`[1-2 párrafos + lista de conceptos si As-Is con múltiples novedades (ej. HHEE, plus, licencias).]`

## 3. Alcance y Límites

* **Evento Disparador (Trigger):** `[Hecho o fecha exacta que da inicio al flujo.]`
* **Alcance General (End-to-End):** `[Límites inicial y final del procedimiento.]`
* **Resultado Final Esperado:** `[Entregable final o estado de cierre.]`
* **Exclusiones Expresas:** `[Procesos satélite fuera de alcance, ej. Gestión de Licencias en SAP/Nessie.]`

### 3.1 Calendario Operativo del Proceso (Ciclo de Vida)

| Hito / Fase | Responsable | Frecuencia / Plazo | Detalle Operativo |
| :--- | :--- | :--- | :--- |
| **1. [Hito Apertura]** | `[Rol]` | `[Día -5 hábil / Según necesidad]` | `[Parametrización, padrón, feriados]` |
| **2. [Hito Cierre / Corte]** | `[Rol]` | `[Día 7-8 hábil / Cut-Off]` | `[Validación y envío]` |

---

## 4. Roles y Responsabilidades

`Usar bullets si <5 roles, tabla si ≥5 roles.`

| Rol | Responsabilidad Principal | Tareas / Funciones Clave |
| :--- | :--- | :--- |
| **`[Nombre del Rol]`** | `[Resumen]` | `[Detalle de acciones operativas.]` |

---

## 5. Matriz RACI

> **R** = Responsible (Ejecuta) · **A** = Accountable (Aprueba, único por fila) · **C** = Consulted (Consultado) · **I** = Informed (Informado) — Usar `—` si no aplica

| Actividad / Paso del Proceso | [Rol 1] | [Rol 2] | [Rol 3] | [Rol 4] |
| :--- | :---: | :---: | :---: | :---: |
| **1. Carga / Inicio** | **R** | — | — | **I** |
| **2. Revisión** | — | **R** | **C** | — |
| **3. Aprobación** | — | — | — | **A** |

---

## 6. Herramientas y Sistemas

| Herramienta / Sistema | Función Principal | Control de Acceso |
| :--- | :--- | :--- |
| **`[Nombre Sistema / SAP]`** | `[Función exacta o transacción ej. VA01, CJ20N, j1amonitor]` | Perfil de usuario / Rol |

---

## 7. Reglas de Negocio y Aclaraciones

> **Formato híbrido obligatorio To-Be, recomendado As-Is:** Tabla ID | Regla | Aplicación. Se admite texto libre solo en As-Is simple.

| ID | Regla de Negocio | Aplicación en el Procedimiento |
| :--- | :--- | :--- |
| **RN01** | `[Nombre, ej. Formato de Carga 0.5h]` | `[Validación en origen, bloqueo, rango medianoche 00:00-23:59]` |
| **RN02** | `[Manejo de Excepciones]` | `[Flujo ON HOLD, desvío, criterio devolución]` |

---

## 8. Procedimiento Detallado (Paso a Paso)

> **Estructura híbrida:** Actor + Sistema + Acción + Cambio de Estado. `Cambio de Estado` obligatorio en To-Be digital, opcional en As-Is manual.

### FASE A — `[Nombre de la Fase]`

#### 1. `[Nombre del Paso]` — Actor: `[Rol]` — Sistema: `[Portal/SAP/Excel]`
* **Acción Concreta:** `[Botón que presiona, transacción VA01, validación que ejecuta]`
* **Cambio de Estado:** `ESTADO_ORIGEN → ESTADO_DESTINO` *(opcional As-Is, obligatorio To-Be)*

---

## 9. Matriz de Riesgos, Controles y Evidencias (ISO 31000)

| ID | Riesgo Identificado | Control Mitigante / Acción Preventiva | Evidencia Auditable |
| :--- | :--- | :--- | :--- |
| **R01** | `[Riesgo Operativo / Legal]` | `[Validación en origen, workflow, bloqueo]` | `[Log Portal, Acta firmada, Excel]` |

---

## 10. Indicadores de Desempeño (KPIs)

> Fórmula + Meta obligatoria To-Be, placeholder `[En Pausa - Reunión Finanzas/RRHH]` permitido As-Is.

| KPI | Fórmula | Meta | Frecuencia |
| :--- | :--- | :--- | :--- |
| `[Lead Time]` | `Fecha Pago - Fecha Apertura` | `≤2 días hábiles` | Mensual |
| `[FTR]` | `(Registros OK / Total) *100` | `≥98%` | Mensual |

---

## 11. Entradas, Salidas y Clientes/Proveedores (SIPOC)

| Proveedor | Entradas Requeridas | Salidas Generadas | Cliente (Interno/Externo) |
| :--- | :--- | :--- | :--- |
| `[Origen]` | `[Archivos / Datos]` | `[Entregables]` | `[Destino]` |

---

## 12. Diagrama de Flujo

Link al tablero Miro / Visio con swimlanes. Ej: `[SOP-XXX Swimlanes](https://miro.com/...)`

---

## 13. Glosario

| Término | Definición |
| :--- | :--- |
| `[Sigla]` | `[Definición]` |

---

## 14. Anexos Técnicos

* **Anexo A: Master Data / Campos de Carga** — Tabla `Campo | Tipo Dato | Descripción/RN | Ejemplo`
* **Anexo B: Parámetros / Políticas** — Tabla `Concepto | Criterio | Tope | Aprobación`
* **Anexo C: Interfaz / Archivos Salida** — Tabla `Campo | Posición | Tipo | Regla Formato`

Estructura celda por celda obligatoria para Excel/CSV/TXT.
