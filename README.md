# Tutoría Fácil UTA — Prueba práctica integradora IHC

Universidad Técnica de Ambato · FISEI · Carrera de Software
Interacción Humano Computador · Quinto semestre · Docente: Ing. José Rubén Caiza Caizabuano, Mg.

## Problema de diseño

**Reto:** diseñar desde cero Tutoría Fácil UTA, una aplicación web móvil que permita consultar disponibilidad, reservar, confirmar y reprogramar una tutoría académica.

**Problema:** ¿Cómo permitir que un estudiante reserve o reprograme una tutoría desde un teléfono, con claridad, bajo esfuerzo cognitivo, prevención de errores y acceso mediante teclado o tecnologías de apoyo?

**Alcance:** la tarea empieza cuando el estudiante desea buscar un horario y termina cuando obtiene una confirmación comprensible; incluye la ruta para reprogramar una cita. No incluye autenticación, reportes ni administración de usuarios.

**Proceso actual:** WhatsApp, hojas de cálculo y agendas personales; 14 minutos y 9 mensajes hasta obtener una confirmación (E4).

## Integrantes y roles

| Integrante | Usuario GitHub | Rol | Rama |
|---|---|---|---|
| Acaro Ibujés Pedro Sebastián | @Sebastianyiyi | Analista DCU · dueño del repositorio | `feature/sebastian-análisis-dcu` |
| González Álvarez Vladimir Humberto | @VladAlz | Usabilidad y accesibilidad · coordinación | `feature/vladimir-usabilidad-accesibilidad` |
| Mora Beltrán Santiago Sebastián | @ | Decisiones de diseño y evaluación | `feature/santiago-...` |
| Vinces Cueva Boris Yussef | @ | Prototipo en Figma | `feature/boris-prototipo-figma` |

## Aporte de Pedro — Análisis IHC y DCU

_(Sección a cargo de Pedro: matriz humano–sistema, contexto de uso, persona, escenario, journey map y requisitos.)_

## Aporte de Vladimir — Usabilidad y accesibilidad

Evidencia: [docs/02_usabilidad_accesibilidad.pdf](docs/02_usabilidad_accesibilidad.pdf)

**Indicadores de usabilidad (ISO 9241-11)**

| Dimensión | Indicador y forma de medir | Meta |
|---|---|---|
| Efectividad | % de participantes que completan la reserva sin ayuda con una confirmación inequívoca (línea base: 4 de 12 confirmaciones ambiguas, E3) | ≥ 90 % |
| Eficiencia | Tiempo hasta ver la confirmación y número de acciones (línea base: 14 min y 9 mensajes, E4) | ≤ 2 min y ≤ 6 acciones |
| Satisfacción | Valoración posterior a la tarea en escala de 1 a 7 | Promedio ≥ 5,5 / 7 |
| Aprendizaje y errores | Éxito al primer intento, intentos de elegir un horario ocupado y recuperación con «Volver / Corregir» (E3, E10) | ≥ 80 % al primer intento; 0 horarios ocupados elegidos |

**Decisiones de accesibilidad POUR**

| Principio | Decisión | Verificación |
|---|---|---|
| Perceptible | Estados del horario y de la cita con texto y borde, no solo color; contraste ≥ 4,5:1 (E2, E9) | Inspección de las 4 pantallas |
| Operable | Orden de tabulación lógico (fecha → horario → confirmar), foco visible y área táctil ≥ 44×44 px (E1, E2) | Recorrido solo con teclado |
| Comprensible | Etiquetas completas en el calendario y mensajes que explican cómo corregir (E2, E3) | Tarea de reserva |
| Robusto | Cada componente con nombre accesible y rol definidos (E2) | Especificación en Figma: anotaciones por componente y recuadro «Especificación de accesibilidad · POUR Robusto» debajo de las pantallas |

También aporté la disciplina de ergonomía en la matriz humano–sistema y coordiné los issues del equipo.

## Aporte de Santiago — Decisiones de diseño y evaluación

_(Sección a cargo de Santiago: matriz de decisiones de diseño, leyes Gestalt y registro de la prueba cruzada.)_

## Aporte de Boris — Guía de estilo y prototipo

_(Sección a cargo de Boris: guía de estilo, cuatro pantallas conectadas y mejora aplicada.)_

## Enlaces

- Tablero FigJam del análisis: https://www.figma.com/board/RxNI7LFxOQOvLSq2LCuIog/Quetal
- Prototipo navegable: https://www.figma.com/proto/QO6lpg2qhDT3Tykj20B7Y9/Untitled?node-id=2-1380&starting-point-node-id=2%3A1380
- Archivo de diseño en Figma: https://www.figma.com/design/QO6lpg2qhDT3Tykj20B7Y9/Untitled

## Estructura del repositorio

```
PruebaParcial_IHC/
├── README.md
├── docs/
│   └── 02_usabilidad_accesibilidad.pdf     Indicadores ISO 9241-11 y decisiones POUR
├── Prototipo/
│   ├── Capturas/Pantalla1.png … Pantalla4.png
│   ├── guia_estilo.png
│   ├── EnlacePrototipo.md
│   └── Antes/Depués/                       Capturas antes/después y Cambios.md
└── evaluacion/
    └── prueba_iteracion.md                 Registro de la prueba cruzada
```

## Resumen de la prueba cruzada y mejora aplicada

- **Conducida por:** Santiago Mora.
- **Tiempo de la tarea:** 5 minutos, frente a 14 minutos del proceso actual (E4). La meta de eficiencia (≤ 2 min) todavía no se alcanza.
- **Resultado:** tarea completada, aprobada con parámetros de mejora.
- **Hallazgos y mejoras aplicadas:**
  1. Faltaba una forma de regresar durante la selección de horario → se añadió un botón de retorno (E10).
  2. Los horarios no disponibles no se entendían del todo → se añadió la metáfora del candado junto al texto «Ocupado» (E3, E9).
- **Evidencia:** [Cambios.md con capturas antes y después](Prototipo/Antes/Depu%C3%A9s/Cambios.md)
