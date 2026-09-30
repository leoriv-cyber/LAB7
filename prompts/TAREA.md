# Tarea: Mi prompt avanzado

## Tarea elegida
Seleccioné la generación y validación de código para una API REST de gestión de inventarios en Java con Spring Boot. La idea es obtener una clase DTO con validaciones integradas, su mapeador a entidad y el controlador REST con manejo de errores básico.

## Version 1: prompt basico
```text
Crea el codigo en Java para manejar productos en una tienda usando Spring Boot.
```

## Version 2
Actua como un Desarrollador Senior backend en Java. Crea la clase ProductoDTO con campos de id, nombre y precio. Agrega validaciones con Jakarta Validation y dame un ejemplo de JSON valido y uno invalido.

## Version 3: prompt final
Actuas como un Arquitecto de Software experto en Java y Spring Boot. Tu objetivo es diseñar la arquitectura del modulo de inventario.

Analiza y piensa paso a paso lo siguiente antes de responder:
1. Define los atributos necesarios para el DTO considerando tipos de datos adecuados (usa BigDecimal para dinero).
2. Agrega validaciones estrictas en el DTO.
3. Muestra el controlador REST manejando las respuestas con ResponseEntity.

Sigue este ejemplo de formato para las validaciones:
"nombre" -> @NotBlank(message = "El nombre es obligatorio")
"precio" -> @DecimalMin(value = "0.01", message = "El precio debe ser mayor a 0")

Estructura tu respuesta exactamente en 3 secciones:
- ### 1. Entidad y DTO
- ### 2. Ejemplo de Peticiones (JSON)
- ### 3. Controlador REST

Al final, revisa tu propio código y señala 2 posibles puntos de mejora o riesgos de seguridad.

## Tecnicas usadas en el prompt final
| Parte del prompt final | Técnica correspondiente |
|---|---|
| "Actuas como un Arquitecto de Software experto en Java..." | Role Prompting |
| "Analiza y piensa paso a paso lo siguiente antes de responder..." | Chain of Thought |
| "Sigue este ejemplo de formato: 'nombre' -> @NotBlank..." | Few-shot |
| "Estructura tu respuesta exactamente en 3 secciones..." | Prompt Estructurado |
| "Al final, revisa tu propio código y señala 2 posibles puntos..." | Autocrítica |

## Evaluacion del resultado
| Criterio de evaluación | ¿Cumplió? (Sí / No) |
|---|---|
| ¿El código generado es funcional y listo para usar? | Sí |
| ¿Mantuvo el formato exacto de las 3 secciones solicitadas? | Sí |
| ¿Aplicó las reglas de validación en las propiedades del DTO? | Sí |
| ¿Encontró errores o mejoras en su propia autocrítica? | Sí |

## Por que elegi estas tecnicas
Elegí esta mezcla porque pedir código sin contexto suele dar resultados genéricos. Combinar Role Prompting con Chain of Thought obliga a la IA a analizar la arquitectura antes de programar, mientras que el Few-Shot y la estructura evitan respuestas desordenadas. Además, la autocrítica es vital para detectar fallas de seguridad antes de llevar el código a producción.