# Capa Gold

## Propósito

Organizar productos analíticos listos para consultas y consumo por herramientas de visualización. Esta carpeta documenta el alcance previsto para la capa Gold; todavía no contiene tablas calculadas, consultas SQL ni resultados.

## Productos analíticos previstos

- Tablas de análisis que relacionen metas, avances físicos, indicadores y, cuando sea posible, información narrativa vinculada.
- Indicadores agregados y trazables, con su definición, unidad de medida, periodo y reglas de cálculo.
- Consultas SQL que permitan obtener conjuntos claros para responder preguntas del proyecto; por ejemplo, avance porcentual por meta.
- Datos preparados para visualizaciones como gráficos de barras horizontales, si son adecuados para el indicador y la pregunta analítica.

El ejemplo de una tabla meta–avance–texto es una idea inicial. Su diseño definitivo dependerá de las variables disponibles y de las decisiones metodológicas del proyecto.

## Consumo y publicación

Power BI y Gradio pueden consumir productos de Gold si se confirman como herramientas del equipo. Las aplicaciones, la conexión a modelos de IA y el despliegue (por ejemplo, en Hugging Face) son componentes de presentación o publicación y se definirán aparte de las tablas Gold.

La implementación y el almacenamiento podrían realizarse en Databricks. El equipo deberá definir cómo se versionarán las consultas y el código en GitHub, y cómo se compartirán las tablas sin incluir credenciales ni información restringida.

## Criterios para considerar un producto Gold listo

- Tiene una pregunta de análisis y una población o nivel de agregación definidos.
- Documenta campos, unidades, periodos, filtros y fórmulas.
- Mantiene trazabilidad hacia las fuentes y transformaciones de Silver.
- Se valida con controles básicos de consistencia antes de conectarlo a una visualización.
- Distingue resultados descriptivos de predicciones y no presenta prototipos como sistemas en producción.

> Estado: capa preparada como documentación. Las tablas, consultas y visualizaciones aún no se han implementado.
