# Pipeline Integral de Ciencia de Datos
## Análisis de Adjudicaciones y Contratos — DNCP Paraguay (2021–2022)

Trabajo Práctico — Maestría en Ciencia de Datos | Universidad Comunera

---

## Descripción

Análisis completo del pipeline de ciencia de datos aplicado a datos reales de contrataciones públicas del Estado paraguayo, obtenidos del Portal de Datos Abiertos de la DNCP. Se trabaja con ~24,000 registros de adjudicaciones de los años 2021 y 2022.

## Estructura del repositorio

```
/
├── data/
│   ├── records_adjudicaciones_2021.csv
│   ├── records_adjudicaciones_2022.csv
│   ├── records_contratos_1.csv
│   └── records_contratos_2.csv
├── notebooks/
│   └── prediccion_riesgo_crediticio.ipynb
├── reports/
│   └── informe_final.pdf
├── requirements.txt
└── README.md
```

## Etapas del trabajo

| Etapa | Descripción | Resultado |
|---|---|---|
| 1 | Carga, limpieza y preprocesamiento | 23,982 registros, 24 columnas |
| 2 | Análisis Exploratorio (EDA) | Distribución por modalidad, institución y monto |
| 3 | Clasificación supervisada | Random Forest — Accuracy 0.70, F1 0.65 |
| 4 | Regresión supervisada | Random Forest — R² 0.637, MAE USD 8,804 |
| 5 | Clustering | 4 perfiles de instituciones identificados |

## Dataset

- **Fuente:** [contrataciones.gov.py/datos](https://www.contrataciones.gov.py/datos)
- **Formato:** CSV — Open Contracting Data Standard (OCDS)
- **Años:** 2021 y 2022
- **Registros finales:** 23,982 adjudicaciones completas

## Instalación

```bash
pip install -r requirements.txt
```

## Dependencias

```
pandas==2.2.2
numpy==2.0.2
scikit-learn==1.6.1
matplotlib==3.10.0
seaborn==0.13.2
```

## Uso de IA generativa

Este documento README y partes del código fueron asistidas por herramientas de IA generativa, identificadas en el notebook con el comentario `# Asistido por IA`.
