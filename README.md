# Laboratorio 8 — Embeddings

Laboratorio de NLP sobre embeddings distribucionales en español. El notebook principal es `lab8.ipynb` y debe ejecutarse desde este directorio.

## Contenido

- `lab8.ipynb`: desarrollo reproducible, resultados y visualizaciones.
- `requirements.txt`: dependencias con versiones fijadas.
- `models/`: modelos propios y vectores del modelo seleccionado.
- `outputs/`: gráficas generadas por el notebook.
- `data/`: datos y recursos locales; los datasets grandes y fastText SUC no deben subirse al repositorio.
- `reporte.md`: resumen de metodología, resultados y limitaciones.

## Ejecución

Desde la raíz del proyecto:

```powershell
python -m venv .venv_lab8
.\.venv_lab8\Scripts\Activate.ps1
python -m pip install --upgrade pip
python -m pip install -r .\Lab8\requirements.txt
python -m ipykernel install --user --name lab8-embeddings --display-name "Python (Lab8 Embeddings)"
```

Abrir `lab8.ipynb`, seleccionar el kernel `Python (Lab8 Embeddings)` y ejecutar desde `Lab8`. El archivo SUC M se carga con `limit=200_000` y se mantiene fuera de Git.

## Modelo propio seleccionado

Se seleccionó `vector_size_50` entre las variantes exigidas por el PDF. Obtuvo el mejor top-5 de analogías (23.08 %) y la correlación de Spearman menos negativa del conjunto evaluado (-0.0326), con 90 % de cobertura del gold standard.

## Nota sobre el PDF

El documento menciona clasificación, búsqueda y una sección 9 en los entregables, pero no especifica completamente los experimentos, particiones, métricas ni parámetros necesarios. Por eso esas partes se identifican como no especificadas y no se presentan resultados inventados.
