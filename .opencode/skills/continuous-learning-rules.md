# ⚙️ SKILL: Reglas de Aprendizaje Continuo y Re-Entrenamiento BPE

Este skill define el protocolo algorítmico que debe seguir el **`continuous-learning-agent`** para procesar nuevo conocimiento y re-entrenar la célula de agentes.

---

## 1. Protocolo de Extracción de Patrones

Cada vez que un proceso sea completado o validado por el analista de proceso, el Subagente de Aprendizaje Continuo ejecutará el siguiente análisis de 4 pasos:

```text
 ┌────────────────────────┐      ┌────────────────────────┐      ┌────────────────────────┐
 │ 1. Escaneo de Archivos │ ───► │ 2. Detección de Novedad│ ───► │ 3. Actualización de    │
 │    en Subcarpetas      │      │    (Nuevos Patrones)   │      │    MEMORY.md           │
 └────────────────────────┘      └────────────────────────┘      └───────────┬────────────┘
                                                                             │
                                                                             ▼
                                                                 ┌────────────────────────┐
                                                                 │ 4. Re-entrenamiento de │
                                                                 │    Subagentes & Skills │
                                                                 └────────────────────────┘
