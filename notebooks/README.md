# Notebooks

Los cuatro notebooks reproducen secuencialmente el flujo completo del TFM.

## Orden de ejecución

1. `01_Seleccion_datos.ipynb`
2. `02_Preprocesamiento_transformacion.ipynb`
3. `03_Analisis_exploratorio_de_los_datos.ipynb`
4. `04_Modelizacion_regresiones_por_ciudad_zscore_train_test_random_forest_FINAL.ipynb`

## Descripción

### 01. Selección de datos
Revisa los diez archivos originales, analiza sus dimensiones y variables, identifica la intersección y la unión de columnas e integra los anuncios en una estructura común.

### 02. Preprocesamiento y transformación
Analiza los valores ausentes, elimina variables sin utilidad analítica, depura contenido auxiliar y multimedia, elimina registros completamente duplicados y genera `data/processed/viviendas_limpio.csv`.

### 03. Análisis exploratorio
Restringe el análisis a pisos, define la muestra comparativa, aplica el filtrado P1-P99 de `price` y `size` por ciudad, analiza las principales relaciones descriptivas y genera las figuras exploratorias.

### 04. Modelización y validación predictiva
Prepara las variables de modelización, construye las especificaciones OLS base y ampliada, estandariza mediante Z-score dentro de cada ciudad, aplica inferencia HC3 y calcula los diagnósticos estadísticos. Además, realiza una partición reproducible 80/20 con `random_state=42`, evitando *data leakage*, y compara el OLS ampliado con un Random Forest Regressor de 500 árboles.

La validación cruzada se contempla como posible extensión metodológica, pero no se ejecuta en el análisis definitivo.

## Rutas

Los notebooks detectan automáticamente la raíz del proyecto buscando simultáneamente:

```text
data/raw/
notebooks/
reports/
```

Por este motivo, debe conservarse la estructura del repositorio.

Las salidas de ejecución de los notebooks se han eliminado de los archivos `.ipynb` publicados para evitar incluir rutas locales o previsualizaciones de datos. Las tablas y figuras académicas generadas se conservan en `reports/`.
