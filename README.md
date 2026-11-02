# Proyecto Estadísticas de YouTube (PLN)

Proyecto del curso de Procesamiento de Lenguaje Natural (Especialización en Inteligencia Artificial, Universidad de Cundinamarca).

**Objetivo:** predecir qué tanto interactúa la gente con un video de YouTube — `engagement = (likes + comentarios) / vistas`, en escala logarítmica — a partir de los comentarios y de algunos datos del video.

**Datos:** [YouTube Statistics (advaypatil, Kaggle)](https://www.kaggle.com/datasets/advaypatil/youtubestatistics): ~1.881 videos y ~18.409 comentarios.

**Código base:** el taller [lemrei2025-ai/Analisis_PLN_Youtube--II](https://github.com/lemrei2025-ai/Analisis_PLN_Youtube--II), que los notebooks clonan para ejecutar el pipeline.

## Notebooks

Ejecutarlos en este orden, en Google Colab:

| # | Notebook | Qué hace | Abrir |
|---|----------|----------|-------|
| 1 | `00_colab_inicio.ipynb` | Prepara el entorno, descarga y valida los datos, limpia el texto y construye las variables | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jensulvillalba/proyecto-youtube/blob/main/00_colab_inicio.ipynb) |
| 2 | `01_eda.ipynb` | Análisis estadísticos de los datos | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jensulvillalba/proyecto-youtube/blob/main/01_eda.ipynb) |
| 3 | `02_modelos.ipynb` | Entrena y compara cinco modelos (Base, Ridge, SVM lineal, Bosque aleatorio y Gradient boosting), prueba un ensamble y analiza el modelo seleccionado | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jensulvillalba/proyecto-youtube/blob/main/02_modelos.ipynb) |

## Cómo reproducirlo

1. Abrir el notebook en Google Colab con el botón de la tabla.
2. Guardar las credenciales en los **Secretos** de Colab (nunca escritas en el código): `KAGGLE_API_TOKEN` y `YOUTUBE_API_KEY`.
3. Conectar Google Drive cuando el notebook lo pida (ahí se guardan datos y reportes).
4. Ejecutar las celdas en orden.

## Resultado en breve

El modelo seleccionado fue **Ridge** (regresión lineal regularizada) con variables de contexto, features de los comentarios y TF-IDF. Casi iguala a los modelos más complejos, es más rápido y es fácil de explicar. Un ensamble de los cuatro modelos mejoró un poco más, pero solo se midió en la prueba, sin validación cruzada.

## Equipo

- Jensul Villalba Gaitán
