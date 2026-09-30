# Registro de Evaluación, Prueba Cruzada e Iteración

## 1. Registro de la Prueba Cruzada

* **Evaluador / Facilitador:** Santiago Sebastián Mora Beltrán (@SantiagoMora)
* **Participante:** Estudiante evaluador de otro grupo de IHC
* **Tarea solicitada:** Reservar una tutoría de Cálculo I para el día miércoles a las 15:00 con la Prof. Daniela Rojas y, posteriormente, validar la opción de retorno/modificación antes de confirmar.
* **Tiempo de ejecución:** 5 minutos
* **Resultado:** Aprobado con parámetros de mejora identificados.

### Matriz de Resultados

| Criterio | Observación registrada |
| :--- | :--- |
| **Completitud de la tarea** | Éxito. El usuario completó el flujo de reserva hasta la confirmación y exploró las opciones de navegación. |
| **Tiempo de tarea** | 5 minutos (incluyendo la revisión de interfaz y retroalimentación oral). |
| **Errores / Dificultades observadas** | 1. **Falta de opción clara de retorno:** En la pantalla de revisión (*Paso 2 de 3*), el usuario sintió incertidumbre sobre cómo retroceder si quería corregir la fecha u hora sin perder su avance.<br>2. **Ambigüedad en el estado de horarios:** Aunque los bloques no disponibles se diferencian por color gris, el usuario sugirió un refuerzo visual para identificar de forma inmediata qué horarios están cerrados/ocupados. |
| **Comentario del participante** | *"El flujo es bastante claro, pero en el resumen de la cita me gustaría ver un botón explícito para regresar por si me equivoco de hora, y un icono más claro en los bloques ocupados para no confundirlos."* |

---

## 2. Hallazgos e Iteración Aplicada

A partir de los hallazgos observados en la prueba cruzada, se implementaron dos mejoras concretas de diseño y usabilidad:

1. **Incorporación de la acción explícita de retorno (`Volver / Corregir`):**
   * **Problema:** La pantalla de confirmación previa solo contaba con el botón primario `Confirmar`, obligando al usuario a depender de la navegación del navegador o generar dudas sobre la pérdida de datos (Carga cognitiva / Prevención de errores, **E10**).
   * **Solución:** Se añadió un botón secundario con contorno `Volver / Corregir` inmediatamente debajo del botón principal de confirmación.

2. **Refuerzo metáfora visual de bloqueo/candado en horarios ocupados:**
   * **Problema:** Los bloques de horario ocupados dependían únicamente de texto gris y estilo de línea punteada.
   * **Solución:** Se incorporó un icono de candado en la etiqueta de la leyenda (`Ocupado`) y dentro de cada tarjeta de horario no disponible (ej. `10:30` y `18:00`), mejorando la perceptibilidad y affordance de no-interactividad (**E2, E9**).

---

## 3. Evidencia Comparativa: Antes y Después

### Mejora 1: Adición del botón de retorno en la confirmación previa (Paso 2 de 3)

| Estado | Captura | Descripción del cambio |
| :---: | :---: | :--- |
| **Antes** | ![AntesConfirmación](AntesConfirmación.png) | Solo presentaba el botón de acción principal `Confirmar`, generando duda sobre cómo corregir la selección. |
| **Después** | ![DespuésConfirmación](DespuésConfirmación.png) | Se integra el botón `Volver / Corregir` con un icono de flecha hacia la izquierda, otorgando control y libertad al usuario. |

### Mejora 2: Implementación de la metáfora de candado en horarios no disponibles

| Estado | Captura | Descripción del cambio |
| :---: | :---: | :--- |
| **Antes** | ![AntesCandado](AntesCandado.png) | Los horarios ocupados solo mostraban el texto en gris con borde punteado, pudiendo pasar desapercibidos. |
| **Después** | ![DespuésCandado](DespuésCandado.png) | Se añade el icono de candado tanto en la leyenda descriptiva como en cada tarjeta de hora ocupada (`10:30`, `18:00`). |