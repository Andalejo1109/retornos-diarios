# retornos-diarios

# Análisis de Desempeño de Portafolios (2026)

Este repositorio contiene un script en Python para el análisis y visualización del desempeño de un portafolio de inversión específico para el año 2026.

## Descripción

Este proyecto se centra en la simulación y análisis de un portafolio de inversión compuesto por varios ETFs y acciones (SPYG, SMH, IEMG, VTI, BRK-B) con pesos predefinidos. El script descarga datos históricos del mercado, calcula rendimientos diarios, rendimientos mensuales acumulados, y el rendimiento acumulado Year-to-Date (YTD) con una media móvil de 50 días. Además, proporciona visualizaciones claras del desempeño diario, mensual y las correlaciones entre los activos del portafolio.

Aunque los datos se descargan para un periodo futuro (2026-01-01 a 2026-08-07), esto se puede ajustar fácilmente para analizar datos históricos reales.

## Características

-   **Definición de Portafolio**: Fácil configuración de activos (tickers) y sus pesos.
-   **Descarga de Datos**: Utiliza `yfinance` para obtener datos de precios ajustados.
-   **Cálculo de Rendimientos**: Determina los rendimientos diarios y el rendimiento del portafolio.
-   **Análisis de Días**: Clasifica los días como positivos, negativos o neutros.
-   **Rendimiento Acumulado Mensual y YTD**: Cálculo del desempeño a lo largo del tiempo, incluyendo una media móvil de 50 días para el YTD.
-   **Visualizaciones Interactivas**: Generación de gráficos para:
    -   Rendimiento Diario del Portafolio (con resumen de días positivos/negativos/neutros y YTD actual).
    -   Evolución Acumulada Year-to-Date (YTD) con media móvil de 50 días.
    -   Rendimiento Mensual del Portafolio.
    -   Matriz de Correlación entre los activos del portafolio.
 
    ![Gráfico de Desempeño Acumulado](desempeño_acumulado.png)

## Requisitos

Asegúrate de tener instaladas las siguientes librerías de Python:

-   `pandas`
-   `yfinance`
-   `matplotlib`
-   `seaborn`

Puedes instalarlas usando `pip`:

```bash
pip install pandas yfinance matplotlib seaborn
```

## Uso

1.  **Clona el repositorio**:
    ```bash
    git clone https://github.com/andalejo1109/retornos-diarios.git
    cd nombre_del_repositorio
    ```

2.  **Abre el Notebook en Google Colab o tu entorno preferido**:
    Si estás en Google Colab, sube el archivo `.ipynb` directamente.

3.  **Ejecuta las celdas del Notebook**:
    El notebook está estructurado secuencialmente. Ejecuta cada celda para:
    -   Importar las librerías necesarias.
    -   Definir los tickers y pesos de tu portafolio.
    -   Descargar los datos históricos (puedes ajustar el rango de fechas en la celda correspondiente).
    -   Realizar los cálculos de rendimiento.
    -   Generar y visualizar los gráficos de desempeño.

4.  **Modifica el portafolio**:
    Ajusta la lista `tickers` y `pesos` en la primera celda para analizar diferentes composiciones de portafolio.

5.  **Ajusta el rango de fechas**:
    Modifica los parámetros `start` y `end` en la función `yf.download()` para cambiar el período de análisis de los datos.

## Contribuciones

¡Las contribuciones son bienvenidas! Si deseas mejorar este proyecto, puedes:

-   Abrir un *issue* para reportar errores o sugerir nuevas características.
-   Crear un *pull request* con tus mejoras.

## Licencia

Este proyecto está bajo la Licencia MIT. Consulta el archivo `LICENSE` para más detalles.
