# Actividad 4.1 — Modelado no supervisado para Big Data

## Pregunta
¿Qué estructuras de agrupación pueden identificarse a partir de las características cartográficas y qué tan confiables y útiles resultan los grupos obtenidos?

## Metodología
Covertype (581,012 observaciones): separación de `Cover_Type`; estandarización de 10 variables cuantitativas; conservación de 44 binarias en 0/1; Incremental PCA; MiniBatch K-Means para k=2–8 y semillas 17, 42 y 91; métricas internas; estabilidad mediante ARI; comparación con referencia sin PCA; validación externa final mediante ARI y NMI.

## Resultado
Se documenta `k=3, semilla=17` como configuración final. Se conservan 14 componentes, equivalentes a 95.51% de varianza acumulada. La concordancia externa es baja (ARI≈0.0289; NMI≈0.0189), por lo que los grupos se interpretan como segmentación exploratoria, no como categorías naturales definitivas.

## Reproducción
Instalar `requirements.txt` y ejecutar `notebooks/actividad_4_1_modelado.ipynb`. El archivo `data/covtype.data.gz` está incluido.

## Estructura
- `README.md`
- `notebooks/actividad_4_1_modelado.ipynb`
- `figures/`
- `data/covtype.data.gz`
- `requirements.txt`
- `cluster_results.csv`
- `stability_results.csv`
- `perfil_grupos.csv`

## Referencias
Blackard, J. A., & Dean, D. J. (2000). Comparative accuracies of artificial neural networks and discriminant analysis in predicting forest cover types from cartographic variables. *Computers and Electronics in Agriculture, 24*(3), 131–151.

Blackard, J. A., Dean, D. J., & Anderson, C. W. (1998). *Covertype dataset*. UCI Machine Learning Repository.

Pedregosa, F., et al. (2011). Scikit-learn: Machine Learning in Python. *Journal of Machine Learning Research, 12*, 2825–2830.
