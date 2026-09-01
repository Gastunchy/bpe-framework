---
name: bpe-auditor-checklist
description: Checklist auditoría SOP 9 dimensiones (gobernanza, RACI 1xA, RN, riesgos ISO31000). Usar para auditar SOP As-Is/To-Be propio o de terceros y generar reporte con estados 🟢/🟡/🔴.
---

# Skill: Checklist Auditoría SOP BPE

Criterios para auditar SOP y generar devolución. Ref: MEMORY.md:4

---

# Reporte Auditoría BPE

> **Documento:** `[SOP-XXX vX.X.md]` **Fecha:** `[DD/MM/AAAA]` **Auditor:** `auditor-agent`

## 1. Resumen
`[1-2 párrafos: madurez técnica, publicable como base]`

## 2. Matriz 9 Dimensiones

| Dimensión | Criterios v3.1 | Estado `🟢/🟡/🔴` | Gaps |
| :--- | :--- | :---: | :--- |
| 1.Gobernanza | Ficha 6c + Historial `DD/MM/AAAA`, sin Aprobadores `MEMORY.md:4` | [ ] | [ ] |
| 2.Límites | Objetivo+Trigger+Alcance+Exclusiones+Calendario 4c | [ ] | [ ] |
| 3.RACI | Roles + RACI 1xA único, `—` si no aplica | [ ] | [ ] |
| 4.Tecnológico | Sistema/Función/Acceso, SAP ver `00_draft` | [ ] | [ ] |
| 5.RN | `ID|Regla|Aplicación` con validaciones duras | [ ] | [ ] |
| 6.Paso a Paso | FASE A-E `Actor/Sistema/Acción/Estado` | [ ] | [ ] |
| 7.Riesgos | `Riesgo/Control/Evidencia` ISO31000 | [ ] | [ ] |
| 8.KPIs | `Fórmula+Meta+Frecuencia` o `En Pausa` | [ ] | [ ] |
| 9.Anexos | SIPOC 4c + Miro link + Master Data/Interfaz | [ ] | [ ] |

## 3. Plan Acción
1. **[Mejora 1]:** [acción concreta]
2. **[Mejora 2]:** [acción estructura]

## Reglas bloqueantes
- RACI 1xA único (`—` si no aplica) — `A/R` duplicado → `🔴`
- Sin Aprobaciones, Ficha 6c + Historial `DD/MM/AAAA`
- En Pausa: `[SOLICITADO]/[SOLICITAR]` → `🟡`
- RN `ID|Regla|Aplicación` obligatoria
- Coherencia: Roles Paso∈RACI, Riesgos mitigan GAPs, Calendario 4c

## Entrega
`Reporte_Auditoria_[DOC].md` en carpeta auditada con `workdir="/Procesos/SOP-XXX - Nombre"`
