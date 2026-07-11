# Datos — Licitaciones DNCP Paraguay (2021–2022)

Los archivos CSV de este proyecto (~101 MB en total) **no se versionan en git**
(ver `.gitignore` en la raíz). Esta carpeta documenta su origen y cómo obtenerlos.

## Archivos esperados

| Archivo | Contenido |
|---|---|
| `records_adj_2021.csv` | Adjudicaciones 2021 |
| `records_adj_2022.csv` | Adjudicaciones 2022 |
| `records_contratos_2021.csv` | Contratos 2021 |
| `records_contratos_2022.csv` | Contratos 2022 |

## Origen

- **Fuente:** Portal de Datos Abiertos de la DNCP (Dirección Nacional de
  Contrataciones Públicas del Paraguay) — [contrataciones.gov.py/datos](https://www.contrataciones.gov.py/datos)
  - Adjudicaciones: https://www.contrataciones.gov.py/datos/adjudicaciones
  - Contratos: https://www.contrataciones.gov.py/datos/contratos
- **Formato:** CSV según el estándar [Open Contracting Data Standard (OCDS)](https://standard.open-contracting.org/)
- **Años:** 2021 y 2022

## Descarga

El notebook (`notebooks/licitaciones_paraguay.ipynb`) descarga automáticamente
los CSV en su primera celda de código usando `gdown`, desde una carpeta pública
de Google Drive:

```python
import gdown
gdown.download_folder(
    url='https://drive.google.com/drive/folders/1738grWDl9j2VXf3ju0JFq0Njo2WXiQGo',
    output='data',
    quiet=False,
)
```

> Nota: la carpeta de Drive debe estar compartida como
> "Cualquiera con el enlace" para que la descarga funcione.

También pueden descargarse manualmente desde el Portal DNCP (enlaces arriba)
y colocarse en esta carpeta con los nombres de la tabla.
