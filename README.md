# 📱 Análisis de Datos y Segmentación de Clientes: ConnectaTel

## 🎯 Objetivo del Proyecto
El objetivo principal de este proyecto es analizar los patrones de consumo y las características demográficas de los usuarios de la empresa de telecomunicaciones **ConnectaTel**. A través de la limpieza de datos, análisis exploratorio y segmentación, se busca identificar perfiles de clientes de alto valor, corregir anomalías en los registros y proveer insights accionables para rediseñar la oferta comercial de ofertas de prepago y pospago.

## 🗂️ Datasets Utilizados
El análisis integra múltiples fuentes de datos relacionales provistas por la compañía:
* `plans`: Catálogo de los planes comerciales ofrecidos (Básico, Premium).
* `users`: Demografía de los clientes (edad, ciudad, fecha de registro).
* `usage`: Registro transaccional detallado del consumo de llamadas (duración) y mensajes (cantidad) por usuario.

## 🛠️ Etapas del Análisis Realizadas
1. **Carga y Exploración (EDA):** Ingesta inicial de datos y revisión de estructuras, tipos de datos y estadísticas descriptivas.
2. **Limpieza y Calidad de Datos:** Tratamiento de valores centinela (ej. edad -999), estandarización de nulos estructurales (MAR) en los registros de consumo, y corrección de fechas anómalas (años futuros).
3. **Ingeniería de Características:** Agrupación y suma del consumo individual para crear métricas consolidadas (`cant_mensajes`, `cant_llamadas`, `cant_minutos_llamada`) por cliente.
4. **Análisis de Outliers (Heavy Users):** Uso de visualizaciones (Histogramas y Boxplots) y el método del Rango Intercuartílico (IQR) para identificar usuarios de consumo extremo, justificando su retención por su alto valor comercial.
5. **Segmentación de Clientes:** Creación de cohortes analíticas clasificando a los usuarios según su nivel de actividad (Bajo, Medio, Alto) y grupo demográfico (Joven, Adulto, Adulto Mayor).
6. **Insight Ejecutivo:** Generación de recomendaciones estratégicas basadas en el comportamiento real de los segmentos frente a los planes contratados.

## 🚀 Cómo ejecutar el Notebook (Guía de Reproducción)

Para revisar o ejecutar este análisis localmente o en la nube:

**Requisitos previos:**
* Python 3.8 o superior.
* Librerías: `pandas`, `numpy`, `matplotlib`, `seaborn`.

**Ejecución:**
1. Clona este repositorio: `git clone [URL_DE_TU_REPOSITORIO_AQUI]`
2. Asegúrate de que los archivos de datos (CSV) estén en la misma carpeta que el notebook, o ajusta las rutas de lectura en la primera celda.
3. Abre el archivo principal `.ipynb` utilizando **Jupyter Notebook** localmente, o súbelo a **Google Colab**.
4. Ejecuta las celdas secuencialmente (de arriba hacia abajo) para replicar la limpieza, la fusión de tablas y la generación de gráficos.
