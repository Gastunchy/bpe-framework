---
name: bpe-template-sop
description: Plantilla Híbrida SOP v3.1 As-Is/To-Be sin Cómo Leer. Usar para crear SOP-AsIs.md o SOP-ToBe.md desde minuta discovery y evidencias.
---

# Skill: Plantilla Híbrida SOP v3.1 (As-Is/To-Be)

Unifica As-Is/To-Be sin Cómo Leer (decisión 31/08/2026). Framework v3.3 — Ficha tabla 6c Campo|Valor, RACI 1xA único (— si no aplica), RN ID|Regla|Aplicación, Paso Actor/Sistema/Acción/Estado (opt As-Is/oblig To-Be), KPIs LaTeX, En Pausa 🟡 sin penalizar.

---

# SOP-[AREA]-[CODIGO]: [Nombre]

> **[Tag1] · [Tag2] · [Tag3]**

## Ficha Técnica
| Campo | Valor |
| :--- | :--- |
| **Código** | `SOP-[AREA]-[CODIGO]` |
| **Versión** | `v2.2 As-Is` / `v3.0 To-Be` |
| **Owner** | `[Área/Rol]` |
| **Actualización** | `DD/MM/AAAA` (siempre formato auditable `DD/MM/AAAA`, no "Julio 2026") |
| **Estado** | `Vigente/En Revisión/Propuesto` |
| **Autor** | `Farias, Gastón David / Equipo BPE` |

## 1. Historial
| Versión | Fecha | Cambio | Autor |
| :---: | :--- | :--- | :--- |
| v1.0 | DD/MM/AAAA | Inicial E2E | Equipo BPE |
| v2.2 | DD/MM/AAAA | As-Is + riesgos | Farias |
| v3.0 | DD/MM/AAAA | To-Be digital | Equipo BPE |

## 2. Objetivo
`[1-2 párrafos]`

> **Nota:** si aplica, listar conceptos/casos incluidos en el objetivo (p.ej. el listado de novedades del SOP-RRHH-001).

## 3. Alcance y Límites
* **Trigger:** `[evento inicio]`
* **Alcance E2E:** `[inicio-fin]`
* **Resultado:** `[entregable cierre]`
* **Exclusiones:** `[procesos fuera alcance]`

> **Nota:** declarar **Procesos satélite / insumos externos** — qué procesos relacionados quedan fuera del alcance y actúan como input del presente SOP.
### 3.1 Calendario
| Hito | Responsable | Frecuencia | Detalle |
| :--- | :--- | :--- | :--- |
| [Apertura] | [Rol] | [Día -5] | [padrón/feriados] |
| [Cierre] | [Rol] | [Día 7-8/Cut-Off] | [validación/envío] |

**Notas / Restricciones de Calendario:** *(opcional, recomendado)*
* Hitos fijos/inamovibles (p.ej. cierre de mes, cut-off emisión).
* Bloqueos y demoras de proveedor (p.ej. respuesta ≤72hs).
* Dependencias de aprobadores.
* Límite de retroactividad de carga.
* Plazos de prescripción (si aplica).

## 4. Roles
| Rol | Responsabilidad | Tareas |
| :--- | :--- | :--- |
| [Rol] | [Resumen] | [detalle] |

> **Nota:** agregar contexto del rol entre paréntesis cuando aplique (p.ej. `Manager (CeCo)`, `SDM (WBS)`) para distinguir aprobadores según criterio de imputación.

## 5. RACI
> R=Ejecuta A=Aprueba único C=Consultado I=Informado — `—` si no aplica

| Actividad | [Rol1] | [Rol2] | [Rol3] |
| :--- | :---: | :---: | :---: |
| 1.Carga | R | — | I |
| 2.Aprobación | — | — | A |

**Reglas bloqueantes RACI:**
- **Sin doble responsabilidad en una misma celda (SoD):** prohibido combinar `R/A`, `A/R`, `C/I` o `R/I` en una celda. El rol que aprueba (`A`) debe ser **distinto** del rol que ejecuta (`R`). Separación de Funciones (ISO 31000 / control interno).
- **1xA único por fila:** una sola celda `A` por fila (`—` si no aplica). Duplicado de `A` en celdas distintas → 🔴.
- Sin Aprobaciones, solo Ficha tabla 6c + Historial DD/MM/AAAA.

## 6. Herramientas
| Sistema | Función | Acceso |
| :--- | :--- | :--- |
| [SAP/Portal] | [TX ej. PR05] | [Perfil] |

## 7. Reglas Negocio
| ID | Regla | Aplicación |
| :--- | :--- | :--- |
| RN01 | [0.5h/medianoche] | [bloqueo origen] |
| RN02 | [Excepciones] | [ON HOLD/criterio] |

> **Formato RN válido:** tabla 3c `ID|Regla|Aplicación` **o** redacción narrativa `### RN0X: Título` + descripción. Ambos formatos son igualmente válidos.
> **Sub-estructura:** cuando una regla tenga múltiples criterios, usar sub-estructura A/B/C (`#### A.`, `#### B.`, `#### C.`).

## 8. Procedimiento
> Actor/Sistema/Acción/Estado — Estado oblig To-Be, opt As-Is
> Mientras la información esté presente (Actor, Sistema, Acción, Estado, RN), la estructura puede ser **narrativa, listado o ficha**. En encabezados de fase/paso, usar `:` o `—` de forma consistente dentro del documento o la fase.

### 8.1 Estados del Workflow *(opcional, recomendado)*
> Cada paso del procedimiento debe usar estados `ORIGEN→DESTINO`. Estado obligatorio en To-Be, recomendado en As-Is.

| Estado Origen | Estado Destino | Sistema | Significado Operativo |
| :--- | :--- | :--- | :--- |
| [ORIGEN] | [DESTINO] | [Portal/SAP] | [qué implica] |

### FASE A — [Nombre]
#### 1. [Paso] — Actor:[Rol] Sistema:[Portal/SAP]
* **Acción:** [botón/TX/validación]
* **Estado:** `ORIGEN→DESTINO`
* **RN:** `(RN01)` *(formato corto, cita única por paso — ver Guía de Estilo)*

> **Nota (Práctica real):** `[qué se hace en lugar de lo formal]` — callout para capturar la brecha entre procedimiento formal y práctica observada. Insumo directo para Gap Analysis.

## 9. Riesgos (ISO 31000)
| ID | Riesgo | Tipo de Impacto | Control | Evidencia |
| :--- | :--- | :--- | :--- | :--- |
| R01 | [Riesgo] | [Financiero/Operativo/Legal/Cumplimiento/Gobernanza] | [validación/workflow] | [Log/Acta] |

> **Nota:** Tipo de Impacto = Financiero/Operativo/Legal/Cumplimiento/Gobernanza (columna recomendada).

## 10. KPIs
| KPI | Fórmula | Meta | Frecuencia |
| :--- | :--- | :--- | :--- |
| Lead Time | `Pago-Apertura` | ≤2d háb | Mensual |
| FTR | `OK/Total*100` | ≥98% | Mensual |

Si `[SOLICITADO]/[SOLICITAR]` → `🟡 En Pausa` sin penalizar. Ver auditor-checklist.

**KPIs candidatos sugeridos** *(para solicitar al stakeholder cuando falten métricas):*
* Lead Time E2E
* % entregas en plazo
* % ON HOLD / retrabajo
* Exactitud de carga
* % automatización

## 11. SIPOC
| Proveedor | Entradas | Salidas | Cliente (Interno/Externo) |
| :--- | :--- | :--- | :--- |
| [Origen] | [Datos] | [Entregable] | [Destino] |

> **Nota:** recomendar viñetas por celda (p.ej. listar varias entradas/salidas en una misma celda con viñetas) y etiquetar la columna Cliente como `Cliente (Interno/Externo)`.

## 12. Diagrama
Link Miro/Visio swimlanes. Recomendado: link al widget exacto del board (`https://miro.com/app/board/.../?moveToWidget=...&cot=14`) y nomenclatura del archivo de diagrama (p.ej. `SOP-XXX_Diagrama_AsIs`).

## 13. Glosario
> Preferir formato tabla `Término | Definición`; viñetas como alternativa válida.

| Término | Definición |
| :--- | :--- |
| [Sigla] | [def] |

## 14. Anexos
* **A:** Master Data `Campo|Tipo|Descripción|Ejemplo`
* **B:** Parámetros `Concepto|Criterio|Tope`
* **C:** Interfaz `Col/N°|Campo|Tipo de Dato|Requerido|Formato/Ejemplo|Regla` — celda x celda oblig. Insumo discovery. Si el artefacto es Excel, indicar color de celda (amarilla = carga manual, gris = fórmula automática).
* **D:** Evidencias y Archivos Usados — mails modelo, PDFs, zip, capturas (con formato de enlace `<ruta relativa a la carpeta del SOP>`).
* **E:** Pendientes de Relevamiento — tabla `ID | Tema | Acción | Responsable | Fecha` para centralizar deuda de relevamiento (entrevistas pendientes, permisos no otorgados, KPIs por solicitar) en lugar de esparcirla en el cuerpo.

## Reglas de aplicación
- Ficha tabla 6c (2 cols `Campo|Valor`) + Historial DD/MM/AAAA sin bloque Aprobaciones
- Calendario 4c, RN tabla 3c, RACI 1xA + sin celdas mixtas (SoD)
- Entrega: `SOP-[CODIGO]-AsIs.md` en `01_process_survey_as-is/` o `SOP-[CODIGO]-ToBe-v3.0.md` en `03_process_future_state_to-be/` con workdir

## Guía de Estilo de Redacción
1. **Tiempo verbal:** As-Is → presente descriptivo (cómo ES); To-Be → obligación ("deberá/debe"). Un solo tiempo verbal por documento.
2. **Cita RN:** cada RN se cita una sola vez por paso, con formato corto `(RN01)` al final; prohibido "siguiendo estrictamente los lineamientos establecidos en la RN01..." repetido.
3. **Single source of truth:** la regla vive en una única sección (RN); calendario/procedimiento referencian, no reproducen.
4. **Jerarquía única de anotaciones:** `RN` (obligatoria) · `Nota` (aclaración operativa) · `Excepción` (desvío). Prohibido "Aclaración 1/2" como categoría paralela.
5. **Roles consistentes:** roles definidos una vez en §4 y usados IDÉNTICOS en RACI, procedimiento y glosario (copy-paste del nombre canónico).
6. **Estructura de paso:** 1 párrafo intro breve + viñetas para acciones/criterios (escaneable). Backticks para archivos, negrita para roles/sistemas. QA ortográfico antes de publicar versión.
