---
name: bpe-sop-tobe
description: Reglas transformación SOP As-Is → To-Be v3.0 (bump v3.0, RACI digital, RN bloqueos 0.5h/medianoche, Estado oblig). Usar con Gap validado para generar SOP To-Be final.
---

# Skill: Reglas SOP To-Be v3.1

Transforma As-Is → v3.0 sin Cómo Leer. Usar después de Matriz Brechas validada.

## Reglas transformación
1. **Ficha+Historial:** Bump `v3.0`, Ficha 6c, Historial `v1.0-v2.2 + v3.0 To-Be`.
2. **3.1 Calendario:** Añadir 4ª col `Detalle Operativo`.
3. **5 RACI:** Quitar roles manual obsoleto, añadir digitales, 1xA `—` si no aplica.
4. **7 RN tabla:** `ID|Regla|Aplicación` con bloqueos 0.5h/00:00-23:59/solap.
5. **8 Proc con Estado:** FASE A-E `Actor/Sistema/Acción/Estado` oblig (`REGISTRADO→APROBADO`).
6. **9 Riesgos 3c:** `Riesgo/Control/Evidencia` + logs.
7. **10 KPIs:** Fórmula LaTeX + meta (Lead Time, FTR ≥98%, %Auto 100%).

## Detalle operativo
- Plantilla base: `skill(bpe-template-sop)` v3.1
- Validaciones origen: 0.5h, 00:00/23:59, solapamiento
- Workflow firma digital, parametrización perfil
- Estado obligatorio en cada paso To-Be
- Entrega: `SOP-XXX-ToBe-v3.0.md` en `03_process_future_state_to-be/` con workdir
