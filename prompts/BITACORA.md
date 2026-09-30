# Bitacora de tecnicas avanzadas

Laboratorio 07: Tecnicas Avanzadas de Prompting.
Herramienta de IA usada: (escribe aqui cual usaste, por ejemplo: ChatGPT o Gemini)

## Ejercicio 2: Zero-shot, one-shot y few-shot

| Tipo      | Aciertos (de 5) | Formato de la respuesta        | Todas con el mismo formato (Sí/No) |
| --------- | --------------- | ------------------------------ | ---------------------------------- |
| Zero-shot | 5               | Texto libre con explicaciones  | No                                 |
| One-shot  | 5               | Más estructurado               | No                                 |
| Few-shot  | 5               | Estricto ("texto" -> etiqueta) | Sí                                 |

## Ejercicio 3: Chain of Thought

| Pedido      | Respuesta de la IA                             | Muestra los pasos (Si/No) | Correcta (Si/No) |
| ----------- | ---------------------------------------------- | ------------------------- | ---------------- |
| Directo     | 318,60                                         | No                        | Sí               |
| Paso a paso | Desglose completo de cada operación matemática | Sí                        | Sí               |

Es útil ver el razonamiento paso a paso porque permite identificar con exactitud en qué cálculo matemático ocurrió un error en caso de que el resultado final sea incorrecto.

## Ejercicio 4: Role prompting

| Version        | Vocabulario (sencillo/tecnico) | Usa ejemplos o codigo            | A quien le sirve mas              |
| -------------- | ------------------------------ | -------------------------------- | --------------------------------- |
| A. Sin rol     | Neutral / Estándar             | No                               | Público general o consulta rápida |
| B. Rol docente | Sencillo y amigable            | Sí (la caja con etiqueta)        | Estudiantes principiantes         |
| C. Rol senior  | Técnico y avanzado             | Sí (conceptos de memoria y Java) | Desarrolladores con experiencia   |

## Ejercicio 5: Descomposicion

- **Pedido de una sola vez:** Generó un resultado genérico, desordenado y difícil de aplicar directamente al código.
- **Paso 1:** Listó correctamente los 5 requisitos específicos para una tienda pequeña.
- **Paso 2:** Diseñó las clases de forma coherente basándose en los requisitos anteriores.
- **Paso 3:** Generó el código Java exacto de la clase Producto con atributos, constructor y métodos get/set.
- **Paso 4:** Propuso 3 mejoras útiles y aplicables al código generado.

## Ejercicio 6: Prompt estructurado y autocritica

| Qué revisar                                      | Cumple (Sí / No) |
| ------------------------------------------------ | ---------------- |
| ¿Tiene las 4 columnas pedidas?                   | Sí               |
| ¿Incluye el bloqueo después de 3 intentos?       | Sí               |
| ¿Incluye casos con campos vacíos?                | Sí               |
| ¿Indica qué casos agregó en la autocrítica?      | Sí               |
| ¿Hay algún caso repetido o que no tenga sentido? | No               |

```text
<rol>Actua como analista de pruebas de software.</rol>
<contexto>Login web con correo y contrasena. La cuenta se bloquea despues de 3 intentos fallidos.</contexto>
<tarea>Piensa paso a paso que puede fallar y escribe 6 casos de prueba.</tarea>
<formato>Tabla con las columnas: ID, escenario, datos de entrada, resultado esperado.</formato>

Mensaje de autocrítica:
Revisa tu tabla: faltan casos limite como campos vacios, correo sin @ o contrasena con espacios? Agrega los que falten e indica cuales agregaste.
```
