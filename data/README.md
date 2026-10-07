# Datos

Este directorio mantiene separadas las dos etapas de datos utilizadas por los notebooks.

## `raw/`

Contiene los archivos Excel originales de las diez ciudades. Estos archivos **no se publican en el repositorio**.

Para ejecutar los Notebooks 01 y 02, deben situarse en `data/raw/` con los siguientes nombres:

```text
A Coruña 2026.xlsx
Alicante 2026.xlsx
Avila 2026.xlsx
Barcelona 2026.xlsx
Las Palmas 2026.xlsx
Madrid 2026.xlsx
Malaga 2026.xlsx
Sevilla 2026.xlsx
Valencia 2026.xlsx
Zaragoza 2026.xlsx
```

El código localiza archivos que siguen el patrón:

```text
* 2026.xlsx
```

y utiliza el nombre del archivo para identificar la ciudad.

## `processed/`

El Notebook 02 genera automáticamente:

```text
viviendas_limpio.csv
```

Este archivo contiene el conjunto procesado utilizado como entrada común para el análisis exploratorio y la modelización.

Los datos procesados tampoco se publican en el repositorio. Para reproducirlos debe ejecutarse primero el Notebook 02 a partir de los archivos originales.
