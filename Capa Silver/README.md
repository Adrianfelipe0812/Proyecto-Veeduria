# Capa Silver

## Propósito

Preparar una versión limpia, normalizada e integrada de la información que llega desde [`Capa Bronce/`](../Capa%20Bronce/). Esta carpeta documenta el alcance previsto para la capa Silver; todavía no contiene procesos ELT ni tablas transformadas.

## Flujo previsto

1. Inventariar archivos, hojas, campos, periodos de seguimiento e identificadores disponibles.
2. Revisar calidad: tipos de dato, valores faltantes, duplicados, formatos y consistencia entre cortes.
3. Normalizar fechas, identificadores de metas, nombres de entidades, unidades y porcentajes.
4. Clasificar las variables según su significado y comportamiento temporal. Las categorías propuestas en el plan de trabajo (constante, creciente, decreciente y suma) deben validarse con el diccionario de datos antes de aplicarse.
5. Extraer y normalizar el texto de los informes y vincularlo con metas y cortes únicamente cuando exista una llave o trazabilidad suficiente.
6. Documentar cada transformación y conservar la relación con los archivos fuente.

## Trabajo previsto en Databricks

La implementación ELT y las tablas resultantes probablemente se desarrollarán en Databricks. Antes de iniciar, el equipo definirá dónde vivirá el código (por ejemplo, notebooks o archivos fuente), cómo se sincronizará con GitHub y dónde se almacenarán las tablas. No se incluyen credenciales, tokens ni datos procesados en este marcador.

## Criterios para considerar una tabla Silver lista

- Identificadores y fechas tienen formatos consistentes.
- Los cambios de estructura y reglas de limpieza están documentados.
- Los valores faltantes, duplicados y excepciones quedan cuantificados o explicados.
- Cada registro conserva trazabilidad hacia su fuente y corte.
- La integración entre datos tabulares y texto no inventa correspondencias cuando no hay identificadores confiables.

> Estado: capa preparada como documentación. Las transformaciones y salidas aún no se han implementado.
