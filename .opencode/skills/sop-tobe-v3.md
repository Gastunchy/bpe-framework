# 📘 SKILL: Reglas de Actualización del SOP To-Be Final (v3.1 Híbrida)

Este skill establece los criterios para transformar un SOP As-Is en la versión **v3.0/v3.1** híbrida optimizada (sin "Cómo Leer"):

1. **Ficha Técnica e Historial (v3.1):**
   * Incrementar a **v3.0** y usar Ficha bullet (Código/Versión/Owner/Estado/Autor).
   * En Historial condensar `v1.0-v2.2 As-Is` + fila `v3.0 Rediseño To-Be Digital`.

2. **Sección 3.1 — Calendario:**
   * Añadir 4ª columna `Detalle Operativo` parametrizado (ej. padrón SAP, feriados).

3. **Sección 5 — RACI To-Be:**
   * Eliminar roles de consolidación manual obsoleta y añadir actores digitales (Portal, BDO, Finanzas).
   * Mantener 1xA por fila, usar `—` si no aplica.

4. **Sección 7 — RN en Tabla:**
   * Convertir texto libre As-Is en tabla `ID | Regla | Aplicación` con validaciones duras (bloqueos 0.5h, medianoche 00:00/23:59, solapamiento).

5. **Sección 8 — Procedimiento con Estado:**
   * Reestructurar en FASE A-E con formato `Actor / Sistema / Acción Concreta / Cambio de Estado` (Estado obligatorio To-Be, ej. `REGISTRADO→APROBADO_HEAD`).
   * Eliminar traspaso Excel/mails, reemplazar por clics en Portal.

6. **Sección 9 — Riesgos (3 cols):**
   * Simplificar a `Riesgo / Control / Evidencia` asociando controles a validaciones automáticas y logs.

7. **Sección 10 — KPIs con Fórmula:**
   * Incorporar tablero con fórmula LaTeX y meta (Lead Time, FTR ≥98%, %Auto 100%).

> Nota 31/08/2026: Sección "Cómo Leer este Documento" excluida por decisión del autor. No generar.
