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
~~~
import seaborn as sns

sns.scatterplot(x = x, y = y)

# Equivalente a:
sns.scatterplot(x = "x", y = "y", data = df)

# Equivalente a:
sns.relplot(x = x, y = y)
~~~
![grafico-dispersion-seaborn](https://github.com/user-attachments/assets/03ffae71-fc52-4523-a388-7ea33a42bfa5)

### Gráficos de líneas (lineplot): 
- #### Ideales para mostrar tendencias a lo largo del tiempo.
~~~
import seaborn as sns

sns.lineplot(x, y)

# Equivalente a:
sns.lineplot(x = "x", y = "y", data = df)
~~~
![lineplot-seaborn](https://github.com/user-attachments/assets/9b25a7c0-9f9b-4d7e-a9f0-ec778c509dba)

### Histogramas (histplot): 
- #### Visualizan la distribución de datos.
~~~
import numpy as np
import seaborn as sns

# Simulación de datos
rng = np.random.RandomState(0)
x = rng.normal(0, 1, size = 1000)
df = {'x': x}

# Histograma
sns.histplot(x = x)

# Equivalente a:
sns.histplot(x = "x", data = df)
~~~
![histplot-seaborn](https://github.com/user-attachments/assets/83bace35-353f-4c20-bd52-d8b1555f910c)

### Gráficos de densidad (kdeplot): 
- #### Representan la estimación de densidad de probabilidad de una variable.
~~~
import numpy as np
import seaborn as sns

# Simulación de datos
rng = np.random.RandomState(4)
x = rng.normal(0, 1, size = 100)
df = {'x': x}

# Gráfico de densidad
sns.kdeplot(x = x)

# Equivalente a:
sns.kdeplot(x = "x", data = df)
~~~
![image](https://github.com/user-attachments/assets/ebf1f697-0264-40a0-a878-e062ea4ead68)

### Gráficos de caja (boxplot): 
- #### Muestran la distribución de datos con base en cuartiles.
~~~
import seaborn as sns

# Box plot
sns.boxplot(x = variable)

# Equivalente a:
sns.boxplot(x = "variable", data = df)
~~~
![image](https://github.com/user-attachments/assets/8f899c7d-e06a-4550-8213-abec5b5a6eef)

### Gráficos de violín (violinplot): 
- #### Combinan características de los gráficos de caja y de densidad.
~~~
import seaborn as sns

# Gráfico de violín
sns.violinplot(x = variable)

# Equivalent to:
sns.violinplot(x = "variable", data = df)
~~~
![image](https://github.com/user-attachments/assets/58a99db4-de49-4f33-9b00-e85aed753fe2)

### Gráficos de barras (barplot): 
- #### Comparan cantidades en diferentes categorías.
~~~
import seaborn as sns

# Gráfico de barras
sns.barplot(x = grupo, y = variable)

# Equivalente a:
sns.barplot(x = "grupo", y = "variable", data = df)
~~~
![image](https://github.com/user-attachments/assets/2261edf5-a72e-481a-a9b3-9427403fec29)

### Gráficos de pares (pairplot): 
- #### Muestran todas las combinaciones de variables en un conjunto de datos.
~~~
import seaborn as sns

sns.pairplot(df, vars = ["petal_length", "petal_width"])
~~~
![image](https://github.com/user-attachments/assets/e9deabb8-2ce3-4328-8c3f-a5da6c341596)

### Mapas de calor (heatmap): 
- #### Visualizan datos en forma de matriz, destacando patrones con colores.
~~~
import numpy as np
import seaborn as sns

# Simulación de datos
np.random.seed(1)
data = np.random.rand(10, 10)

sns.heatmap(data)
~~~
![image](https://github.com/user-attachments/assets/6169fe30-864a-4fe9-bc9c-6462a964f932)

# Estilos para una Presentación Más Profesional

## Seaborn incluye varios estilos predefinidos que puedes utilizar para hacer tus gráficos más atractivos:

### Estilo de fondo oscuro (darkgrid): 
- #### Útil para destacar datos en gráficos complejos.
~~~
import numpy as np
import seaborn as sns

# Datos
rng = np.random.RandomState(10)
x = rng.normal(0, 1, size = 100)

# Establecer el color de fondo
sns.set_style(rc = {'axes.facecolor': 'lightsteelblue'})

# Gráfico
sns.histplot(x = x) 
~~~
![image](https://github.com/user-attachments/assets/77661f15-4976-4ed2-9d00-ffa15ab3eef5)

### Estilo blanco con cuadrícula (whitegrid): 
- #### Muy utilizado en presentaciones por su claridad.
~~~
import seaborn as sns

df = sns.load_dataset("tips")

sns.set_style("whitegrid")

sns.boxplot(x = "day", y = "total_bill", data = df) 
~~~
![image](https://github.com/user-attachments/assets/230b07fb-345c-4ef5-9a1e-e333fd9bfeb6)

### Estilo limpio (white): 
- #### Sin cuadrículas, ideal para gráficos más simples.
~~~
import seaborn as sns

df = sns.load_dataset("tips")

sns.set_style("white")

sns.boxplot(x = "day", y = "total_bill", data = df) 
~~~
![image](https://github.com/user-attachments/assets/6cfa3a5e-5e94-4aea-beeb-dfce2153dba1)


