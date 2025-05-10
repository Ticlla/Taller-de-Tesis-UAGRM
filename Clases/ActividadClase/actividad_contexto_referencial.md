## 1. Procedimiento paso a paso para el análisis de datos  
*(enfoque cuantitativo – diseño cuasi-experimental con grupo control y grupo experimental para evaluación de solución IA en generación de casos de prueba)*  

| **Etapa** | **Paso** | **Acción concreta** | **Resultado esperado** |
|-----------|---------|---------------------|------------------------|
| **Preparación** | 1 | Consolidar los datos de ambos grupos (control usando técnicas tradicionales y experimental usando IA) incluyendo métricas de tiempo, cobertura de pruebas, defectos detectados y satisfacción del usuario. | Base de datos unificada con todas las métricas. |
| | 2 | Verificar integridad: identificar valores atípicos o faltantes y documentar su tratamiento (exclusión o imputación). | Dataset limpio y trazable. |
| **Codificación** | 3 | Codificar variables cualitativas (rol en equipo ágil, experiencia previa, tipo de proyecto) y normalizar métricas numéricas (tiempo en minutos, cobertura en %). | Variables listas para análisis estadístico. |
| **Descriptivos** | 4 | Calcular estadísticas descriptivas (media, mediana, desviación estándar) para las métricas clave: Porcentaje de Detección de Defectos (DDP), tiempo de generación de casos, Tasa de Efectividad de Casos (TCE) y cobertura alcanzada. | Panorama general de diferencias entre grupos. |
| **Supuestos** | 5 | Ejecutar pruebas de normalidad (Shapiro-Wilk) y homogeneidad de varianzas (Levene) para cada métrica. | Determinación sobre uso de tests paramétricos o no paramétricos. |
| **Comparaciones** | 6 | *Si cumple supuestos* → t-Student para comparar grupos y t pareada para cambios pre/post.<br>*Si no* → Mann-Whitney U y Wilcoxon signed-rank. | Evaluación estadística de la hipótesis principal sobre eficiencia y efectividad de la solución IA. |
| **Tamaño de efecto** | 7 | Calcular d de Cohen (si paramétrico) o r de Rosenthal (si no paramétrico) para cuantificar la magnitud de la mejora. | Medida de la relevancia práctica del sistema de IA. |
| **Visualización** | 8 | Crear gráficos comparativos: diagramas de caja para tiempos de generación, gráficos de barras para cobertura y detectabilidad de defectos. | Representación visual del impacto de la solución. |
| **Inferencia adicional** | 9 | Analizar correlaciones entre: tiempo-cobertura, experiencia-rendimiento, y complejidad del proyecto-eficacia de la IA. | Comprensión profunda de factores que influyen en el rendimiento. |
| **Validación & reporte** | 10 | Triangular resultados cuantitativos con retroalimentación cualitativa de usuarios y documentar limitaciones del estudio. | Capítulo de análisis de datos completo y equilibrado. |

---

## 2. Tabla cronológica de autores, aportes y relación con la investigación  

| **Año** | **Autor(es)** | **Aporte clave al tema** | **Conexión con tu investigación** |
|---------|--------------|--------------------------|-----------------------------------|
| 1979 | Glenford Myers | Estableció principios formales de testing y planificación sistemática de casos de prueba. | Base teórica fundamental que sigue vigente incluso en soluciones automatizadas. |
| 2001 | Beck et al. | Manifiesto Ágil: integración de pruebas continuas en ciclos de desarrollo. | Marco metodológico del entorno ágil donde se implementará la solución de IA. |
| 2004 | Harman & Clark | Iniciaron Search-Based Software Testing con algoritmos evolutivos. | Precursor directo de usar IA para generación automática de pruebas. |
| 2007 | Li, Harman & Hierons | Aplicación de búsqueda basada en IA a BD relacionales con mejora de cobertura/tiempo. | Evidencia temprana del potencial de IA en testing, base comparativa. |
| 2019 | Wagner | Métricas de efectividad en testing (DDP, TCE) y automatización. | Framework para evaluar cuantitativamente el impacto de la solución. |
| 2021 | Nair et al. | Generación automática de casos límite en sistemas críticos con ML. | Técnicas aplicables a la detección de bordes y valores extremos. |
| 2021 | Functionize | Documentación sobre costo de corrección de defectos según etapa. | Justificación económica para detección temprana mediante IA. |
| 2021 | Infoworld | Métricas de eficiencia en contextos ágiles (velocidad, lead time). | Indicadores específicos para medir impacto en equipos ágiles. |
| 2023 | LambdaTest | Tendencias en automatización: codeless testing, QAOps, IA en testing. | Contexto actual donde se inserta la propuesta de MVP. |
| 2023 | Babar et al. | NLP para extraer casos de prueba en banca, logrando 47% menos esfuerzo. | Caso de referencia en sector empresarial con beneficios cuantificados. |
| 2024 | Baqar & Khanda | Futuro del testing impulsado por IA y validación automática. | Prospectiva que valida la dirección de la investigación propuesta. |
| 2024 | Ramadan et al. | Estado del arte de ML en testing: métricas de eficiencia y desafíos. | Guía metodológica para diseño experimental e indicadores relevantes. |

---

## 3. Marco organizacional de **Patito SRL**

| **Aspecto** | **Síntesis** |
|-------------|--------------|
| **Misión** | Desarrollar y entregar soluciones de software de alta calidad mediante la integración de prácticas ágiles, automatización inteligente y procesos optimizados que generen valor inmediato y sostenible para nuestros clientes. |
| **Visión** | Convertirnos en la empresa boliviana referente en ingeniería de software ágil e inteligencia artificial aplicada a calidad, reconocida por transformar la eficiencia de los procesos de testing y acelerar la entrega de productos confiables. |
| **Elementos culturales que influyen en la investigación** | - **Orientación a resultados medibles** (facilita evaluación objetiva del MVP).<br>- **Cultura DevOps integrada** (propicia la adopción de automatización en testing).<br>- **Mejora continua como principio** (favorece experimentación con nuevas tecnologías).<br>- **Trabajo en células ágiles autónomas** (entorno ideal para implementar y validar soluciones).<br>- **Valoración del tiempo como recurso crítico** (alineado con el objetivo de reducir esfuerzo en generación de casos).<br>- **Aprendizaje organizacional** (disposición para capacitarse en nuevas herramientas de IA). |

---

