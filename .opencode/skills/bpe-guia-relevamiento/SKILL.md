---
name: bpe-guia-relevamiento
description: Guía de relevamiento BPE por fases F0-F6 (empatía, gobernanza, RACI, reglas, paso a paso, riesgos). Usar al iniciar proyecto con 00_draft vacío o para entrevistar stakeholders y recolectar evidencias celda x celda.
---

# Skill: Guía Relevamiento BPE

## Propósito
Estructurar entrevistas de campo y recolección de evidencias para foto As-Is. Insumo obligatorio para discovery-agent.

## Cuándo usar
- Nuevo SOP con `00_draft/` vacío o con evidencias crudas (Excel/SAP/CSV/TXT)
- El usuario pide relevar proceso, hacer minuta o preparar cuestionario

## Workflow
1. Cargar esta skill al inicio del relevamiento
2. Aplicar cuestionario por fases:
   - **F0 Empatía:** Q0.1 Pitch café (¿qué hacés?), Q0.2 Primer día (¿qué pantalla/mail abrís?), Q0.3 Carga horaria real.
   - **F1 Gobernanza:** Q1 Propósito, Q2 Impacto si no se hace 1 mes, Q3 Trigger, Q4 Cierre exitoso, Q5-8 Alcance/calendario/cut-off.
   - **F2 RACI/SIPOC/Tec:** Q9-12 SIPOC (Suppliers/Inputs/Outputs/Customers), Q13-17 RACI/Owner/Key-Man, Q18-21 Sistemas/SAP/machetes/macros/permisos MFA.
   - **F3 Reglas:** Q22-23 Gobernanza/SoD, Q24-28 Formatos/cálculos/criterio rechazo, recargos.
   - **F4 Paso a Paso:** Q29-31 Secuencia fases, Q32-34 No felices (dato mal/caída sistema/rebote), mayor incendio último mes.
   - **F5-6 Riesgos/Dolores:** Q35-38 Riesgo/estrés/fraude/Audit Trail, Q41 Botón mágico (¿qué borrarías?), Q42 Cuello botella, Q43 Carta blanca.
3. Extraer evidencias **celda x celda** `MEMORY.md:1` (encabezados/tipo/formato/fórmulas) → insumo Anexo C para sop-agent
4. Validar sistemas vs `MEMORY.md:2` (genéricos) + `00_draft` (SAP específico). No inventar TX.
5. Generar lista de gaps informativos (corte/aprobador/tope faltante) como preguntas cortas
6. Entrega: `01_process_survey_as-is/Minuta_Relevamiento_[PROCESO].md` con `workdir="/Procesos/SOP-XXX - Nombre"`

## Output
- Minuta markdown limpio con `---`, tablas scannables
- Anexo evidencias celda x celda
- Lista preguntas pendientes
