# Resultados generados

Los notebooks generan automáticamente las visualizaciones y tablas utilizadas para documentar las distintas fases del TFM.

## Figuras

Los Notebooks 01, 03 y 04 generan las visualizaciones almacenadas en `reports/figures/`.

```text
figura_3_01_registros_variables_por_ciudad.png
figura_3_02_distribucion_precio_logprice.png
figura_3_03_muestra_por_ciudad_outliers.png
figura_3_04_superficie_precio.png
figura_3_05_habitaciones_banos_precio.png
figura_3_06_equipamientos_precio.png
figura_3_07_aparcamiento_precio.png
figura_3_08_precio_mediano_ciudad.png
figura_3_09_precio_m2_ciudad.png
figura_3_10_matriz_correlaciones.png
figura_5_01_mediana_equipamientos.png
figura_5_02_r2_ajustado_modelos.png
figura_5_03_comparacion_r2_aic_bic.png
figura_5_04_betas_estandarizadas.png
figura_5_05_radar_sin_superficie.png
figura_5_06_factor_secundario_dominante.png
figura_5_07_residuos_ajustados.png
figura_5_08_diagnosticos_modelos.png
```

## Tablas

Los cuatro notebooks exportan tablas de resultados y de trazabilidad a `reports/tables/`.  
El prefijo del archivo identifica el notebook que lo genera.

### Notebook 01 — Selección e integración

```text
01_detalle_variables_exclusivas.csv
01_frecuencia_variables.csv
01_registros_integrados_por_ciudad.csv
01_resumen_archivos_por_ciudad.csv
01_resumen_frecuencia_variables.csv
01_resumen_variables_exclusivas_por_ciudad.csv
01_variables_comunes.csv
01_variables_totales.csv
```

### Notebook 02 — Preprocesamiento y transformación

```text
02_categorias_variables_vacias.csv
02_resumen_aparcamiento.csv
02_resumen_caracteristicas.csv
02_resumen_nulos_por_intervalo.csv
02_resumen_reducciones_precio.csv
02_resumen_variables_restantes.csv
02_tipos_datos.csv
02_variables_completamente_vacias.csv
02_variables_revision_mas_90_nulos.csv
```

### Notebook 03 — Análisis exploratorio

```text
03_estadisticas_precio.csv
03_matriz_correlaciones.csv
03_mediana_aparcamiento.csv
03_mediana_equipamientos.csv
03_mediana_precio_por_estado.csv
03_mediana_variables_complementarias.csv
03_muestra_por_ciudad.csv
03_precio_m2_mediano_por_ciudad.csv
03_precio_mediano_por_ciudad.csv
```

### Notebook 04 — Modelización OLS y diagnóstico

```text
04_coeficientes_estandarizados_HC3.csv
04_comparacion_modelos.csv
04_diagnosticos_modelos.csv
04_muestra_por_ciudad.csv
04_resumen_modelos_por_ciudad.csv
04_significancia_variables_adicionales.csv
04_variable_mas_influyente_sin_superficie.csv
04_vif_por_ciudad.csv
```

Las figuras y tablas incluidas documentan las salidas académicas generadas durante el análisis exploratorio y la modelización OLS. El Notebook 04 publicado incorpora además la validación *holdout* 80/20 y el contraste predictivo con Random Forest descritos en la versión final del TFM.

Las salidas pueden regenerarse ejecutando los notebooks en el orden indicado en el `README.md` principal, siempre que se disponga de los datos originales no publicados.

## Resultados incorporados en la versión final del TFM

La versión definitiva añade los resultados derivados de los cambios metodológicos finales:

- `04_validacion_train_test_modelos.csv`: métricas train/test de OLS base y ampliado.
- `04_comparacion_train_test_modelos.csv`: comparación fuera de muestra entre ambas especificaciones OLS.
- `04_resultados_random_forest.csv`: resultados por ciudad del Random Forest de 500 árboles.
- `04_comparacion_ols_random_forest.csv`: comparación directa OLS ampliado vs. Random Forest en test.
- `04_top5_importancias_random_forest.csv`: cinco variables con mayor importancia interna del Random Forest por ciudad.
- `figura_5_09_r2_test_base_ampliado.png`: R² de test de OLS base y ampliado.
- `figura_5_10_comparacion_ols_random_forest.png`: comparación de métricas fuera de muestra.
- `figura_5_11_r2_test_ols_random_forest.png`: comparación gráfica del R² de test entre OLS ampliado y Random Forest.

Estos archivos corresponden a los resultados de la versión final del Notebook 04 y completan las tablas y figuras que ya existían en el repositorio anterior.
