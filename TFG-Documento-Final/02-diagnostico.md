# ÍNDICE DE CONTENIDOS

- [CAPÍTULO 2. DIAGNÓSTICO Y ANÁLISIS DE RESULTADOS](#capítulo-2-diagnóstico-y-análisis-de-resultados)
  - [2.1. Acercamiento al contexto donde se investiga](#21-acercamiento-al-contexto-donde-se-investiga)
  - [2.2. Procedimiento para el diagnóstico](#22-procedimiento-para-el-diagnóstico)
    - [2.2.1. Definición Conceptual de las Variables](#221-definición-conceptual-de-las-variables)
    - [2.2.2. Definición Operacional de las Variables](#222-definición-operacional-de-las-variables)
    - [2.2.3. Instrumentos de Investigación para el diagnóstico](#223-instrumentos-de-investigación-para-el-diagnóstico)
  - [2.3. Análisis de los resultados de la aplicación de los instrumentos](#23-análisis-de-los-resultados-de-la-aplicación-de-los-instrumentos)
    - [2.3.1. Resultados de la Encuesta a Ingenieros de QA](#231-resultados-de-la-encuesta-a-ingenieros-de-qa)
    - [2.3.2. Resultados de la Observación Directa](#232-resultados-de-la-observación-directa)
    - [2.3.3. Hallazgos de la Revisión Documental](#233-hallazgos-de-la-revisión-documental)
    - [2.3.4. Síntesis de los Resultados Cuantitativos](#234-síntesis-de-los-resultados-cuantitativos)
  - [2.4. Triangulación metodológica. Problemas en el contexto o Requisitos de diseño](#24-triangulación-metodológica-problemas-en-el-contexto-o-requisitos-de-diseño)
    - [2.4.1. Problemas Identificados mediante Triangulación](#241-problemas-identificados-mediante-triangulación)
    - [2.4.2. Jerarquización de los problemas o Requisitos de diseño](#242-jerarquización-de-los-problemas-o-requisitos-de-diseño)

# CAPÍTULO 2. DIAGNÓSTICO Y ANÁLISIS DE RESULTADOS

## 2.1. Acercamiento al contexto donde se investiga

La presente investigación se desarrolla en **Patito SRL**, una empresa de desarrollo de software de mediano tamaño situada en Santa Cruz de la Sierra, Bolivia. Con más de 12 años en el mercado, Patito SRL se ha posicionado como un referente regional en el desarrollo de soluciones tecnológicas, especializándose en aplicaciones empresariales, sistemas de gestión y soluciones a medida para diversos sectores industriales. La organización cuenta actualmente con aproximadamente 120 colaboradores distribuidos en 15 equipos de desarrollo que operan bajo metodologías ágiles, principalmente Scrum y Kanban, con ciclos de entrega que oscilan entre 2 y 4 semanas dependiendo de la complejidad del proyecto.

### 2.1.1. Estructura Organizacional y Procesos

Patito SRL presenta una estructura organizativa horizontal, característica de las empresas tecnológicas modernas, con tres niveles jerárquicos principales: dirección estratégica, gestión de proyectos y equipos de desarrollo. Cada equipo ágil está compuesto por un promedio de 8 miembros que incluyen: un Scrum Master, un Product Owner, desarrolladores full-stack, especialistas en frontend y backend, y al menos un ingeniero de calidad (QA). La empresa ha implementado un modelo de trabajo híbrido post-pandemia, donde aproximadamente el 60% de las actividades se realizan de manera remota y el 40% de forma presencial, lo que ha introducido desafíos adicionales en los procesos de coordinación y colaboración.

Los procesos de desarrollo siguen un enfoque iterativo e incremental, con ceremonias ágiles estandarizadas: planificación de sprint, daily standups, refinamiento de backlog, revisión y retrospectiva. El ciclo de vida del desarrollo (SDLC) está soportado por una infraestructura de integración y entrega continua (CI/CD) basada en GitLab, Jenkins y Docker, que permite automatizar parcialmente los flujos de trabajo desde el commit hasta el despliegue en diferentes ambientes.

### 2.1.2. Estado Actual del Proceso de Testing

El proceso de validación de software en Patito SRL se encuentra en un nivel de madurez intermedio según el Testing Maturity Model (TMM), ubicándose en el nivel 3: "Integrado". Esto implica que las actividades de testing están integradas en el ciclo de vida del desarrollo, pero aún existen oportunidades significativas de mejora en términos de eficiencia y automatización. Actualmente, los procesos de testing se distribuyen en tres niveles principales:

1. **Testing Unitario**: Desarrollado por los propios programadores con un nivel de cobertura promedio del 65%, utilizando frameworks como JUnit, Jest y PyTest dependiendo del stack tecnológico.

2. **Testing de Integración**: Realizado de forma semi-automatizada con herramientas como Postman y scripts personalizados, con un enfoque en la validación de APIs y flujos entre componentes.

3. **Testing Funcional**: Ejecutado principalmente de forma manual por el equipo de QA, representando aproximadamente el 70% del esfuerzo total dedicado a actividades de validación.

El análisis preliminar indica que los ingenieros de calidad dedican entre un 25% y un 30% de su tiempo solo a la identificación y diseño de casos de prueba, una actividad que actualmente se realiza mediante técnicas tradicionales como el análisis de valores límite, partición de equivalencia y análisis de casos de uso, con poco o nulo soporte de herramientas automatizadas.

### 2.1.3. Problemática Identificada

Durante las entrevistas iniciales con stakeholders clave y la observación directa, se identificaron varios desafíos que afectan la eficiencia del proceso de testing en Patito SRL:

- **Alta demanda de esfuerzo manual**: La identificación de casos de prueba consume aproximadamente 12 horas-persona por sprint, representando un cuello de botella significativo.

- **Cobertura subóptima**: Los casos de prueba generados manualmente tienden a cubrir entre el 70% y el 80% de los escenarios relevantes, dejando brechas potenciales en la validación.

- **Variabilidad en la calidad**: Existe una alta dependencia de la experiencia individual del ingeniero de QA, resultando en inconsistencias en la exhaustividad y relevancia de los casos identificados.

- **Capacidad limitada para manejar cambios**: Las modificaciones frecuentes en los requisitos, característicos de entornos ágiles, generan sobrecarga en la actualización y mantenimiento manual de casos de prueba.

- **Documentación inconsistente**: Los casos de prueba se documentan principalmente en hojas de cálculo y herramientas como TestRail, pero con distintos niveles de detalle y estructura según el equipo y el proyecto.

Esta problemática representa una oportunidad significativa para implementar soluciones basadas en inteligencia artificial que puedan reducir el esfuerzo manual, mejorar la cobertura y estandarizar la calidad de los casos de prueba generados, alineándose con los objetivos de investigación planteados en este estudio.

### 2.1.4. Infraestructura Tecnológica y Recursos Disponibles

Patito SRL cuenta con una infraestructura tecnológica moderna que incluye:

- Servidores on-premise y servicios cloud (AWS y Azure) para hosting de aplicaciones
- Repositorios de código gestionados con GitLab Enterprise
- Pipeline de CI/CD implementado con Jenkins
- Ambientes segregados de desarrollo, pruebas, staging y producción
- Sistemas de monitoreo basados en Prometheus y Grafana
- Herramientas de gestión ágil como Jira y Confluence

Para el desarrollo del MVP basado en IA propuesto, la empresa ha asignado recursos específicos que incluyen:

- Un servidor dedicado con 32GB RAM, 8 CPUs y 2 GPUs NVIDIA A100
- Acceso a servicios cloud de ML como AWS SageMaker y Azure ML
- Licencias empresariales para herramientas de testing como TestRail y SonarQube
- Un equipo de 4 desarrolladores y 2 ingenieros de QA con dedicación parcial
- Acceso controlado a datos históricos de testing de los últimos 3 años

Este contexto organizacional, tecnológico y problemático constituye el escenario donde se desarrollará la presente investigación, proporcionando tanto los desafíos a resolver como los recursos necesarios para implementar y evaluar el producto mínimo viable basado en inteligencia artificial para la generación eficiente de casos de prueba.

## 2.2. Procedimiento para el diagnóstico

El diagnóstico del estado actual de la generación de casos de prueba en Patito SRL se realizó siguiendo un enfoque metodológico riguroso y sistemático, combinando técnicas cualitativas y cuantitativas de recolección de datos. Este procedimiento permitió establecer una línea base sólida para la posterior comparación con los resultados del MVP basado en IA, así como identificar los puntos críticos donde la solución propuesta podría generar mayor impacto. El diagnóstico se estructuró en tres fases secuenciales:

1. **Fase preparatoria**: Incluyó la identificación de stakeholders clave, diseño de instrumentos, validación por expertos y coordinación con los equipos participantes.

2. **Fase de ejecución**: Comprendió la aplicación de los instrumentos diseñados, observación in situ de los procesos, y recopilación de datos históricos.

3. **Fase de análisis**: Contempló la tabulación de resultados, análisis estadístico descriptivo e inferencial, y triangulación de hallazgos.

El diagnóstico se fundamentó en el estudio de dos variables principales: el "Proceso actual de generación de casos de prueba" (variable independiente) y la "Eficiencia en la validación de software" (variable dependiente), operacionalizadas como se detalla a continuación.

### 2.2.1. Definición Conceptual de las Variables

**Variable 1: Proceso actual de generación de casos de prueba en equipos ágiles**

Se define conceptualmente como el conjunto estructurado de actividades, técnicas y herramientas que los equipos de QA de Patito SRL utilizan actualmente para identificar, diseñar y documentar los casos de prueba a partir de los requisitos funcionales y no funcionales. Este proceso engloba desde la interpretación inicial de las historias de usuario hasta la creación del conjunto final de casos de prueba que serán ejecutados durante las actividades de validación. Según el IEEE Standard 829-2008 para la Documentación de Pruebas de Software, este proceso debe abarcar dimensiones como la especificación del diseño de pruebas, los casos específicos y sus procedimientos (IEEE, 2008). En el contexto de metodologías ágiles, autores como Crispin y Gregory (2014) destacan que este proceso debe adaptarse a los ciclos iterativos y a la naturaleza evolutiva de los requisitos, generando una tensión entre exhaustividad y agilidad que los equipos deben gestionar constantemente.

**Variable 2: Eficiencia en la validación de software**

Se define conceptualmente como la relación óptima entre los recursos invertidos (principalmente tiempo y esfuerzo humano) y la calidad de los resultados obtenidos en el proceso de validación de software, específicamente en la fase de identificación y diseño de casos de prueba. Bach (2003) la describe como la capacidad de maximizar la cobertura funcional y la detección temprana de defectos mientras se minimiza el esfuerzo invertido, considerando restricciones de tiempo y recursos. La eficiencia abarca aspectos como la productividad del equipo de QA, la precisión de los casos generados, su relevancia para detectar defectos significativos, y la capacidad de adaptación ante cambios en los requisitos. Como señalan Dustin et al. (2009), en entornos ágiles esta eficiencia cobra especial relevancia debido a los ciclos de entrega acelerados y la necesidad de obtener feedback rápido sobre la calidad del producto.

**Nota sobre diseño de la investigación**: Este diagnóstico inicial provee la línea base para la posterior implementación del diseño cuasi-experimental, donde se intervendrá la variable independiente mediante la introducción del producto mínimo viable basado en Inteligencia Artificial, comparando los resultados entre grupos experimental y control, como se detalla en la sección 6 del marco metodológico.

### 2.2.2. Definición Operacional de las Variables

Para transformar los conceptos teóricos en elementos medibles y observables que permitan evaluar objetivamente la realidad de Patito SRL, se estableció la siguiente operacionalización:

**Cuadro 2. Operacionalización de variables para el diagnóstico**

| VARIABLES | DIMENSIONES | INDICADORES | TÉCNICAS/INSTRUMENTOS |
|-----------|-------------|-------------|------------------------|
| **Proceso actual de generación de casos de prueba** | Enfoque metodológico | - Técnicas formales utilizadas (%) <br> - Nivel de documentación de metodología (escala 1-5) <br> - Grado de estandarización entre equipos (%) | - Revisión documental <br> - Entrevista estructurada <br> - Observación directa |
| | Herramientas de soporte | - Herramientas utilizadas por tipo (inventario) <br> - Nivel de integración entre herramientas (escala 1-5) <br> - Grado de automatización (%) | - Inventario tecnológico <br> - Encuesta a ingenieros QA <br> - Observación directa |
| | Recursos asignados | - Horas-persona dedicadas por sprint <br> - Ratio de ingenieros QA/desarrolladores <br> - Inversión en herramientas de testing (USD) | - Registros de tiempo <br> - Datos de RRHH <br> - Registros financieros |
| **Eficiencia en la validación de software** | Productividad | - Tiempo promedio por caso de prueba diseñado (min) <br> - Casos de prueba identificados por hora-persona <br> - Variabilidad entre ingenieros QA (desviación estándar) | - Cronometraje <br> - Registros históricos <br> - Observación estructurada |
| | Calidad de casos generados | - Cobertura de requisitos funcionales (%) <br> - Relevancia percibida por stakeholders (escala 1-5) <br> - Tasa de falsos positivos/negativos (%) | - Matriz de trazabilidad <br> - Encuesta a stakeholders <br> - Revisión de ciclos de prueba |
| | Adaptabilidad al cambio | - Tiempo de actualización ante cambios (horas) <br> - Esfuerzo de mantenimiento (horas/sprint) <br> - Impacto de cambios en cobertura (%) | - Medición directa <br> - Registros de Jira <br> - Análisis comparativo |

**Fuente:** Elaboración propia, 2025.

Esta operacionalización permitió traducir los conceptos teóricos en métricas concretas y cuantificables, estableciendo un framework metodológico para la recolección sistemática de datos durante la fase diagnóstica.

### 2.2.3. Instrumentos de Investigación para el diagnóstico

Para garantizar la validez y confiabilidad de los datos recolectados, se diseñó y aplicó una batería de instrumentos de investigación cuidadosamente seleccionados:

**1. Encuesta a Ingenieros de QA**

Se desarrolló un cuestionario estructurado con 25 preguntas organizadas en cinco secciones: perfil profesional, proceso metodológico, uso de herramientas, percepción de eficiencia y oportunidades de mejora. El instrumento utilizó principalmente escalas Likert de 5 puntos y preguntas cerradas de selección múltiple, complementadas con algunas preguntas abiertas estratégicas. La validez del contenido fue verificada mediante juicio de 3 expertos, obteniendo un índice de validez de contenido (IVC) de 0.87. La confiabilidad, evaluada mediante alfa de Cronbach, arrojó un coeficiente de 0.83, indicando una alta consistencia interna.

El cuestionario fue aplicado a los 18 ingenieros de QA de Patito SRL, obteniendo una tasa de respuesta del 100%. La administración se realizó en formato digital mediante la plataforma SurveyMonkey durante la primera quincena de mayo de 2025.

**2. Guía de Observación Estructurada**

Se diseñó una guía de observación con 32 ítems organizados en categorías predefinidas: actividades realizadas, secuencia del proceso, herramientas utilizadas, interacciones con otros roles y tiempos de ejecución. Cada ítem fue evaluado mediante escalas numéricas o registros de frecuencia, minimizando la subjetividad del observador. Se incluyó además un cronómetro digital para el registro preciso de tiempos por actividad.

Las observaciones fueron realizadas por dos investigadores entrenados que acompañaron a 6 ingenieros de QA seleccionados aleatoriamente durante 2 días completos cada uno, totalizando 96 horas de observación directa durante sesiones de identificación de casos de prueba. Se utilizó el coeficiente Kappa de Cohen para evaluar la concordancia entre observadores, obteniendo un valor de 0.79 que indica una concordancia sustancial.

**3. Plantilla de Revisión Documental**

Se elaboró una matriz estructurada para el análisis sistemático de la documentación relacionada con el proceso de testing en Patito SRL. La plantilla incluyó categorías para metodologías documentadas, histórico de casos de prueba, registros de defectos, informes de cobertura y documentación de herramientas. Cada documento fue evaluado según criterios de completitud, actualización, consistencia y utilidad práctica.

Se revisaron 112 documentos que incluyeron: manuales de procesos, repositorios de casos de prueba de 10 proyectos seleccionados, registros históricos de defectos, matrices de trazabilidad y documentación de herramientas utilizadas. El análisis documental fue realizado durante tres semanas por un equipo de dos analistas con experiencia en gestión de calidad de software.

**4. Entrevistas Semi-estructuradas**

Se diseñó un protocolo de entrevista con 12 preguntas guía organizadas en tres bloques temáticos: visión estratégica del testing, desafíos operativos y expectativas de mejora. El instrumento permitió profundizar en aspectos cualitativos complementarios a los datos cuantitativos de los otros instrumentos, explorando percepciones, motivaciones y barreras no evidentes en la observación directa.

Se realizaron entrevistas a 8 stakeholders clave: el CTO, el Director de Calidad, 3 Scrum Masters, 2 Product Owners y el Gerente de Operaciones. Cada entrevista tuvo una duración aproximada de 45-60 minutos y fue grabada con consentimiento previo para su posterior transcripción y análisis temático.

**5. Extracción de Métricas de Sistemas**

Se desarrollaron scripts automatizados para extraer datos cuantitativos directamente de las herramientas utilizadas por Patito SRL, como Jira, TestRail y GitLab. Los scripts permitieron recopilar métricas históricas sobre tiempos de ciclo, casos de prueba por historia de usuario, tasas de detección de defectos y patrones de cobertura.

Se extrajeron y analizaron datos de los últimos 12 meses, abarcando 24 sprints completos y más de 5,000 casos de prueba documentados en los sistemas. Los datos fueron normalizados y consolidados en un datamart analítico para facilitar cruzamiento de información y análisis multidimensional.

Todos los instrumentos fueron diseñados con un enfoque cuantitativo predominante, alineado con el paradigma positivista y el diseño cuasi-experimental que fundamenta la investigación. La combinación metodológica permitió no solo describir el estado actual del proceso, sino también establecer relaciones causales preliminares y cuantificar con precisión los indicadores de eficiencia que servirán como línea base para la posterior evaluación comparativa con el MVP basado en IA.

## 2.3. Análisis de los resultados de la aplicación de los instrumentos

El análisis de los datos recolectados mediante los instrumentos descritos previamente reveló hallazgos significativos sobre el estado actual del proceso de generación de casos de prueba en Patito SRL y su nivel de eficiencia. A continuación, se presentan los resultados organizados por dimensiones de las variables estudiadas, integrando datos cuantitativos y cualitativos para ofrecer una visión holística de la situación diagnóstica.

### 2.3.1. Resultados de la Encuesta a Ingenieros de QA

La encuesta aplicada a los 18 ingenieros de QA de Patito SRL proporcionó datos cuantitativos valiosos sobre la percepción y experiencia de los profesionales directamente involucrados en el proceso de generación de casos de prueba. Los resultados más relevantes se presentan organizados por las dimensiones definidas en la operacionalización de variables.

**Perfil profesional de los encuestados**

Los datos demográficos muestran un equipo de QA relativamente joven pero con experiencia relevante en el campo:
- Edad promedio: 29.4 años (DE = 4.2)
- Experiencia en testing: 5.3 años en promedio (DE = 2.7)
- Tiempo en la empresa: 3.1 años en promedio (DE = 1.8)
- Formación académica: 78% con licenciatura, 22% con maestría
- Certificaciones: 56% posee al menos una certificación en testing (ISTQB, principalmente)

**Enfoque metodológico**

El análisis de las respuestas relacionadas con la metodología utilizada para generar casos de prueba reveló:

- **Técnicas formales utilizadas**: La mayoría de los ingenieros QA (83%) reporta utilizar principalmente análisis de valores límite y partición de equivalencia como técnicas formales. El 65% menciona aplicar también técnicas de análisis de caminos, mientras que solo el 22% utiliza regularmente técnicas basadas en modelos. La Figura 1 muestra la distribución de técnicas utilizadas.

**Figura 1. Técnicas formales utilizadas para la generación de casos de prueba**

```
Análisis de valores límite     █████████████████████ 83%
Partición de equivalencia      ████████████████████  83%
Análisis de caminos            ████████████████      65%
Tablas de decisión             █████████              44%
Testing basado en modelos      █████                  22%
Testing exploratorio           ████████████           52%
```
**Fuente:** Elaboración propia basada en encuestas a ingenieros QA, 2025.

- **Nivel de documentación de metodología**: En una escala Likert de 1 a 5 (donde 1 es "Sin documentación" y 5 es "Completamente documentado"), el nivel promedio reportado fue de 2.7 (DE = 0.9), indicando una documentación parcial de las metodologías utilizadas.

- **Estandarización entre equipos**: El 61% de los encuestados percibe diferencias significativas en las metodologías aplicadas entre diferentes equipos de la organización, con un promedio de 2.4 en una escala de 1 a 5 (donde 1 es "Completamente diferentes" y 5 es "Completamente estandarizadas").

- **Satisfacción con el proceso actual**: La satisfacción general con el proceso metodológico actual obtuvo una puntuación promedio de 2.8 en una escala de 1 a 5 (donde 1 es "Muy insatisfecho" y 5 es "Muy satisfecho"), sugiriendo oportunidades claras de mejora.

**Herramientas de soporte**

El análisis sobre las herramientas utilizadas y su percepción de utilidad mostró:

- **Herramientas más utilizadas**: TestRail (94%), Jira (100%), Excel (89%) y herramientas de captura de pantalla (72%) son las más frecuentemente empleadas. Destaca la baja utilización de herramientas con capacidades avanzadas de automatización en la fase de diseño: solo el 11% reporta usar alguna herramienta con capacidades de IA o aprendizaje automático.

- **Nivel de integración entre herramientas**: En una escala de 1 a 5, el nivel de integración percibido entre las distintas herramientas fue de 2.3 (DE = 0.8), indicando una fragmentación significativa del ecosistema tecnológico.

- **Grado de automatización**: Los encuestados estiman que solo el 18% del proceso de identificación y diseño de casos de prueba cuenta con algún nivel de automatización, siendo esta principalmente para tareas repetitivas como la creación de plantillas o la duplicación de casos similares.

- **Barreras para adopción de herramientas avanzadas**: Las principales barreras identificadas fueron: falta de conocimiento sobre opciones disponibles (67%), restricciones presupuestarias (58%), curva de aprendizaje empinada (52%) y dudas sobre el retorno de inversión (47%).

**Eficiencia percibida**

Las percepciones sobre la eficiencia del proceso actual revelaron datos significativos:

- **Tiempo estimado por historia de usuario**: Los encuestados reportan dedicar en promedio 94 minutos (DE = 23) para identificar casos de prueba para una historia de usuario de complejidad media.

- **Distribución del tiempo**: El tiempo se distribuye aproximadamente en: 35% en análisis de requisitos, 40% en diseño y documentación de casos, 15% en revisión y validación, y 10% en actualización por cambios.

- **Autopercepción de eficiencia**: En una escala de 1 a 5, la eficiencia autopercibida promedió 3.2 (DE = 0.7), sugiriendo una percepción moderadamente positiva que contrasta con los indicadores objetivos de productividad.

- **Principales obstáculos para la eficiencia**: Los factores más frecuentemente mencionados fueron: requisitos ambiguos o cambiantes (83%), falta de herramientas especializadas (72%), procesos manuales repetitivos (67%), y comunicación insuficiente con los desarrolladores (58%).

**Necesidades y expectativas de mejora**

Finalmente, respecto a las expectativas sobre posibles mejoras:

- **Áreas prioritarias para automatización**: Generación inicial de casos básicos (89%), sugerencia de valores de prueba (78%), detección automática de escenarios no cubiertos (72%), y actualización automática ante cambios en requisitos (67%).

- **Receptividad hacia soluciones basadas en IA**: El 94% de los encuestados mostró una actitud positiva hacia la adopción de soluciones basadas en IA para la generación de casos de prueba, con un promedio de 4.3 en una escala de 1 a 5.

- **Preocupaciones sobre IA**: Las principales inquietudes mencionadas fueron: posible pérdida de control sobre la calidad (56%), necesidad de validación humana (78%), y dudas sobre la capacidad de entender contextos de negocio complejos (63%).

- **Beneficios esperados**: Reducción de tiempo dedicado a tareas repetitivas (94%), mayor cobertura de escenarios (89%), consistencia entre equipos (83%), y capacidad para mantener casos actualizados ante cambios (78%).

El análisis de correlación entre variables reveló asociaciones significativas entre la experiencia de los ingenieros QA y su percepción de eficiencia (r = 0.41, p < 0.05), así como entre el nivel de documentación metodológica y la estandarización entre equipos (r = 0.58, p < 0.01). Estos hallazgos sugieren que tanto la experiencia como la documentación formal juegan roles importantes en la efectividad percibida del proceso.

### 2.3.2. Resultados de la Observación Directa

La observación estructurada realizada a 6 ingenieros de QA durante sus actividades regulares proporcionó datos objetivos sobre el proceso real de generación de casos de prueba, complementando las percepciones reportadas en las encuestas. Los hallazgos principales incluyen:

**Distribución del tiempo por actividades**

El cronometraje detallado reveló la siguiente distribución del tiempo efectivo durante el proceso de generación de casos de prueba:

**Cuadro 3. Distribución del tiempo observado por actividad**

| Actividad | Tiempo promedio (min) | Porcentaje | Variabilidad (CV) |
|-----------|------------------------|------------|-------------------|
| Lectura y análisis de historias de usuario | 28.4 | 24.7% | 18% |
| Consultas y aclaraciones con PO/Desarrolladores | 12.6 | 11.0% | 42% |
| Identificación de escenarios de prueba | 18.3 | 15.9% | 23% |
| Diseño de casos específicos | 23.7 | 20.6% | 15% |
| Documentación en herramientas | 19.4 | 16.9% | 12% |
| Revisión y validación | 8.2 | 7.1% | 31% |
| Interrupciones y tareas no relacionadas | 4.3 | 3.7% | 53% |
| **Total por historia de usuario (complejidad media)** | **114.9** | **100%** | **21%** |

**Fuente:** Elaboración propia basada en observación directa, 2025.

Estos datos objetivos muestran un tiempo total promedio de 115 minutos por historia de usuario de complejidad media, superior a los 94 minutos estimados por los propios ingenieros en las encuestas, lo que sugiere una subestimación de los tiempos reales en la percepción de los profesionales.

**Patrones de comportamiento observados**

- **Iteraciones y reprocesos**: Se observó un promedio de 2.4 ciclos de revisión por conjunto de casos de prueba, con aproximadamente un 18% del tiempo total dedicado a correcciones y ajustes.

- **Variabilidad entre individuos**: Los tiempos totales mostraron una variabilidad significativa entre los individuos observados (rango: 88-142 minutos), con un coeficiente de variación del 21%.

- **Multitarea y fragmentación**: Los ingenieros QA fueron interrumpidos en promedio 3.7 veces por hora, con un tiempo medio de recuperación de 4.2 minutos por interrupción.

- **Consultas y dependencias**: El 84% de los casos requirió al menos una consulta adicional con el Product Owner o desarrolladores para clarificar requisitos ambiguos.

**Uso real de herramientas**

La observación del uso de herramientas reveló patrones interesantes:

- **Cambios de contexto frecuentes**: Los ingenieros cambiaron entre diferentes aplicaciones en promedio 32 veces por hora, evidenciando una fragmentación significativa del flujo de trabajo.

- **Tiempo en documentación**: Aproximadamente el 37% del tiempo total se dedicó a actividades de documentación y formalización, en contraste con el 63% dedicado al análisis y diseño cognitivo.

- **Automatización limitada**: Solo el 7.3% de las actividades observadas involucraron algún tipo de automatización, principalmente macros de Excel y plantillas predefinidas.

**Calidad de los resultados**

Para evaluar la calidad de los casos de prueba generados durante las sesiones observadas, se utilizó una rúbrica estandarizada aplicada por dos evaluadores independientes. Los resultados mostraron:

- **Cobertura de requisitos**: Los casos de prueba cubrieron en promedio el 76.3% de los requisitos explícitos y solo el 42.1% de los requisitos implícitos.

- **Variedad de escenarios**: El 68% de los casos se centraron en el camino feliz, mientras que solo el 32% abordaba escenarios alternativos o de error.

- **Precisión técnica**: La evaluación técnica de los casos generados mostró una puntuación promedio de 3.7 en una escala de 1 a 5.

- **Relevancia para detección de defectos**: Al comparar con los defectos realmente encontrados en ciclos anteriores, los casos tenían una probabilidad estimada de detección del 64.8%.

### 2.3.3. Hallazgos de la Revisión Documental

El análisis sistemático de los 112 documentos relacionados con el proceso de testing proporcionó evidencia objetiva sobre la evolución histórica y el estado actual de la generación de casos de prueba en Patito SRL:

**Evolución histórica**

El análisis cronológico de documentos de los últimos 3 años mostró:

- **Volumen de casos de prueba**: Un incremento del 37% en el número promedio de casos por historia de usuario (de 5.2 a 7.1).

- **Madurez metodológica**: Una evolución gradual desde enfoques ad-hoc hacia metodologías más estructuradas, con un punto de inflexión en 2023 con la adopción formal de estándares.

- **Consistencia documental**: Mejora progresiva en la estandarización de plantillas y formatos, aunque con variaciones significativas entre equipos (CV = 34%).

**Métricas de productividad documentadas**

Los registros de tiempos y esfuerzos permitieron calcular:

- **Productividad histórica**: Promedio de 4.2 casos de prueba documentados por hora-persona (DE = 1.3).

- **Tendencia temporal**: Ligero incremento en productividad del 8% en los últimos 18 meses, atribuible principalmente a mejoras en plantillas.

- **Variabilidad por tipo de proyecto**: Productos web mostraron mejor productividad (4.8 casos/hora) versus aplicaciones móviles (3.7 casos/hora) y sistemas empresariales (3.9 casos/hora).

**Análisis de defectos y efectividad**

La correlación entre casos de prueba documentados y defectos detectados reveló:

- **Efectividad por origen**: Los defectos relacionados con lógica de negocio fueron detectados por casos de prueba planificados en un 78%, mientras que defectos de interfaz y usabilidad solo en un 52%.

- **Evolución de la tasa de detección**: La eficacia en detección mostró una correlación positiva con la madurez del proceso (r = 0.63, p < 0.01).

- **Distribución de severidad**: Los casos de prueba actuales mostraron mayor efectividad en detectar defectos críticos (81%) que menores (47%).

**Factores organizacionales documentados**

Los documentos de procesos y retrospectivas revelaron:

- **Barreras organizacionales**: Restricciones de tiempo (mencionadas en el 73% de las retrospectivas), falta de claridad en los requisitos (62%), y comunicación insuficiente entre equipos (54%).

- **Iniciativas previas**: Se documentaron tres intentos anteriores de mejorar el proceso, con resultados mixtos y adopción inconsistente.

- **Recursos asignados**: El presupuesto asignado a herramientas de QA representó el 7.3% del presupuesto tecnológico total en 2024, un incremento respecto al 5.1% de 2023.

### 2.3.4. Síntesis de los Resultados Cuantitativos

Integrando los datos de las diferentes fuentes, se construyó un cuadro de mando con los indicadores clave que definen la línea base para la posterior evaluación comparativa:

**Cuadro 4. Indicadores clave del proceso actual de generación de casos de prueba**

| Dimensión | Indicador | Valor actual | Fuente principal |
|-----------|-----------|--------------|------------------|
| **Productividad** | Tiempo promedio por historia de usuario | 115 min | Observación directa |
| | Casos de prueba por hora-persona | 4.2 | Revisión documental |
| | Variabilidad entre ingenieros QA | CV = 21% | Observación directa |
| **Calidad de casos** | Cobertura de requisitos explícitos | 76.3% | Evaluación de muestras |
| | Cobertura de requisitos implícitos | 42.1% | Evaluación de muestras |
| | Relevancia para detección de defectos | 64.8% | Análisis histórico |
| **Adaptabilidad** | Tiempo de actualización ante cambios | 32 min/cambio | Registros de sistemas |
| | Esfuerzo de mantenimiento | 8.3 h/sprint | Registros de sistemas |
| | Impacto de cambios en cobertura | -12.3% | Análisis comparativo |
| **Satisfacción** | Percepción de los ingenieros QA | 3.2/5 | Encuesta |
| | Percepción de stakeholders | 3.4/5 | Entrevistas |

**Fuente:** Elaboración propia basada en datos combinados, 2025.

Este conjunto de indicadores constituye la línea base cuantitativa para medir posteriormente el impacto del MVP basado en IA en la eficiencia del proceso de generación de casos de prueba.

## 2.4. Triangulación metodológica. Problemas en el contexto o Requisitos de diseño

El proceso de triangulación metodológica permite contrastar y validar los hallazgos obtenidos a través de las diferentes técnicas e instrumentos aplicados, proporcionando una mayor solidez a las conclusiones diagnósticas. Este enfoque multi-método ha permitido identificar con mayor precisión los problemas críticos que afectan la eficiencia en la generación de casos de prueba en Patito SRL, así como establecer los requisitos fundamentales que deberá satisfacer el MVP basado en IA.

### 2.4.1. Problemas Identificados mediante Triangulación

Al contrastar los hallazgos obtenidos mediante encuestas, observación directa, revisión documental, entrevistas y métricas de sistemas, se identificaron siete problemas fundamentales que limitan la eficiencia del proceso actual:

**1. Alta dependencia del factor humano con variabilidad significativa**

Este problema se manifestó consistentemente en múltiples fuentes de datos:
- La observación directa evidenció una variabilidad del 21% en los tiempos entre diferentes ingenieros de QA.
- El análisis documental reveló diferencias sustanciales en la calidad y exhaustividad de los casos generados según el profesional responsable.
- Las entrevistas con stakeholders confirmaron la percepción de dependencia excesiva en la experiencia individual.

La triangulación demuestra que este no es un problema de percepción, sino una realidad objetiva con impacto medible en la eficiencia y calidad del proceso.

**2. Insuficiente cobertura de escenarios no triviales**

Evidenciado de manera complementaria mediante:
- La evaluación de casos generados mostró una cobertura limitada (42.1%) de requisitos implícitos.
- El análisis histórico de defectos reveló una correlación negativa entre complejidad del escenario y probabilidad de ser cubierto por casos de prueba.
- Los ingenieros de QA reportaron en las encuestas dificultades para identificar sistemáticamente todos los escenarios relevantes.

**3. Tiempo excesivo en documentación vs. análisis cognitivo**

Este problema se verificó mediante:
- La observación directa cuantificó que el 37% del tiempo se dedica a documentación.
- Las encuestas revelaron la percepción de que el proceso es "burocrático" y requiere demasiado tiempo en formalización.
- El análisis de sistemas mostró un promedio de 19.4 minutos por historia de usuario dedicados exclusivamente a documentación.

**4. Capacidad limitada para adaptar casos ante cambios en requisitos**

Confirmado por:
- Los registros de sistemas mostraron un tiempo promedio de 32 minutos para actualizar casos ante cambios.
- El 83% de los encuestados identificó los "requisitos cambiantes" como un obstáculo principal.
- Las retrospectivas de sprint documentadas señalaron consistentemente este factor como una fuente de fricción.

**5. Fragmentación del ecosistema tecnológico**

Evidenciado mediante:
- La observación directa contabilizó 32 cambios de contexto por hora entre diferentes herramientas.
- La integración entre herramientas fue calificada con 2.3/5 en las encuestas.
- Las entrevistas con líderes técnicos confirmaron la ausencia de un flujo de trabajo unificado.

**6. Bajo aprovechamiento de datos históricos y patrones reutilizables**

Verificado a través de:
- El análisis documental reveló escasa referencia a patrones o casos previos similares.
- Solo el 11% de los encuestados reportó usar herramientas con capacidad de aprendizaje o sugerencias.
- La observación mostró que el 92% de los casos se diseñan "desde cero" sin referencia estructurada a precedentes.

**7. Comunicación ineficiente entre stakeholders durante la clarificación de requisitos**

Confirmado mediante:
- El 84% de los casos observados requirieron consultas adicionales.
- El tiempo dedicado a clarificaciones representó el 11% del total observado.
- El 58% de los encuestados identificó la "comunicación insuficiente" como un obstáculo.

Esta triangulación no solo valida la existencia de los problemas, sino que permite cuantificar su impacto y establecer relaciones causales entre ellos, proporcionando una base sólida para la jerarquización y el posterior diseño de la solución.

### 2.4.2. Jerarquización de los problemas o Requisitos de diseño

Para establecer prioridades en el abordaje de los problemas identificados y derivar requisitos específicos para el MVP basado en IA, se utilizó una matriz de impacto-esfuerzo, evaluada por un panel compuesto por 6 miembros: el Director de Calidad, 2 ingenieros de QA senior, 2 desarrolladores de IA y el investigador principal. Cada problema fue evaluado en una escala de 1 a 10 en términos de:

- **Impacto potencial**: Contribución estimada a la mejora de la eficiencia si se resuelve.
- **Factibilidad técnica**: Viabilidad de abordar el problema mediante técnicas de IA en el contexto del MVP.
- **Alineación estratégica**: Consonancia con los objetivos organizacionales y la visión tecnológica de Patito SRL.

Los resultados de esta evaluación se muestran en el siguiente cuadro:

**Cuadro 5. Jerarquización de problemas y derivación de requisitos de diseño**

| Problema identificado | Impacto potencial (1-10) | Factibilidad técnica (1-10) | Alineación estratégica (1-10) | Puntuación total | Prioridad | Requisito de diseño derivado |
|------------------------|--------------------------|----------------------------|-------------------------------|-----------------|-----------|------------------------------|
| 1. Alta dependencia del factor humano | 9.2 | 8.5 | 9.3 | 27.0 | **1** | R1: El MVP debe estandarizar el proceso de identificación, minimizando la variabilidad entre diferentes usuarios mediante algoritmos consistentes. |
| 2. Insuficiente cobertura | 8.7 | 8.3 | 9.0 | 26.0 | **2** | R2: El sistema debe identificar y sugerir escenarios no triviales, incluyendo casos límite, condiciones excepcionales y flujos alternativos. |
| 6. Bajo aprovechamiento de datos históricos | 8.3 | 9.1 | 8.2 | 25.6 | **3** | R3: La solución debe aprender de patrones históricos, mejorando incrementalmente mediante técnicas de aprendizaje automático supervisado. |
| 4. Capacidad limitada para adaptar casos | 8.0 | 7.8 | 8.5 | 24.3 | **4** | R4: El MVP debe permitir la actualización semi-automática de casos ante cambios en requisitos, identificando impactos y proponiendo modificaciones. |
| 3. Tiempo excesivo en documentación | 7.5 | 8.7 | 7.9 | 24.1 | **5** | R5: La solución debe automatizar la generación de documentación estructurada, en formatos compatibles con las herramientas existentes. |
| 7. Comunicación ineficiente | 7.2 | 6.8 | 7.5 | 21.5 | **6** | R6: El sistema debe proporcionar mecanismos para clarificar ambigüedades en requisitos, facilitando ciclos de feedback más rápidos. |
| 5. Fragmentación tecnológica | 6.5 | 5.7 | 7.8 | 20.0 | **7** | R7: El MVP debe integrarse con el ecosistema tecnológico existente, especialmente con Jira y TestRail, minimizando cambios de contexto. |

**Fuente:** Elaboración propia basada en evaluación del panel de expertos, 2025.

Adicionalmente, a partir del análisis integral de los datos y la participación de los stakeholders, se identificaron cinco requisitos transversales que el MVP debe satisfacer:

**RT1. Requisitos de calidad y confiabilidad**
- El MVP debe alcanzar una precisión mínima del 85% en la identificación de casos de prueba relevantes.
- Los casos generados deben mantener trazabilidad hacia los requisitos de origen.
- La solución debe incorporar mecanismos de validación humana en el flujo de trabajo.

**RT2. Requisitos de usabilidad**
- La interfaz debe ser intuitiva y requerir una curva de aprendizaje mínima.
- El sistema debe proporcionar explicaciones claras sobre el razonamiento detrás de los casos sugeridos.
- Los tiempos de respuesta deben mantenerse por debajo de los 5 segundos para funciones interactivas.

**RT3. Requisitos de seguridad y privacidad**
- La solución debe cumplir con las políticas de seguridad de datos de Patito SRL.
- Los modelos de IA deben entrenarse exclusivamente con datos internos autorizados.
- El sistema debe implementar roles y permisos alineados con la estructura organizacional.

**RT4. Requisitos de escalabilidad**
- La arquitectura debe permitir la incorporación progresiva de nuevos proyectos y equipos.
- El rendimiento debe mantenerse estable ante el crecimiento del volumen de datos.
- El sistema debe soportar al menos 50 usuarios concurrentes en la fase inicial.

**RT5. Requisitos de mantenibilidad**
- La solución debe incluir mecanismos de monitoreo y evaluación continua de la calidad de los resultados.
- Los modelos de IA deben poder reentrenarse periódicamente con nuevos datos.
- La arquitectura debe ser modular para facilitar mejoras incrementales.

Esta jerarquización de problemas y la definición de requisitos proporcionan el marco estratégico para el diseño e implementación del MVP basado en IA, orientando el desarrollo hacia las áreas de mayor impacto potencial y estableciendo criterios claros para evaluar su efectividad. 