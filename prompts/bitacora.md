# Bitacora de tecnicas avanzadas

Laboratorio 07: Tecnicas Avanzadas de Prompting.
Herramienta de IA usada: (escribe aqui cual usaste)

## Ejercicio 2: Zero-shot, one-shot y few-shot
| Tipo | Aciertos (de 5) | Formato de la respuesta | Todas con el mismo formato (Si/No) |
|---|---|---|---|
| Zero-shot | 5 | Tabla (Comentario, Clasificación) | Sí |
| One-shot | 5 | Lista numerada con comentario entre paréntesis | Sí |
| Few-shot | 5 | Texto simple con flechas ("Texto" -> Clasificación) | Sí |

## Ejercicio 3: Chain of Thought
| Pedido | Respuesta de la IA | Muestra los pasos (Si/No) | Correcta (Si/No) |
|---|---|---|---|
| Directo | 318.6 | No | Sí |
| Paso a paso | Muestra el cálculo paso a paso: Precio base (S/ 120.00), Descuento del 25% (S/ 30.00 -> S/ 90.00), e IGV del 18% (S/ 16.20 -> S/ 106.20 por unidad, total S/ 318.60 por 3 unidades). | Sí | Sí |

## Ejercicio 4: Role prompting
| Version | Vocabulario (sencillo/tecnico) | Usa ejemplos o codigo | A quien le sirve mas |
|---------|-------------------------------|-----------------------|----------------------|
| A. Sin rol | | | |
| B. Rol docente | | | |
| C. Rol senior | | | |

## Ejercicio 5: Descomposicion

## Bitácora de Descomposición
* **Paso 1 (Diseño de clases):** La IA entregó el diseño de la clase `Producto` detallando sus atributos, tipos de datos y descripciones en una tabla.
* **Paso 2 (Código Java):** La IA entregó el código fuente en Java con la estructura de la clase `Producto`, sus atributos privados, constructores y métodos getter/setter.
* **Comparación con el pedido directo:** Dividir el problema en pasos permitió obtener primero una estructura conceptual clara antes del código, mientras que pedirlo de una sola vez genera directamente la implementación sin previa validación del diseño.
## Ejercicio 6: Prompt estructurado y autocritica

## Prompot
```text
<rol>Actua como analista de pruebas de software.</rol>
<contexto>Login web con correo y contrasena. La cuenta se bloquea despues de 3 intentos fallidos.</contexto>
<tarea>Revisa tu tabla: faltan casos limite como campos vacios, correo sin @ o contrasena con espacios? Agrega los que falten e indica cuales agregaste.</tarea>
<formato>Tabla con las columnas: ID, escenario, datos de entrada, resultado esperado.</formato>
```


