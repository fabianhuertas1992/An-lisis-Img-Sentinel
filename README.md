
# Análisis Manual de NDVI - Comparativo de Dos Periodos

Este proyecto en Python permite realizar un análisis comparativo manual del índice de vegetación de diferencia normalizada (NDVI) entre dos periodos utilizando imágenes de Sentinel-2. El análisis se restringe a un área de interés definida por un archivo **GeoJSON**.

## Contenido

- Conexión a Google Drive (para cargar imágenes y guardar resultados).
- Instalación de librerías necesarias (rasterio, geopandas, shapely, matplotlib, etc.).
- Definición manual de rutas de entrada (imágenes anteriores, posteriores y GeoJSON).
- Cálculo del NDVI para cada imagen.
- Comparación de los resultados en gráficos.
- Clasificación de NDVI por coberturas vegetales.
- Generación de estadísticas de cambio.
- Exportación de resultados y gráficas.

## Requisitos

- Python 3.8 o superior
- Google Colab o entorno compatible
- Librerías:
  - `pystac-client`
  - `planetary-computer`
  - `geopandas`
  - `shapely`
  - `rioxarray`
  - `xarray`
  - `pyproj`
  - `rasterio`
  - `matplotlib`
  - `unidecode`
  - `weasyprint`
  - `scikit-learn`
  - `joblib`

## Estructura del Script

1. **Acceso a Google Drive**: monta Drive para acceder a las imágenes y guardar los resultados.
2. **Instalación de librerías**: asegura que todas las dependencias estén instaladas.
3. **Definición de rutas**: especifica las carpetas de las imágenes de los dos periodos y el archivo GeoJSON de análisis.
4. **Cálculo de NDVI**:
   - Normalización de bandas Red (B04) y NIR (B08).
   - Cálculo del índice NDVI.
5. **Análisis Comparativo**:
   - Comparación visual mediante gráficos.
   - Cálculo de cambios en la cobertura vegetal.
   - Estadísticas de cambios (hectáreas ganadas/perdidas por clase de NDVI).
6. **Resultados**:
   - Gráficos comparativos guardados como imágenes.
   - Exportación de tablas de resultados.
   - Opcionalmente, generación de un informe PDF (requiere `weasyprint`).

## Ejemplos de Resultados

- **Mapa NDVI de cada periodo**
- **Mapa de diferencia NDVI**
- **Gráficos de cambio por clases de vegetación**
- **Tabla resumen de cambios en hectáreas**

## Uso

1. Monta Google Drive en tu entorno Colab.
2. Define las rutas de imágenes y GeoJSON en las variables correspondientes.
3. Ejecuta el script paso a paso.
4. Visualiza y analiza los gráficos generados.
5. Revisa los resultados exportados en la carpeta de salida.

## Créditos

Desarrollado como parte de un análisis de prefactibilidad para proyectos de monitoreo ambiental mediante imágenes satelitales.
