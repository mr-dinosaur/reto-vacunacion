# Reto de Pandas y Numpy | Análisis del progreso mundial de vacunación

Análisis con Python (pandas y NumPy) del dataset
[COVID-19 World Vaccination Progress](https://www.kaggle.com/datasets/gpreda/covid-world-vaccination-progress)
(Our World in Data, vía Kaggle): 86,512 registros de 223 países, del 2020-12-02 al 2022-03-29.

## Contenido

| Archivo | Descripción |
|---|---|
| `DS_C2_SC2_CarlosTapia.ipynb` | Libreta con los requerimientos a–l (texto + código) |
| `resultadosReto.xlsx` | DataFrames generados, una hoja cada uno: `conDiferencias`, `conCantidad`, `antes20`, `pfizer` |

## Cómo ejecutarlo

1. Abre la libreta en Colab: [Abrir en Google Colab](https://colab.research.google.com/drive/1m_ywkgJ20ug2yRnMaSbAcvfNqWoUaCjq?usp=sharing)
2. Ejecuta todo (`Entorno de ejecución > Ejecutar todo`).
   La libreta descarga el dataset con `kagglehub`; si falla, pide subir `country_vaccinations.csv`.

## Resultados principales

- Vacunas aplicadas en el mundo (suma de `daily_vaccinations`): **11,320,239,871**
- Promedio por país: **50,763,407**
- Vacunas aplicadas el 29/01/2021: **4,884,052**
- Periodo cubierto: **482 días**
- Registros antes del 20/12/2020: **70**
- Registros con vacuna Pfizer: **64,193**

## Decisiones de análisis

- "Vacunas aplicadas" se calcula con `daily_vaccinations`, la única columna diaria. Sumar `total_vaccinations` contaría las dosis varias veces.
- Los valores vacíos (`NaN`) no se rellenan: se ignoran en sumas y promedios. Rellenarlos alteraría los resultados.
- `diferencias` = `daily_vaccinations` − `daily_vaccinations_raw`.
- `canVac` = número de vacunas distintas del registro, separando `vaccines` por coma.

## Autor

Carlos Alberto Tapia Hernández y Claude como herramienta
