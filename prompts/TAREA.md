# Tarea: Mi prompt avanzado

## Tarea elegida

Generar los casos de prueba detallados para el módulo de registro de usuarios de una aplicación web, considerando validaciones de campos y seguridad.

## Version 1: prompt basico

Crea casos de prueba para un registro de usuarios.

- Qué técnica agregaste: Ninguna (Prompt directo / Zero-shot básico).
- Por qué: Es el punto de partida para ver cómo responde la IA sin restricciones.
- Qué mejoró en la respuesta: Da una lista muy general y básica, pero sin un formato estructurado ni casos límite claros.

## Version 2

<rol>Actua como analista de calidad de software (QA).</rol>
<contexto>El sistema web registra nuevos usuarios pidiendo correo, contrasena y confirmacion.</contexto>
<tarea>Escribe 5 casos de prueba considerando entradas validas e invalidas.</tarea>

- Qué técnica agregaste: Prompt estructurado (usando etiquetas) y Role prompting.
- Por qué: Para darle un rol técnico específico a la IA y organizar mejor los parámetros de entrada y contexto.
- Qué mejoró en la respuesta: Los casos de prueba ahora son más profesionales y enfocados en QA, aunque todavía falta detallar el razonamiento paso a paso de los escenarios límite.

## Version 3: prompt final

<rol>Actua como analista de calidad de software (QA).</rol>
<contexto>El sistema web registra nuevos usuarios pidiendo correo, contrasena y confirmacion.</contexto>
<instrucciones>Piensa paso a paso los posibles fallos de seguridad y validacion antes de estructurar la tabla.</instrucciones>
<tarea>Escribe 6 casos de prueba detallados.</tarea>
<formato>Tabla con columnas: ID, Escenario, Datos de entrada, Resultado esperado.</formato>

- Qué técnica agregaste: Chain of Thought (piensa paso a paso) y formato de tabla estricto.
- Por qué: Para obligar a la IA a razonar los fallos ocultos y entregar una estructura limpia lista para documentación.
- Qué mejoró en la respuesta: Generó casos robustos con manejo de errores profundos y una tabla limpia perfecta para el reporte.

## Tecnicas usadas en el prompt final

| Técnica aplicada    | Dónde se ubica en el prompt final                                          |
| ------------------- | -------------------------------------------------------------------------- |
| Role prompting      | `<rol>Actua como analista de calidad de software (QA).</rol>`              |
| Prompt estructurado | Uso de etiquetas de contexto, instrucciones y formato                      |
| Chain of Thought    | `<instrucciones>Piensa paso a paso los posibles fallos...</instrucciones>` |

## Evaluacion del resultado

| Criterio de evaluación                  | Cumple (Sí / No) |
| --------------------------------------- | ---------------- |
| ¿Utiliza un rol específico y técnico?   | Sí               |
| ¿Combina al menos 3 técnicas avanzadas? | Sí               |
| ¿Presenta las 3 versiones solicitadas?  | Sí               |
| ¿Incluye la tabla de mapeo de técnicas? | Sí               |

## Por que elegi estas tecnicas

Elegí el role prompting para darle contexto profesional a la IA, el prompt estructurado mediante etiquetas para evitar ambigüedades en las instrucciones, y el Chain of Thought para garantizar que no se pasen por alto errores críticos de validación en el formulario de registro.
