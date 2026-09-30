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
| Mora Beltrán Santiago Sebastián | @Santio13-code | Decisiones de diseño y evaluación | `feature/santiago-decisionesevaluacion.` |
| Vinces Cueva Boris Yussef | @Boris2403 | Prototipo en Figma | `feature/boris-prototipo-figma` |

## Aporte de Sebastián — Análisis IHC y DCU

Evidencias: 
* [docs/01_matriz_ihc.pdf](docs/01_matriz_ihc.pdf)
* [docs/03_dcu_contexto.pdf](docs/03_dcu_contexto.pdf)

Como Analista DCU y dueño del repositorio, preparé la estructura inicial en `main` y aporté los fundamentos para comprender el problema actual, basándome estrictamente en el paquete de evidencias.

**1. Matriz Humano-Sistema (Actividad 1)**
Identifiqué a los actores principales y los componentes de la solución:
*   **Personas:** El estudiante busca agilidad desde su teléfono (E1), algunos con necesidad de lector de pantalla (E2). Los docentes y secretaría buscan evitar errores manuales (E6, E7).
*   **Sistema y Entrada/Salida:** La aplicación centraliza disponibilidades (E6) y devuelve estados claros para evitar ambigüedades o selecciones erróneas (E3, E10).
*   **Disciplinas:** La informática reduce mensajes (E4), la ergonomía adapta la app al bus (E1), y la psicología/diseño evitan íconos ambiguos (E2, E9).

**2. Contexto de Uso, Persona y Escenario (Actividad 3)**
Definí el contexto móvil y la conexión variable (E1, E8). Creé a "Carlos", un estudiante de 20 años que viaja en bus, usa lector de pantalla (E2) y se frustra por los 14 minutos que toma reservar por WhatsApp (E1, E4). El escenario plantea su necesidad urgente de agendar una tutoría sin perderse en el chat.

**3. Journey Map del Proceso Actual (Actividad 3)**
Mapeé las 5 etapas del problema en WhatsApp: Buscar (E1), Contactar (E6), Acordar (E3), Confirmar (E5) y Cambiar (E7). Esto evidenció la oportunidad de tener horarios en tiempo real y estados inconfundibles.

**4. Requisitos de Usuario (Actividad 3)**
Formulé 5 requisitos verificables vinculados al prototipo:
*   **RU1:** Ver solo horarios libres en el teléfono para no equivocarse (E1, E3) → Pantalla 2.
*   **RU2:** Operar con teclado para no depender del ratón (E2) → Pantallas 2 y 3.
*   **RU3:** Deshacer o corregir antes de confirmar (E10) → Pantalla 3.
*   **RU4:** Leer estado confirmado inconfundiblemente (E5, E8) → Pantalla 4.
*   **RU5:** Iniciar reprogramación sin chat (E7, E10) → Pantalla 4.

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

Evidencias:
* [docs/04_decisiones_diseno.pdf](docs/04_decisiones_diseno.pdf)
* [evaluacion/prueba_iteracion.md](evaluacion/prueba_iteracion.md)

Como encargado de las decisiones de diseño y la evaluación cruzada, formalicé los principios de IHC para garantizar una baja carga cognitiva, prevención de errores y un flujo interactivo evaluarle con usuarios.

**1. Decisiones de diseño e IHC (Actividad 4)**
* **Metáforas e Iconografía:** Utilización de la metáfora del *Calendario académico* y la *Tarjeta de cita* (E9) para reducir la curva de aprendizaje, complementada con símbolos universales (candado para elementos bloqueados/ocupados) para evitar ambigüedades.
* **Affordance y Mapeo:** Controles de horarios configurados con estados visuales diferenciados (radio-buttons, bordes y etiquetas «Disponible», «Ocupado» y «Seleccionado») para dejar claro qué elementos admiten interacción (E3, E9).
* **Manipulación Directa:** Selección directa de bloques de hora sin necesidad de escribir comandos o enviar mensajes manuales (E10).
* **Carga Cognitiva y Gestalt:** Aplicación estricta de las leyes Gestalt:
  * *Proximidad:* Agrupación de fechas y horas en bloques coherentes.
  * *Semejanza:* Estilos unificados para botones primarios y tarjetas de docentes.
  * *Figura-Fondo:* Tarjetas elevadas sobre fondos neutros para destacar la información clave y priorizar decisiones (E4, E5).
* **Retroalimentación y Riesgo Cultural:** Notificación de estado mediante confirmaciones inequívocas (resumen de cita previa a la confirmación final y alerta de éxito con número de reserva) acompañadas de texto explícito (E2, E8).

**2. Prueba Cruzada y Evaluación de Iteración (Actividad 6)**
Conduje la prueba evaluativa del prototipo navegable con un usuario externo. Se registró un tiempo de ejecución de **5 minutos** (frente a los 14 minutos del proceso manual por WhatsApp, E4) y una tasa de éxito del 100% con hallazgos para iteración.

**Mejoras concretas aplicadas al prototipo (Antes / Después):**
1. **Control de usuario y recuperación de errores (E10):** Se integró la opción explícita «Volver / Corregir» en la Pantalla de Confirmación para permitir modificar selecciones previas sin perder datos.
2. **Refuerzo de Perceptibilidad y Prevención de Errores (E3, E9):** Se añadió el icono de **candado** en la leyenda y dentro de los bloques de horarios «Ocupado», evitando intentos fallidos de selección de citas no disponibles.

---

## Aporte de Boris — Guía de estilo y prototipo 

## Actualización de la Estructura del Prototipo

Se ha actualizado la estructura de archivos del repositorio para integrar las evidencias y resultados de la fase de prototipado. A continuación se describen los nuevos elementos añadidos:

* **`Capturas/`**: Carpeta que almacena las evidencias visuales mediante capturas de pantalla de las diferentes interfaces del prototipo.
* **`EnlacePrototipo.md`**: Archivo que contiene el enlace directo al proyecto en Figma, donde se puede visualizar y ejecutar el flujo de trabajo interactivo.
* **`Antes\ Depués/`**: Directorio destinado a mostrar las iteraciones de diseño y los cambios realizados tras las pruebas de usuario. Este apartado documenta específicamente las mejoras implementadas a partir de la prueba cruzada realizada por Santiago Mora, evidenciando correcciones como la adición de un botón de retorno y la implementación de un candado visual para denotar los horarios no disponibles.


## Enlaces
- FigJam:
https://www.figma.com/board/RxNI7LFxOQOvLSq2LCuIog/Quetal?node-id=0-1&p=f&t=6QvPHekfe613jzYc-0
- Prototipo: https://www.figma.com/proto/QO6lpg2qhDT3Tykj20B7Y9/Untitled?node-id=2-1639&p=f&t=tVEyy5TupkpnkvKf-1&scaling=min-zoom&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=2%3A1380

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
# PruebaParcial_IHC





