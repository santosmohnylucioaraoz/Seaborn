# Seaborn

### Seaborn es una biblioteca de visualización de datos en Python que se basa en Matplotlib. Fue diseñada para hacer que la creación de gráficos estadísticos sea más fácil y atractiva visualmente. Aquí te dejo algunos puntos clave sobre Seaborn:

### Facilidad de uso: 
- #### Seaborn simplifica la creación de gráficos complejos al proporcionar funciones de alto nivel que requieren menos código.

### Estadísticas integradas: 
- #### Permite realizar visualizaciones que incorporan análisis estadístico de manera sencilla, como gráficos de regresión y distribuciones.

### Estilos y temas: 
- #### Ofrece una variedad de estilos y paletas de colores que facilitan la creación de gráficos más atractivos y profesionales.

### Compatibilidad con pandas: 
- #### Se integra fácilmente con DataFrames de pandas, lo que facilita la manipulación y visualización de datos.

### Gráficos diversos: 
- #### Permite crear una amplia gama de visualizaciones, como gráficos de dispersión, líneas, barras, cajas, violines y mapas de calor, entre otros.

# Tipos de Gráficos en Seaborn

## Seaborn es una biblioteca de visualización de datos en Python basada en Matplotlib. Ofrece una variedad de gráficos útiles:

### Gráficos de dispersión (scatterplot): 
- #### Muestran la relación entre dos variables numéricas.
import seaborn as sns

sns.lineplot(x, y)

# Equivalente a:
sns.lineplot(x = "x", y = "y", data = df)
![grafico-dispersion-seaborn](https://github.com/user-attachments/assets/03ffae71-fc52-4523-a388-7ea33a42bfa5)

### Gráficos de líneas (lineplot): 
- #### Ideales para mostrar tendencias a lo largo del tiempo.
Histogramas (histplot): Visualizan la distribución de datos.
Gráficos de densidad (kdeplot): Representan la estimación de densidad de probabilidad de una variable.
Gráficos de caja (boxplot): Muestran la distribución de datos con base en cuartiles.
Gráficos de violín (violinplot): Combinan características de los gráficos de caja y de densidad.
Gráficos de barras (barplot): Comparan cantidades en diferentes categorías.
Gráficos de pares (pairplot): Muestran todas las combinaciones de variables en un conjunto de datos.
Mapas de calor (heatmap): Visualizan datos en forma de matriz, destacando patrones con colores.
