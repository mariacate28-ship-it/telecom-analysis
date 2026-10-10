# Análisis ConnectaTel – Sprint 7

Análisis del comportamiento de uso de los clientes de **ConnectaTel**, empresa de telecomunicaciones con operaciones en México y Colombia, con datos registrados hasta 2024.

## 🎯 Objetivo
Identificar patrones de uso de llamadas y mensajes, detectar comportamientos atípicos y segmentar a los clientes por edad y nivel de uso, para proponer mejoras en la oferta comercial de planes.

## 📊 Datasets
- `plans.csv`: planes actuales (precio, minutos y GB incluidos, costo por extra).
- `users_latam.csv`: información de los clientes (edad, ciudad, fecha de registro, plan, churn).
- `usage.csv`: detalle del uso real (llamadas con duración y mensajes con longitud).

## 📂 Contenido del repositorio
- `S7 Version-Estudiante-Project-ConnectaTel.ipynb`: notebook principal con limpieza, estadísticas, visualizaciones, outliers, segmentación y conclusiones.

## 🔄 Etapas del análisis
1. Carga y exploración de los tres datasets.
2. Identificación de problemas de calidad: nulos, sentinels (-999 en edad, "?" en ciudad) y fechas fuera de rango.
3. Limpieza: imputación de edad con la mediana, conversión de sentinels a nulos y validación de nulos MAR.
4. Resumen estadístico del uso por usuario (mensajes, llamadas y minutos).
5. Visualización de distribuciones con histogramas y detección de outliers con boxplots y método IQR.
6. Segmentación de clientes por nivel de uso y grupo de edad.
7. Insight ejecutivo con conclusiones y recomendaciones comerciales.

## 💡 Hallazgos principales
- El 73.6% de los clientes tiene un uso medio; solo el 7% es de alto uso.
- Los usuarios Básico y Premium muestran patrones de uso muy similares.
- Se detectó un grupo atípico de usuarios con 130 a 155 minutos de llamada que requiere revisión.

## ▶ Cómo ver y ejecutar el notebook
- **Para ver el análisis:** haz clic en el archivo `.ipynb` de este repositorio. 
- **Para ejecutarlo:** descarga el archivo `.ipynb` y ábrelo en Jupyter Notebook.

## 🔁 Guía de reproducción
1. Descarga el notebook de este repositorio.
2. Coloca los archivos `plans.csv`, `users_latam.csv` y `usage.csv` en una carpeta llamada `datasets`, o ajusta las rutas de `pd.read_csv()` a la ubicación de tus archivos.
3. Instala las librerías necesarias: pandas, numpy, seaborn y matplotlib.
4. Ejecuta todas las celdas en orden (**Kernel → Restart Kernel and Run All Cells**).

## 🛠 Herramientas
Python (pandas, numpy, seaborn, matplotlib) y Jupyter Notebook.
