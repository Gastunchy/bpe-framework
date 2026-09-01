---
name: bpe-template-sop
description: Plantilla Híbrida SOP v3.1 As-Is/To-Be sin Cómo Leer. Usar para crear SOP-AsIs.md o SOP-ToBe.md desde minuta discovery y evidencias.
---

# Skill: Plantilla Híbrida SOP v3.1 (As-Is/To-Be)

Unifica As-Is/To-Be sin Cómo Leer (decisión 31/08/2026). Ref: MEMORY.md:4

---

# SOP-[AREA]-[CODIGO]: [Nombre]

> **[Tag1] · [Tag2] · [Tag3]**

## Ficha Técnica
* **Código:** `SOP-[AREA]-[CODIGO]`
* **Versión:** `v2.2 As-Is` / `v3.0 To-Be`
* **Owner:** `[Área/Rol]`
* **Actualización:** `DD/MM/AAAA`
* **Estado:** `Vigente/En Revisión/Propuesto`
* **Autor:** `Farias, Gastón David / Equipo BPE`

## 1. Historial
| Versión | Fecha | Cambio | Autor |
| :---: | :--- | :--- | :--- |
| v1.0 | DD/MM/AAAA | Inicial E2E | Equipo BPE |
| v2.2 | DD/MM/AAAA | As-Is + riesgos | Farias |
| v3.0 | DD/MM/AAAA | To-Be digital | Equipo BPE |

## 2. Objetivo
`[1-2 párrafos + lista conceptos si aplica]`

## 3. Alcance y Límites
* **Trigger:** `[evento inicio]`
* **Alcance E2E:** `[inicio-fin]`
* **Resultado:** `[entregable cierre]`
* **Exclusiones:** `[procesos fuera alcance]`
### 3.1 Calendario
| Hito | Responsable | Frecuencia | Detalle |
| :--- | :--- | :--- | :--- |
| [Apertura] | [Rol] | [Día -5] | [padrón/feriados] |
| [Cierre] | [Rol] | [Día 7-8/Cut-Off] | [validación/envío] |

## 4. Roles
| Rol | Responsabilidad | Tareas |
| :--- | :--- | :--- |
| [Rol] | [Resumen] | [detalle] |

## 5. RACI
> R=Ejecuta A=Aprueba único C=Consultado I=Informado — `—` si no aplica

| Actividad | [Rol1] | [Rol2] | [Rol3] |
| :--- | :---: | :---: | :---: |
| 1.Carga | R | — | I |
| 2.Aprobación | — | — | A |

Regla: 1xA único por fila (`—` si no aplica). Ver MEMORY.md:4.

## 6. Herramientas
| Sistema | Función | Acceso |
| :--- | :--- | :--- |
| [SAP/Portal] | [TX ej. PR05] | [Perfil] |

## 7. Reglas Negocio
| ID | Regla | Aplicación |
| :--- | :--- | :--- |
| RN01 | [0.5h/medianoche] | [bloqueo origen] |
| RN02 | [Excepciones] | [ON HOLD/criterio] |

## 8. Procedimiento
> Actor/Sistema/Acción/Estado — Estado oblig To-Be, opt As-Is
### FASE A — [Nombre]
#### 1. [Paso] — Actor:[Rol] Sistema:[Portal/SAP]
* **Acción:** [botón/TX/validación]
* **Estado:** `ORIGEN→DESTINO`

## 9. Riesgos (ISO 31000)
| ID | Riesgo | Control | Evidencia |
| :--- | :--- | :--- | :--- |
| R01 | [Operativo/Legal] | [validación/workflow] | [Log/Acta] |

## 10. KPIs
| KPI | Fórmula | Meta | Frecuencia |
| :--- | :--- | :--- | :--- |
| Lead Time | `Pago-Apertura` | ≤2d háb | Mensual |
| FTR | `OK/Total*100` | ≥98% | Mensual |

Si `[SOLICITADO]/[SOLICITAR]` → `🟡 En Pausa` sin penalizar. Ver auditor-checklist.

## 11. SIPOC
| Proveedor | Entradas | Salidas | Cliente |
| :--- | :--- | :--- | :--- |
| [Origen] | [Datos] | [Entregable] | [Destino] |

## 12. Diagrama
Link Miro/Visio swimlanes.

## 13. Glosario
| Término | Definición |
| :--- | :--- |
| [Sigla] | [def] |

## 14. Anexos
* **A:** Master Data `Campo|Tipo|Descripción|Ejemplo`
* **B:** Parámetros `Concepto|Criterio|Tope`
* **C:** Interfaz `Campo|Pos|Tipo|Regla` — celda x celda oblig. Insumo discovery.

## Reglas de aplicación
- Ficha 6c + Historial DD/MM/AAAA sin bloque Aprobaciones
- Calendario 4c, RN tabla 3c, RACI 1xA
- Entrega: `SOP-[CODIGO]-AsIs.md` en `01_process_survey_as-is/` o `SOP-[CODIGO]-ToBe-v3.0.md` en `03_process_future_state_to-be/` con workdir
