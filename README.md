# Proyecto: Análisis de jugadores del Mundial FIFA 2022

Este proyecto tiene como objetivo analizar los datos de los jugadores de FIFA 2022 para identificar los mejores equipos y jugadores que participaron en el Mundial de Fútbol 2022. Utilizo técnicas de análisis de datos y visualización para explorar las estadísticas de los jugadores, determinar los mejores equipos por país y proponer alineaciones óptimas basadas en formaciones tácticas.

## Herramientas utilizadas
- **Python**: Lenguaje de programación principal.
- **Pandas**: Para la manipulación y análisis de datos.
- **NumPy**: Para operaciones numéricas.
- **Seaborn y Matplotlib**: Para la visualización de datos.
- **Jupyter Notebook**: Entorno de desarrollo interactivo.

## Datos
El conjunto de datos utilizado es `players_22.csv`, que contiene información detallada sobre los jugadores de FIFA 22, incluyendo:
- Nombre corto (`short_name`)
- Edad (`age`)
- Nacionalidad (`nationality_name`)
- Valoración general (`overall`)
- Potencial (`potential`)
- Club (`club_name`)
- Valor en euros (`value_eur`)
- Salario en euros (`wage_eur`)
- Posiciones (`player_positions`)

## Pasos del proyecto

### 1. Carga y limpieza de datos
- Se cargan los datos desde el archivo `players_22.csv`.
- Se filtran las columnas relevantes para el análisis.
- Se eliminan jugadores que no participaron en el Mundial 2022.
- Se normalizan las posiciones de los jugadores para simplificar el análisis.

### 2. Análisis exploratorio de datos (EDA)
- **Distribución de la valoración general (`overall`)**: Se visualiza la distribución de las valoraciones de los jugadores.
- **Mejor equipo del Mundial 2022**: Se identifica el mejor equipo posible basado en la valoración general y las posiciones.
- **Mejor jugador por país**: Se determina el jugador con la mayor valoración general para cada país participante.

### 3. Mejor equipo por país
- Se define una función (`mejor_equipo`) para seleccionar el mejor equipo de cada país basado en la valoración general y las posiciones.
- Se calcula el promedio de valoración general para cada equipo.

### 4. Mejor alineación por formación
- Se definen tres formaciones tácticas comunes: `4-3-3`, `4-4-2` y `4-2-3-1`.
- Se crea una función (`best_lineup`) para seleccionar la mejor alineación para un país dado y una formación específica.
- Se identifica la formación óptima para los 10 mejores equipos según su promedio de valoración.

## Resultados

### Mejores equipos por promedio de valoración
| Equipo       | Promedio de Valoración |
|--------------|------------------------|
| España       | 82.40                  |
| Portugal     | 81.73                  |
| Brasil       | 81.67                  |
| Inglaterra   | 81.30                  |
| Francia      | 80.93                  |
| Italia       | 80.83                  |
| Argentina    | 80.30                  |
| Alemania     | 80.17                  |
| Bélgica      | 79.03                  |
| Países Bajos | 78.66                  |

### Mejores formaciones por equipo
- **España**: `4-2-3-1` (Promedio: 85.1)
- **Portugal**: `4-2-3-1` (Promedio: 84.9)
- **Brasil**: `4-3-3` (Promedio: 84.82)
- **Inglaterra**: `4-4-2` (Promedio: 84.45)
- **Francia**: `4-2-3-1` (Promedio: 83.9)
- **Italia**: `4-3-3` (Promedio: 84.45)
- **Argentina**: `4-3-3` (Promedio: 83.09)
- **Alemania**: `4-2-3-1` (Promedio: 84.0)
- **Bélgica**: `4-3-3` (Promedio: 82.91)
- **Países Bajos**: `4-3-3` (Promedio: 82.55)

## Visualizaciones
- **Distribución de la valoración general**: Histograma que muestra la distribución de las valoraciones de los jugadores.
- **Mejor jugador por país**: Gráfico de barras que muestra el mejor jugador de cada país según su valoración general.
- **Promedio de valoración por equipo**: Gráfico de barras que muestra los 10 mejores equipos según su promedio de valoración.

## Cómo ejecutar el proyecto
1. Clona este repositorio.
2. Instala las dependencias necesarias:
   ```bash
   pip install pandas numpy seaborn matplotlib jupyter