# Estructura del TFG

Este repositorio contiene la estructura del Trabajo Final de Grado dividida por capítulos para facilitar su edición y mantenimiento.

## Estructura de archivos

- **00-introduccion.md**: Contiene la introducción, antecedentes, objetivos, hipótesis y diseño metodológico.
- **01-marco-teorico.md**: Marco teórico conceptual (Capítulo 1).
- **02-diagnostico.md**: Diagnóstico y análisis de resultados (Capítulo 2).
- **03-propuesta.md**: Propuesta y validación (Capítulo 3).
- **04-conclusiones.md**: Conclusiones y recomendaciones.
- **05-referencias.md**: Referencias bibliográficas y bibliografía.
- **06-anexos.md**: Anexos del trabajo.

## Instrucciones de uso

Cada archivo representa una sección principal del documento. Para trabajar con ellos:

1. Edite cada archivo según las necesidades de su investigación.
2. Mantenga la estructura de encabezados (# para títulos principales, ## para subtítulos, etc.)
3. Para generar el documento final, puede combinar todos los archivos en orden.

## Generación del documento completo

Para combinar todos los archivos en un único documento, puede utilizar el siguiente comando en la terminal:

```bash
cat 00-introduccion.md 01-marco-teorico.md 02-diagnostico.md 03-propuesta.md 04-conclusiones.md 05-referencias.md 06-anexos.md > documento-completo.md
```

O si necesita generar un PDF, puede utilizar herramientas como Pandoc:

```bash
pandoc 00-introduccion.md 01-marco-teorico.md 02-diagnostico.md 03-propuesta.md 04-conclusiones.md 05-referencias.md 06-anexos.md -o documento-final.pdf
``` 