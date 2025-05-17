---
# Tarea 5: Presentación del avance de la propuesta
---

# CAPÍTULO 3. PROPUESTA Y VALIDACIÓN (Avance)

## 3.1. Esquema general de la propuesta

La propuesta central de este proyecto de investigación es el **Desarrollo y Evaluación de un Producto Mínimo Viable (MVP) basado en Inteligencia Artificial (IA)** diseñado específicamente para la **Generación Eficiente de Identificación de Casos de Pruebas en Equipos Ágiles**. Este MVP busca transformar el proceso actual de testing en la empresa Patito SRL, que, como se detalla en el Capítulo 2 (Diagnóstico), presenta ineficiencias significativas debido a su alta dependencia del esfuerzo humano manual y la variabilidad asociada.

El **objeto de estudio** que se busca transformar es el **proceso de generación e identificación de casos de prueba en los equipos ágiles**, mientras que el **campo de acción** se enfoca en la **eficiencia** de este proceso. La propuesta se enmarca dentro de la **línea de investigación en Ingeniería de Software** y el **eje temático de Validación, Mantenimiento y Evolución del Software**, aplicando conocimientos del área de **Inteligencia Artificial Aplicada al Testing**.

El MVP se concibe como un sistema que, utilizando técnicas de IA, asistirá a los ingenieros de QA en la tarea de identificar y diseñar casos de prueba a partir de requisitos (historias de usuario), aprendiendo de datos históricos y patrones para proponer escenarios de prueba más completos y diversos, reduciendo el tiempo y esfuerzo manual.

### 3.1.1. Por qué del cómo del objetivo general

El Objetivo General ("Desarrollar un producto mínimo viable basado en Inteligencia Artificial para la Generación Eficiente de Identificación de Casos de Pruebas en Equipos Ágiles, que demuestre la mejora significativa en la eficiencia del proceso de validación de software en la empresa Patito SRL durante la gestión 2025") se aborda mediante el desarrollo y evaluación experimental de un MVP por las siguientes razones, fundamentadas en el diagnóstico y marco teórico:

1.  **Abordar problemas críticos identificados en el diagnóstico:** El diagnóstico (Capítulo 2) reveló que la alta dependencia del factor humano (Prioridad 1), la insuficiente cobertura de escenarios no triviales (Prioridad 2), el bajo aprovechamiento de datos históricos (Prioridad 3) y la capacidad limitada para adaptar casos ante cambios (Prioridad 4) son los principales cuellos de botella y áreas de ineficiencia. Un MVP basado en IA está diseñado precisamente para mitigar estos problemas mediante automatización inteligente, aprendizaje a partir de datos y adaptación a cambios.
2.  **Aplicar soluciones de vanguardia validadas teóricamente:** El marco teórico (Capítulo 1, especialmente 1.1.3, 1.1.4, 1.4) confirma que la aplicación de IA (ML, NLP) al testing es una tendencia consolidada y con resultados positivos documentados (Baqar & Khanda, 2024; Ramadan et al., 2024; Garousi et al., 2022). La implementación de un MVP permite aplicar estas técnicas al contexto específico de Patito SRL y validar empíricamente sus beneficios.
3.  **Lograr eficiencia y efectividad:** El MVP apunta a mejorar métricas clave como el tiempo promedio por historia de usuario, los casos de prueba por hora-persona, la cobertura de requisitos (explícitos e implícitos) y la relevancia para la detección de defectos (Cuadro 4, Capítulo 2). La IA, al aprender patrones y sugerir escenarios, puede aumentar la productividad y la calidad de los casos generados más allá de lo que se logra manualmente (Nair et al., 2021).
4.  **Adecuación al contexto ágil de Patito SRL:** Un MVP con enfoque en la generación de casos de prueba se alinea con la necesidad de "testing first" y la integración continua en entornos ágiles (Capítulo 1.3). Permite obtener feedback rápido sobre la propuesta de valor, adaptarse a las dinámicas del equipo y validar la solución de manera incremental (Crispin & Gregory, 2022).
5.  **Validación económica y de factibilidad:** El enfoque de MVP permite una inversión inicial controlada para evaluar el retorno potencial (Justificación Económica, Capítulo 00), verificando la factibilidad técnica de aplicar IA en el contexto de Patito SRL (Cuadro 5, Capítulo 2) antes de un despliegue a gran escala.
6.  **Aportación metodológica y práctica:** Desarrollar y evaluar este MVP constituye una aplicación concreta de los métodos cuasi-experimentales (Capítulo 00, 6.1), generando conocimiento sobre cómo implementar y medir el impacto de soluciones de IA en procesos de testing ágil (Justificación Metodológica, Capítulo 00).

En resumen, el MVP basado en IA es el "cómo" (la solución) que responde al "por qué" (resolver los problemas identificados y lograr los objetivos de eficiencia) basándose en el "qué" (el conocimiento teórico y el diagnóstico del contexto).

## 3.2. Desarrollo de la propuesta (Elementos de la estructura del MVP)

Aunque el detalle completo del desarrollo se abordará en secciones posteriores (marcadas como WIP en el archivo 03-propuesta.md), la estructura conceptual del MVP se define a partir de los requisitos de diseño derivados del diagnóstico (Cuadro 5, Capítulo 2) y los requisitos transversales (RT1-RT5):

Los principales elementos que estructuran la propuesta de MVP son:

1.  **Módulo de Entrada de Requisitos:** Recibirá como input las historias de usuario o especificaciones textuales (R6, R7). Deberá integrarse con herramientas existentes como Jira (R7).
2.  **Módulo de Análisis de Lenguaje Natural (NLP):** Procesará el texto de los requisitos para extraer entidades, acciones, condiciones, reglas de negocio y posibles escenarios de prueba. Utilizará técnicas de NLP avanzadas para comprender semántica y detectar ambigüedades (R6, Capítulo 1.4.3).
3.  **Módulo de Generación Inteligente de Escenarios/Casos:** Aplicará técnicas de Machine Learning (aprendizaje supervisado, por refuerzo o algoritmos genéticos) para proponer escenarios de prueba, incluyendo casos límite, flujos alternativos y condiciones de error, basándose en el análisis de requisitos y patrones aprendidos de datos históricos (R1, R2, R3, Capítulo 1.4.2).
4.  **Repositorio de Datos Históricos:** Almacenará y gestionará datos de casos de prueba previos, resultados de ejecución y patrones de defectos para entrenar y refinar los modelos de IA (R3).
5.  **Módulo de Adaptación al Cambio:** Incorporará lógica para identificar el impacto de las modificaciones en los requisitos y sugerir ajustes a los casos de prueba existentes (R4).
6.  **Módulo de Documentación y Exportación:** Generará automáticamente documentación estructurada de los casos de prueba identificados en formatos compatibles con herramientas como TestRail (R5, R7).
7.  **Interfaz de Usuario Intuitiva:** Proporcionará un medio visual para que los ingenieros de QA interactúen con el sistema, revisen y refinen las sugerencias de casos, proporcionen feedback y gestionen el proceso (RT2).
8.  **Mecanismo de Validación Humana:** Integrará puntos de control donde los ingenieros de QA puedan validar, modificar o descartar los casos de prueba generados automáticamente, manteniendo el control sobre la calidad (RT1, RT2).
9.  **Módulo de Monitoreo y Mejora:** Capturará métricas sobre el uso y rendimiento del MVP (precisión, tiempo ahorrado) para identificar oportunidades de mejora y reentrenar modelos (RT1, RT4, RT5).
10. **Capa de Integración (API):** Facilitará la conexión con otras herramientas del pipeline de desarrollo y testing de Patito SRL (Jira, TestRail, potencialmente herramientas de automatización de ejecución) (R7, RT4).
11. **Consideraciones de Seguridad y Privacidad:** Implementará controles de acceso, protección de datos y cumplimiento de políticas internas (RT3).

Estos elementos definen la arquitectura conceptual del MVP y las capacidades clave que se desarrollarán y evaluarán experimentalmente para validar la hipótesis de que esta solución mejorará significativamente la eficiencia en la generación de casos de prueba en el contexto de Patito SRL.

## 3.3. Validación de la propuesta

La validación de la propuesta se realizará mediante un **diseño cuasi-experimental** con un **enfoque cuantitativo**, como se describe en el Capítulo 00, sección 6.1.

1.  **Fase de Línea Base:** Los datos del diagnóstico (Capítulo 2) establecerán la línea base de eficiencia utilizando los métodos tradicionales.
2.  **Implementación del MVP:** El producto mínimo viable se implementará en un entorno controlado dentro de Patito SRL.
3.  **Experimentación:** Se seleccionarán equipos ágiles (muestra) y se dividirán en un grupo de control (métodos tradicionales) y un grupo experimental (utilizando el MVP). Se asignarán tareas estandarizadas (historias de usuario).
4.  **Recolección de Datos durante la Experimentación:** Se utilizarán métricas cuantitativas (tiempo por caso, casos por hora, cobertura, variabilidad, tiempo de actualización) y técnicas (observación estructurada, métricas de sistemas) para medir el desempeño de ambos grupos en la generación de casos de prueba para las tareas asignadas (Cuadro 4, Capítulo 2).
5.  **Análisis de Datos:** Se realizará un análisis estadístico comparativo (prueba t de Student, análisis de varianza u otros según la naturaleza de los datos) para determinar si existe una diferencia significativa en la eficiencia entre el grupo experimental y el grupo de control.
6.  **Triangulación y Conclusiones:** Los resultados cuantitativos se complementarán con observaciones cualitativas y feedback de los usuarios para una triangulación completa, permitiendo validar si el MVP logró los objetivos de eficiencia y si es una solución viable y adecuada para el contexto de Patito SRL. Se compararán los resultados obtenidos con los indicadores de la línea base.

Este proceso de validación empírica permitirá comprobar la hipótesis planteada y demostrar, con evidencia objetiva, el impacto del MVP basado en IA en la mejora de la eficiencia del proceso de generación de casos de prueba.

---
UAGRM
SCHOOL OF ENGINEERING
UNIDAD DE POSTGRADO