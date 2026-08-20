# 🏆 Premier League 2026-2027: Modelo Predictivo y Simulación de Monte Carlo

## 📝 Descripción del Proyecto
Este proyecto es un análisis predictivo de datos (Data Analytics) diseñado para pronosticar los resultados de la temporada 2026-2027 de la English Premier League. Utilizando datos históricos de los últimos 10 años, el proyecto ejecuta simulaciones de Monte Carlo en Python para determinar las probabilidades de campeonato y descenso de los 20 equipos participantes, visualizando los resultados en un dashboard interactivo.

## 🛠️ Tecnologías Utilizadas
* **Lenguaje:** Python 3.x
* **Librerías:** `pandas` (ETL y manipulación de datos), `numpy` (Simulaciones estadísticas)
* **Visualización de Datos:** Google Looker Studio
* **Formatos de datos:** `.xlsx`, `.csv`

## 🧠 Metodología (Pipeline de Datos)

1. **Extracción y Limpieza (ETL):** 
   * Se procesó un dataset histórico abarcando desde la temporada 2016-17 hasta la 2025-26.
   * Se aplicó limpieza de strings, separación de columnas comprimidas y casting de tipos de datos usando `pandas`.
2. **Transformación y Lógica de Negocio:**
   * **Promedio Ponderado:** Se asignó un peso mayor a las temporadas más recientes para reflejar el estado de forma actual de los equipos.
   * **Tratamiento de Ascendidos:** Los equipos sin historial reciente (ej. Coventry City) recibieron estadísticas base calculadas a partir del rendimiento promedio histórico de los equipos recién ascendidos en la última década (38 Pts).
3. **Simulaciones de Monte Carlo:**
   * Se simularon 10,000 escenarios distintos de la temporada usando distribuciones normales (`numpy.random.normal`) con una desviación estándar aplicada a los Puntos Esperados, capturando la volatilidad del fútbol real (lesiones, rachas, suerte).
4. **Data Storytelling & UX:**
   * Exportación de los resultados procesados y conexión a Looker Studio.
   * Diseño de métricas con formato condicional, barras de datos in-cell y renderizado dinámico de escudos mediante URLs.

## 📊 Dashboard Interactivo
El resultado visual de este modelo puede explorarse aquí:
👉 **[Enlace a tu Dashboard en Looker Studio]**

### Captura de pantalla
*(Sube aquí una imagen JPG/PNG de tu dashboard y pon la ruta aquí, ej: `![Dashboard](dashboard_preview.png)`)*

## 🚀 Cómo ejecutar este proyecto localmente
1. Clona este repositorio:
   ```bash
   git clone [https://github.com/tu-usuario/premier-league-prediction.git](https://github.com/tu-usuario/premier-league-prediction.git)
