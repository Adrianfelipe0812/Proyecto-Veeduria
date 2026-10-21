# Eficiencia y riesgo en el Plan Distrital de Desarrollo de Bogotá 2024–2027

> Anteproyecto de trabajo de grado — Facultad de Estadística, Maestría en Ciencia de Datos, Universidad Santo Tomás, seccional Bogotá.

## Resumen  

Este proyecto propone integrar información financiera, avances físicos y reportes institucionales para estudiar la eficiencia técnica de metas-producto comparables del Plan Distrital de Desarrollo (PDD) de Bogotá 2024–2027, **“Bogotá Camina Segura”**, y explorar la identificación anticipada de riesgos de subejecución física.

La estrategia plantea medir eficiencia relativa mediante Análisis Envolvente de Datos (DEA), organizar información narrativa de los reportes con técnicas de Procesamiento de Lenguaje Natural (NLP) y evaluar modelos de clasificación con validación temporal. Se espera formular un procedimiento analítico reproducible que apoye el seguimiento institucional y la priorización de metas que requieran revisión.

**Estado:** anteproyecto y diseño metodológico. El repositorio contiene archivos de trabajo, pero no presenta resultados empíricos de DEA ni métricas de modelos predictivos entrenados.

## Problema de investigación

La ejecución financiera, el avance físico de las metas y las explicaciones de su cumplimiento se encuentran en fuentes distintas. Revisar cada componente por separado dificulta interpretar si los recursos se traducen en resultados físicos y reconocer barreras operativas que pueden explicar brechas o rezagos.

El proyecto propone integrar estas fuentes para comparar metas con características semejantes, estudiar barreras presentes en los reportes y evaluar si la información disponible en cada corte permite anticipar riesgos de subejecución física.

## Pregunta de investigación

¿De qué manera la integración de la medición de eficiencia técnica y el análisis de información cualitativa permite evaluar la eficiencia y clasificar anticipadamente las metas-producto y actividades según su nivel de riesgo de subejecución física en el Plan de Desarrollo Distrital de Bogotá?

## Objetivos

### Objetivo general

Diseñar y evaluar un esquema analítico para el seguimiento de las metas-producto del Plan Distrital de Desarrollo de Bogotá 2024–2027, integrando información financiera y física de SEGPLAN, medición de eficiencia técnica mediante DEA y variables obtenidas de reportes no estructurados mediante NLP, con el fin de explorar la identificación anticipada de riesgos de subejecución física.

### Objetivos específicos

1. **Medir eficiencia:** estimar la eficiencia técnica relativa de metas-producto comparables, relacionando los recursos financieros utilizados con el avance físico registrado en los cortes de seguimiento.
2. **Analizar reportes:** identificar y estructurar barreras operativas o de gestión presentes en los reportes institucionales y estudiar su relación con las brechas de eficiencia observadas.
3. **Explorar riesgo futuro:** construir y evaluar un modelo de clasificación que use la información disponible hasta cada corte para estimar el riesgo de subejecución física en el periodo siguiente y comparar su desempeño con una línea base financiera.

## Alcance y fuentes

- **Ámbito:** Plan Distrital de Desarrollo de Bogotá 2024–2027, “Bogotá Camina Segura”.
- **Población de referencia:** 425 metas-producto registradas en las fuentes oficiales de seguimiento.
- **Unidad de análisis:** metas-producto y, para la predicción, registros meta–corte.
- **Fuentes previstas:** información de Avance del Plan de Desarrollo, Gestión e Inversión y reportes institucionales asociados a SEGPLAN.
- **Criterio de inclusión:** cada componente se analizará según la disponibilidad, calidad, trazabilidad y comparabilidad de los datos. DEA se aplicará únicamente a grupos de metas con una lógica de comparación defendible.

La cantidad efectiva de observaciones puede variar entre los componentes DEA, NLP y predictivo. La población de referencia no implica que todas las metas necesariamente puedan incluirse en cada análisis.

## Metodología propuesta

1. **Revisión y preparación:** inventariar las fuentes y sus cortes; homologar identificadores, fechas y unidades; revisar duplicados, faltantes, consistencia y comparabilidad.
2. **Medición de eficiencia:** estimar puntajes DEA dentro de grupos comparables. La orientación, los rendimientos a escala y la selección de insumos y productos se definirán después de revisar los datos; se propone evaluar inicialmente un modelo BCC con rendimientos variables a escala.
3. **Procesamiento de reportes:** extraer y normalizar texto, identificar categorías de barreras y vincularlas con una meta y un corte cuando exista trazabilidad suficiente.
4. **Análisis de asociaciones:** estudiar la relación entre las barreras identificadas y las brechas de eficiencia, sin atribuir causalidad al diseño no experimental.
5. **Clasificación temporal:** usar información del periodo *t* para estimar riesgo en *t + 1*, respetar el orden cronológico en la validación y comparar el modelo integrado con una línea base de indicadores financieros.
6. **Revisión de SFA:** evaluar la viabilidad de la Frontera Estocástica como contraste. Solo se incorporará si hay suficientes observaciones y puede justificarse una forma funcional; de lo contrario, el análisis de eficiencia se concentrará en DEA.

## Archivos disponibles

La carpeta [`Capa Bronce/`](Capa%20Bronce/) contiene los cuatro archivos incorporados al repositorio:

- `01_avancefisico20260630 (1).xlsx`
- `inf_pdd_30_6_26.pdf`
- `planacciongestioninversion20260630_entidades.pdf`
- `planacciongestioninversion20260630_ver20260728 (1).xlsx`

La presencia de estos archivos no significa que ya hayan sido depurados, integrados o utilizados para producir resultados. Antes de su análisis se deben revisar su contenido, cobertura, calidad, condiciones de uso y correspondencia entre metas y cortes.

## Estructura preparada

```text
.
├── README.md
├── Capa Bronce/          # Archivos fuente originales
└── Capa Silver/
    └── README.md         # Propósito y flujo de transformación previsto
```

La capa Silver está documentada como preparación para el trabajo en Databricks. Todavía no contiene código ELT ni datos procesados. La capa Gold se agregará cuando se inicie su diseño.
## Equipo

- Jhonatan Smith Doncel Murillo
- Jorge Emmanuel Marín Linares
- Adrian Felipe Grateron Ramírez
- Carlos Isaac Zainea Maya

Facultad de Estadística, Maestría en Ciencia de Datos — Universidad Santo Tomás, seccional Bogotá.

## Consideraciones metodológicas

- Los puntajes DEA son relativos a las unidades comparadas y dependen de la homogeneidad de los grupos y de la calidad de las variables.
- La definición de riesgo de subejecución debe basarse en la programación, la periodicidad y la información realmente disponible en cada corte.
- La validación predictiva debe evitar el uso de información futura y compararse con una línea base financiera.
- Los reportes narrativos pueden variar en formato y detalle; las transformaciones y categorías deben documentarse para favorecer la reproducibilidad.
- El estudio es no experimental, retrospectivo y longitudinal; sus asociaciones no deben interpretarse como efectos causales.

## Licencia y uso de datos

El repositorio aún no especifica una licencia de software o de datos. Antes de redistribuir los archivos, se deben verificar las condiciones de uso, atribución y publicación de cada fuente institucional y definir una licencia apropiada.

