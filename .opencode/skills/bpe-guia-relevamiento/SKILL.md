---
name: bpe-guia-relevamiento
description: Guía de relevamiento BPE por fases F0-F6 (empatía, gobernanza, RACI, reglas, paso a paso, riesgos). Usar al iniciar proyecto con 00_draft vacío o para entrevistar stakeholders y recolectar evidencias celda x celda.
---

# Skill: Guía Relevamiento BPE

## Propósito
Estructurar entrevistas de campo y recolección de evidencias para foto As-Is. Insumo obligatorio para `discovery-agent`. Correlaciona cada bloque con SOP v3.1 (ISO 9001/27001/31000). Ver detalle Q0-47 en `Guia_Master_Q0-47.md` (lazy-load).

## Cuándo usar
- Nuevo SOP con `00_draft/` vacío o con evidencias crudas (Excel/SAP/CSV/TXT)
- El usuario pide relevar proceso, hacer minuta o preparar cuestionario

## Workflow ultra-eficiente
1. Cargar esta skill (35 líneas). Para entrevista profunda, `file_read Guia_Master_Q0-47.md` en misma carpeta.
2. Aplicar cuestionario por fases:
   - **F0 Empatía:** Q0.1 Pitch café, Q0.2 Primer día, Q0.3 Carga horaria.
   - **F1 Gobernanza:** Q1 Propósito, Q2 Impacto 1 mes, Q3 Trigger, Q4 Cierre, Q5-8 Alcance/calendario/cut-off.
   - **F2 RACI/SIPOC/Tec:** Q9-12 SIPOC, Q13-17 RACI/Owner/Key-Man, Q18-21 SAP/machetes/MFA.
   - **F3 Reglas:** Q22-23 Gobernanza/SoD, Q24-28 Formatos/cálculos/criterio rechazo.
   - **F4 Paso a Paso:** Q29-31 Fases/Secuencia/Truco, Q32-34 No felices/incendio/contingencia.
   - **F5-6 Riesgos/Dolores:** Q35-38 Riesgo/estrés/fraude/Audit Trail, Q41 Botón mágico, Q42 Cuello botella, Q43 Carta blanca + Q43.1-43.5 dimensionar brecha (frecuencia/tiempo/causa/parche/impacto) → insumo `bpe-matrix-gap`.
3. Extraer evidencias **celda x celda** `MEMORY.md:1` → Anexo C para `sop-agent`
4. Validar sistemas vs `MEMORY.md:2` + `00_draft` SAP específico. No inventar TX.
5. Generar lista gaps informativos (corte/aprobador/tope faltante)
6. Entrega: `01_process_survey_as-is/Minuta_Relevamiento_[PROCESO].md` con `workdir="/Procesos/SOP-XXX - Nombre"`

## Output
- Minuta markdown limpio con `---`, tablas scannables
- Anexo evidencias celda x celda
- Lista preguntas pendientes

## Anexo Master (lazy-load)
> Detalle completo Q0-47 con Recomendaciones Oro (5), ejemplos y mapeo SOP S2/S3/S4/S5/S7/S8/S9/S10/S11/S13/S14 en `Guia_Master_Q0-47.md`. No se carga por defecto para ahorrar tokens.

