---
name: bpe-guia-relevamiento
description: Guía de relevamiento BPE por fases F0-F6 (empatía, gobernanza, RACI, reglas, paso a paso, riesgos). Usar al iniciar proyecto con 00_draft vacío o para entrevistar stakeholders y recolectar evidencias celda x celda.
---

# Skill: Guía Relevamiento BPE — Process Discovery Master Guide

## Propósito
Estructurar entrevistas de campo y recolección de evidencias para foto As-Is. Insumo obligatorio para `discovery-agent`. Correlaciona cada bloque de preguntas con la plantilla unificada **SOP v3.1**, garantizando 0 lagunas y cumplimiento **ISO 9001/27001/31000, COBIT y SOX**. Las respuestas son insumo directo para `Entregable 1: Diagrama Miro/Swimlanes` y `Entregable 2: SOP As-Is`.

## Cuándo usar
- Nuevo SOP con `00_draft/` vacío o con evidencias crudas (Excel/SAP/CSV/TXT)
- El usuario pide relevar proceso, hacer minuta o preparar cuestionario

## Workflow
1. Cargar esta skill al inicio del relevamiento
2. Aplicar cuestionario por fases F0-F6 (ver detalle abajo)
3. Extraer evidencias **celda x celda** `MEMORY.md:1` (encabezados/tipo/formato/fórmulas) → insumo Anexo C para `sop-agent`
4. Validar sistemas vs `MEMORY.md:2` (genéricos) + `00_draft` (SAP específico). No inventar TX.
5. Generar lista de gaps informativos (corte/aprobador/tope faltante) como preguntas cortas
6. Entrega: `01_process_survey_as-is/Minuta_Relevamiento_[PROCESO].md` con `workdir="/Procesos/SOP-XXX - Nombre"`

## Output
- Minuta markdown limpio con `---`, tablas scannables
- Anexo evidencias celda x celda
- Lista preguntas pendientes

---

# Guía Universal de Relevamiento de Procesos

## 📌 Recomendaciones de Oro para el Analista (Antes de Empezar)

1. **No es un interrogatorio:** Evita leer las preguntas de forma lineal o robótica. Utiliza esta guía como **lista de verificación mental (checklist)**. Deja que el entrevistado narre el flujo de manera natural y ve marcando las respuestas que se vayan contestando solas. Al final, repasa la guía para indagar huecos informativos.
2. **El "Show me" (Mostrame):** No te quedes solo con lo que dice que hace. Solicita ver pantalla en vivo, capturas, registros reales, mails de ejemplo. La diferencia entre proceso teórico y real está en el día a día.
3. **Persigue las excepciones (Caminos No Felices):** Pregunta *"¿Qué pasa si esto falla?", "¿Qué hacen si el dato viene incompleto?", "¿Cuál fue el caso más raro del mes?"*. Allí están las verdaderas RN y riesgos.
4. **Registra la terminología local:** Anota siglas/códigos/nombres de planillas informales para el glosario.
5. **Busca la Automatización Oculta:** Indaga macros caseras, scripts locales, atajos, plantillas personales.

---

## ☕ FASE 0: ROMPER EL HIELO Y CONTEXTO HABITUAL
*Preguntas empáticas para abrir, relajar y entender el día a día. → Insumo contexto SOP.*

* **Q0.1. El Pitch de Café:** *"¿Cómo le explicarías lo que hacés a alguien que no tiene idea de tu área?"*
  > Ej: "Nos encargamos de que a ningún empleado le liquiden mal las horas extras ni se paguen facturas no autorizadas."
* **Q0.2. Primer Día de Trabajo:** *"Si hoy fuera mi primer día y me tuvieras que capacitar, ¿qué pantalla/sistema me harías abrir?"*
  > Ej: "Abrí SAP FB60 y la casilla de mails compartida de Pagos."
* **Q0.3. Carga Horaria Real:** *"¿Cuánto de tu tiempo se te va en este proceso?"*
  > Ej: "Los primeros 5 días del mes 100% de la jornada, resto 1h/día seguimiento."

---

## 📋 CUESTIONARIO ESTRUCTURADO

### FASE 1: CONTROL, GOBERNANZA Y MARCO GENERAL
*→ Completa: Ficha Técnica, S2 Objetivo, S3 Alcance y Límites SOP.*

#### 1.1. Propósito y Valor
* **Q1. Propósito Core:** ¿Cómo definirías el objetivo principal en una frase? ¿Qué valor entrega?
  > Ej: "Garantizar recepción, validación y pago en término a proveedores para evitar cortes y recargos."
* **Q2. Justificación Estratégica:** ¿Por qué existe? ¿Impacto si se deja de ejecutar 1 mes/semana?
  > Ej: "Si no se hace 1 mes, proveedores frenan materia prima y se para planta."

#### 1.2. Disparadores y Entregables
* **Q3. Trigger:** ¿Evento exacto que dispara el proceso?
  > Ej: "Día 20 de cada mes, RRHH emite mail de apertura de liquidación."
* **Q4. Output:** ¿Entregable final? ¿Cuándo se considera cerrado con éxito?
  > Ej: "Archivo .TXT de acreditación bancaria + confirmación Tesorería."

#### 1.3. Alcance, Exclusiones y Calendario
* **Q5. Fronteras E2E:** ¿Dónde empieza la primera acción y termina la última?
  > Ej: "Inicia con PR en Ariba, termina con conciliación GR/IR."
* **Q6. Exclusiones (Out of Scope):** ¿Qué queda explícitamente fuera y es de otro SOP?
  > Ej: "Licencias médicas → SOP-RRHH-005."
* **Q7. Cronograma e Hitos:** ¿Deadlines, cut-off, ventanas operativas?
  > Ej: "Corte inamovible día 8 hábil 18:00 hs para novedades."
* **Q8. Incumplimiento de Plazos:** ¿Qué pasa si no se cumple? ¿Escalamiento y contingencia?
  > Ej: "Alerta al Head, novedades pasan al mes siguiente."

---

### FASE 2: ARQUITECTURA, ROLES Y RELACIONES (SIPOC & RACI)
*→ Completa: S4 Roles, S5 RACI, S11 SIPOC.*

#### 2.1. SIPOC
* **Q9. Suppliers:** ¿Quiénes proveen datos/archivos iniciales?
  > Ej: "Líderes de Proyecto + bajada SAP Nessie."
* **Q10. Inputs:** ¿Entradas exactas y formato obligatorio?
  > Ej: "Planilla 'HHEE y Plus.xlsx' celdas amarillas + mail de aprobación."
* **Q11. Outputs:** ¿Productos/reportes/archivos generados?
  > Ej: "Archivo 'macro_AAAA_DDMMAAAA.csv' para BDO."
* **Q12. Customers:** ¿Destinatarios finales? ¿Cómo consumen?
  > Ej: "Finanzas recibe .TXT para Interbanking."

#### 2.2. Roles y Red Humana
* **Q13. Owner:** ¿Dueño final del proceso?
  > Ej: "AP Manager."
* **Q14. Participantes Operativos:** ¿Roles/áreas que ejecutan día a día?
  > Ej: "Analista AP, Referente Línea, Head, BDO, Tesorería."
* **Q15. RACI por etapa:**
  * **R (Responsible):** ¿Quién ejecuta?
  * **A (Accountable):** ¿Único aprobador? (1xA, `—` si no aplica)
  * **C (Consulted):** ¿A quién se consulta?
  * **I (Informed):** ¿A quién se notifica?
  > Ej: Consolidado: R=Referente, A=Head, C=RRHH, I=PMs.
* **Q16. Aliados y Coordinación:** *"¿Quién te responde al toque y con quién reniegas más?"*
* **Q17. Key-Man Risk:** *"Si te vas 2 semanas, ¿alguien puede hacerlo con ojos cerrados?"*
  > Ej: "Solo Laura sabe correr la Macro VBA."

#### 2.3. Herramientas y Accesos
* **Q18. Inventario Tec:** ¿ERP/SaaS/BD/repo usados?
  > Ej: "SAP S/4HANA MM/FI, Ariba, SharePoint, BDO Payroll."
* **Q19. Machetes no oficiales:** *"¿Tenés algún machete/Excel personal que te salve?"*
  > Ej: "BuscarV para cruzar legajos de altas nuevas."
* **Q20. Accesos y Permisos (ISO 27001):** ¿Usuario nominativo/MFA/VPN/perfil?
  > Ej: "Ariba VPN+MFA, SAP rol 'Analista Contable AP - MIRO'."
* **Q21. Integración y Transferencia:** ¿Export/import manual? ¿Cómo validan integridad?
  > Ej: ".CSV vía SFTP a BDO, validamos conteo registros."

---

### FASE 3: REGLAS DE NEGOCIO Y POLÍTICAS
*→ Completa: S7 Reglas de Negocio.*

#### 3.1. Gobernanza y Cumplimiento
* **Q22. Políticas Imperativas:** ¿Directrices/leyes/políticas que condicionan?
  > Ej: "No PO, No Pay."
* **Q23. SoD:** ¿Qué acciones no puede hacer la misma persona?
  > Ej: "Alta proveedor ≠ aprobación pago mismo usuario."

#### 3.2. Reglas Técnicas y Datos
* **Q24. Calidad de Entrada:** *"¿Viene limpita o haces malabares?"*
  > Ej: "Cambian columnas, ponen texto en celdas numéricas."
* **Q25. Restricciones Formato:** ¿Reglas estrictas de carga?
  > Ej: "HHEE decimal 3.5 no 3:30, legajos 5 dígitos."
* **Q26. Fórmulas/Cálculos:** ¿Cómo se calculan montos/recargos?
  > Ej: "Sábado post-13hs x2.0 (100%), semana diurna x1.5 (50%)."
* **Q27. Excepciones:** ¿Casos con criterio diferenciado?
  > Ej: "Perfil 'Franquero' no cobra 100% finde."
* **Q28. Criterio Rechazo:** ¿Cuándo se rebota al emisor?
  > Ej: "Sin PDF firmado por Head, rebote inmediato."

---

### FASE 4: PROCEDIMIENTO DETALLADO (PASO A PASO)
*→ Completa: S8 Procedimiento, S12 Diagrama.*

#### 4.1. Fases Operativas
* **Q29. Bloques Lógicos:** ¿Fases E2E?
  > Ej: "A Apertura, B Carga, C Consolidación, D Preliq, E Pago."

#### 4.2. Desglose Acción por Acción
* **Q30. Secuencia por paso:** ¿Rol? ¿Insumo? ¿Pantalla/TX/botón/planilla y acción? ¿RN aplica? ¿Salida?
  > Ej: "Analista AP abre SAP MIRO, valida 3-Way Match, contabiliza."
* **Q31. Truco del Experto:** *"¿Truco para que salga a la primera?"*
  > Ej: "Mirar solapa Detalle, código IVA debe coincidir exacto."

#### 4.3. Desvíos e Incendios
* **Q32. Decisión/Validación:** Si **Aprobado** → ¿siguiente paso? Si **Rechazado** → ¿flujo alternativo, notificación, quién corrige y vía reingreso?
  > Ej: "Diferencia >5% → Parked, ticket a Compras."
* **Q33. Incendio Real:** *"¿Mayor incendio del mes y cómo lo apagaste?"*
* **Q34. Contingencia:** ¿Plan manual si sistema/caída/ausencia?
  > Ej: "Si Ariba caído, formulario PR-Emergency.xlsx firmado por Director."

---

### FASE 5: RIESGOS, CONTROLES E INDICADORES (ISO 31000/9001/27001)
*→ Completa: S9 Riesgos, S10 KPIs.*

#### 5.1. Riesgos
* **Q35. Punto Estrés:** *"¿Qué más te estresa? ¿Paso 'que no falle nada'?"*
  > Ej: "Importar CSV a BDO, 1 CUIT mal rebota lote."
* **Q36. Vulnerabilidades:**
  * Financiero: pagos duplicados, liquidaciones erróneas, multas
  * Operativo: pérdida archivos, errores carga, cuellos botella
  * Fraude/Seguridad: modificación no autorizada, filtración, accesos no revocados

#### 5.2. Controles y Evidencia
* **Q37. Controles:** ¿Barreras/validaciones para mitigar?
  > Ej: "Control duplicados Focus Tool."
* **Q38. Evidencia Auditable:** ¿Registro que prueba control ejecutado?
  > Ej: "Mail OK gerencial + PDF corrida en SharePoint."

#### 5.3. KPIs
* **Q39. Medición Actual:** ¿Cómo mide hoy gerencia volumen/velocidad?
  > Ej: "Facturas Parked a fin de mes, % pagos a 30 días."
* **Q40. KPIs Ideales ISO 9001:**
  * Calidad: % rechazadas/corregidas
  * Tiempo: Cycle Time, % cumplimiento cut-off (SLA)
  * Productividad: registros por persona/hora
  > Ej: "First Pass Yield ≥92%."

---

### FASE 6: DOLORES, MEJORAS Y ANEXOS
*→ Completa: S13 Glosario, S14 Anexos. Insumo Gap Analysis.*

#### 6.1. Dolores (Insumo Matriz Brechas)
> Respuestas nutren directamente `GAP-SOP-XXX-v1.0.md` — `skill(bpe-matrix-gap)` 8c + Lean 5 pilares + Roadmap P1/P2/P3.

* **Q41. Botón Mágico:** *"¿Tarea más molesta que borrarías?"*
* **Q42. Cuello Botella:** ¿Tarea más lenta/repetitiva/propensa a error?
* **Q43. Carta Blanca:** *"¿Qué regla/sistema cambiarías con carta blanca?"*
* **Q43.1. Frecuencia Volumen Error:** *"De 100 registros, ¿cuántos vienen con error?"* → Criticidad/Impacto
* **Q43.2. Tiempo Retrabajo:** *"¿Hs/días perdidos destrabando?"* → Brecha/Business Case horas
* **Q43.3. Causa Raíz:** *"¿Por qué falla? ¿Capacitación/sistema/Excel sin validación?"* → Columna Causa Raíz
* **Q43.4. Parches Manuales:** *"¿Truco para que no rebote archivo?"* → Desperdicios Lean
* **Q43.5. Impacto No Cambiar:** *"¿Peor escenario si sigue igual 1 año?"* → Priorización P1/P2/P3

#### 6.2. Anexos y Glosario
* **Q44. Jerga:** ¿Siglas/acrónimos/nombres informales?
  > Ej: "Master File, DART, Nessie."
* **Q45. Tablas Maestras:** ¿Codificación/licencias/CeCo/WBS a anexar?
  > Ej: "Códigos licencia SAP 100-Vacaciones."
* **Q46. Muestras (Evidencias):** Pedir al cierre: archivos anonimizados I/O, mails tipo, capturas.

#### 6.3. Cierre
* **Q47. Pregunta Abierta Final:** *"¿Algo clave que no te pregunté y es vital para entender tu trabajo real?"*
  > Ej: "Ventana especial aguinaldo altera plazos a mitad de año."
