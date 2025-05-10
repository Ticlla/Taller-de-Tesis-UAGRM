## 1. Procedimiento paso a paso para el análisis de datos  
*(enfoque cuantitativo – diseño cuasi-experimental con grupo control y grupo experimental)*  

| **Etapa** | **Paso** | **Acción concreta** | **Resultado esperado** |
|-----------|---------|---------------------|------------------------|
| **Preparación** | 1 | Consolidar en una sola hoja de cálculo los datos crudos (cuestionarios pre/post, tiempos, coberturas, etc.) procedentes de ambos grupos. | Base de datos única, sin duplicados. |
| | 2 | Verificar integridad: detectar valores faltantes o atípicos y documentar su tratamiento (exclusión o imputación). | Conjunto limpio y trazable. |
| **Codificación** | 3 | Codificar variables cualitativas (p. ej. rol, proyecto) y normalizar escalas numéricas (tiempo en min, cobertura %). | Dataset listo para análisis estadístico. |
| **Descriptivos** | 4 | Calcular media, mediana, DE y rangos para cada indicador en pre-test y post-test de ambos grupos. | Visión global de tendencias y dispersión. |
| **Supuestos** | 5 | Pruebas de normalidad (Shapiro-Wilk) y homogeneidad de varianzas (Levene). | Decisión sobre pruebas paramétricas o no-paramétricas. |
| **Comparaciones** | 6 | *Si se cumplen supuestos* → **t-Student** (independientes) y **t pareada** (dentro de grupo).<br>*Si no* → **Mann-Whitney U** y **Wilcoxon**. | Contraste de la hipótesis principal. |
| **Tamaño de efecto** | 7 | Calcular **Cohen _d_** (paramétrico) o **_r_ de Rosenthal** (no-paramétrico). | Evidencia de relevancia práctica. |
| **Visualización** | 8 | Diagramas de caja y gráficos de barras (pre/post × grupo). | Resultados fáciles de comunicar. |
| **Inferencia adicional** | 9 | Correlaciones entre variables (p. ej. tiempo ↔ cobertura) y regresión simple para predicción. | Comprensión profunda de relaciones internas. |
| **Validación & reporte** | 10 | Revisar fiabilidad (α de Cronbach), triangulación con datos cualitativos y redactar conclusiones. | Informe listo para el capítulo “Análisis de datos”. |

---

## 2. Tabla cronológica de autores, aportes y relación con la investigación  

| **Año** | **Autor(es)** | **Aporte clave al tema** | **Conexión con tu investigación** |
|---------|--------------|--------------------------|-----------------------------------|
| 1979 | Glenford Myers | Principios formales de *software testing*; planificación sistemática. | Base histórica de calidad sobre la que se construyen técnicas modernas. |
| 1998 | Elaine Weyuker | Complejidad de diseñar casos de prueba y necesidad de automatización. | Justifica la búsqueda de soluciones basadas en IA. |
| 2001 | Kent Beck et al. | Manifiesto Ágil: pruebas continuas y responsabilidad compartida. | Marco metodológico de los equipos ágiles del estudio. |
| 2004 | Harman & Clark | Inician *Search-Based Software Testing* con algoritmos evolutivos. | Precedente directo de IA para generar pruebas. |
| 2007 | Li, Harman & Hierons | Aplicación de búsqueda basada en IA a BD relacionales; mejora cobertura/tiempo. | Evidencia empírica que tu MVP busca replicar. |
| 2021 | Nair et al. | Generación automática de casos límite en sistemas críticos mediante ML. | Valida técnicas ML en contextos de riesgo. |
| 2023 | Khan & Ali | Framework **TestLab**: generación-ejecución-análisis de pruebas con IA. | Referencia para la arquitectura de tu MVP. |
| 2023 | Babar et al. | NLP para extraer casos de prueba en banca; 47 % menos esfuerzo. | Beneficios concretos en dominio corporativo. |
| 2024 | Baqar & Khanda | Futuro del testing impulsado por IA y validación automática. | Sustento teórico de la hipótesis principal. |
| 2024 | Ramadan et al. | Estado del arte ML en testing: métricas de eficiencia y desafíos. | Guía para seleccionar indicadores de éxito. |

---

## 3. Marco organizacional de **Patito SRL**

| **Aspecto** | **Síntesis** |
|-------------|--------------|
| **Misión** | Desarrollar y entregar soluciones de software de alta calidad que generen valor inmediato a nuestros clientes, integrando prácticas ágiles e innovación continua. |
| **Visión** | Convertirnos en la empresa boliviana referente en ingeniería de software ágil e inteligencia artificial aplicada a la calidad, reconocida por acelerar la entrega de productos confiables. |
| **Elementos culturales que influyen en la investigación** | - **Orientación a la mejora continua** (facilita adopción de tu MVP).<br>- **Colaboración multidisciplinaria** (enfoque de “equipo completo” en pruebas).<br>- **Apertura a la innovación** (menor resistencia al cambio tecnológico).<br>- **Mentalidad ágil** (ciclos cortos requieren casos de prueba rápidos y eficaces).<br>- **Énfasis en la calidad** (dirección prioriza métricas objetivas de eficiencia y cobertura). |

---

### 4. Cómo utilizar esta información

1. **Procedimiento** → capítulo “Análisis de datos”, vinculando cada paso con instrumentos y variables operacionalizadas.  
2. **Tabla cronológica** → inicio del “Marco Teórico Referencial” para mostrar la evolución que sustenta tu propuesta.  
3. **Misión, visión y cultura** → “Marco Contextual” para evidenciar cómo el entorno organizacional habilita o condiciona la investigación.  

> ¡Listo! Copia/pega este contenido directamente en tu documento Markdown y ajústalo según tu estilo de citación preferido.
