<div align="center">

# Análisis Exploratorio de Datos (EDA)

## Hecho por:

<br/>

<p> <strong> 1. Carlos Manuel Vargas López. </strong></p>
<p> <strong> 2. Iris Violeta Talavera. </strong></p>
<p> <strong> 3. David Antonio Membreño Ríos. </strong></p>
<p> <strong> 4. Jocsan Stiven Mejía Villereal. </strong></p>
<p> <strong> 5. Jether Alejandro Martínez Solís. </strong></p>

<br/>

<p align="center">
  <img src="https://th.bing.com/th/id/OIP.wp7VLwfL8Z8gsOHP1J3i8wHaEn?rs=1&pid=ImgDetMain" alt="Texto alternativo" width="400">
</p>

</div>

## Introducción

El Análisis Exploratorio de Datos (EDA) es un proceso crucial para comprender conjuntos de datos y prepararlos para análisis posteriores. Implica varias etapas, cada una con funciones y técnicas específicas para resumir, visualizar y limpiar los datos. Este EDA se realizó a una base de datos con información de ventas y pedidos de la empresa Tecno Nic.

## Etapa 1: Análisis Descriptivo
Esta etapa implica resumir las principales características de los datos.

### Funciones Clave:
- **Características del DataFrame:**
  - `df.shape`: Devuelve el número de filas y columnas.
  - `df.columns`: Lista las columnas.
  - `df.head()`: Muestra las primeras filas.
  - `df.tail()`: Muestra las últimas filas.
  - `df.describe()`: Proporciona resúmenes estadísticos.
  - `df.info()`: Muestra tipos de datos y valores no nulos.
  - `df.values`: Devuelve los valores en un array de NumPy.

- **Acceso a Datos:**
  - `df['nombre_columna']` o `df.nombre_columna`: Accede a una columna específica.
  - `df.loc[índice]`: Accede a una fila por índice.
  - `df.iloc[posición]`: Accede a una fila por posición.

- **Selección Condicional:**
  - `df[df['nombre_columna'] > valor]`: Selecciona filas basadas en una condición.
  - `df.query('condición')`: Selección condicional más expresiva.

- **Modificación de Datos:**
  - `df['nueva_columna'] = valores`: Agrega una nueva columna.
  - `df.drop('nombre_columna', axis=1, inplace=True)`: Elimina una columna.
  - `df.copy()`: Crea una copia del DataFrame.
  - `df.drop_duplicates()`: Elimina filas duplicadas.

- **Reemplazo de Valores:**
  - `df.rename(columns={'viejo_nombre': 'nuevo_nombre'})`: Renombra columnas.
  - `df.replace(valor_a_reemplazar, nuevo_valor)`: Reemplaza valores específicos.

- **Visualización de Datos:**
  - Utiliza histogramas, gráficos de barras y gráficos de pastel para visualizar distribuciones y frecuencias.

## Etapa 2: Ajuste de Tipo de Variables
Asegura que cada variable esté almacenada con el tipo de datos correcto.

### Funciones Clave:
- **Tipos de Datos:**
  - `df.dtypes`: Muestra los tipos de datos de cada columna.

- **Manejo de Fechas:**
  - `pd.to_datetime(df['nombre_columna'])`: Convierte a datetime.
  - Extrae componentes: `df['nombre_columna'].dt.day`, `df['nombre_columna'].dt.month`, `df['nombre_columna'].dt.year`.
  - Calcula diferencias de tiempo: `df['diferencia'] = df['fecha_final'] - df['fecha_inicial']`.

- **Datos Categóricos:**
  - `df['nombre_columna'] = df['nombre_columna'].astype('category')`: Convierte a categoría.
  - `df['nombre_columna'].unique()`: Obtiene categorías únicas.
  - `df['nombre_columna'].cat.set_categories(['cat1', 'cat2', 'cat3'])`: Establece categorías específicas.

## Etapa 3: Detección y Tratamiento de Datos Ausentes
Detecta y trata los datos ausentes para asegurar la integridad del análisis.

### Funciones Clave:
- **Detección:**
  - `df.isna()` o `df.isnull()`: Detecta valores nulos.

- **Eliminación:**
  - `df.dropna()`: Elimina filas o columnas con valores nulos.

- **Relleno:**
  - `df.fillna(valor)`: Rellena valores nulos con un valor específico.
  - `df.interpolate()`: Interpola valores nulos.

## Etapa 4: Identificación y Tratamiento de Datos Atípicos
Identifica y trata los datos atípicos que pueden sesgar los resultados.

### Técnicas Clave:
- **Visualizaciones:**
  - **Histogramas**: Para entender la distribución de datos y detectar atípicos.
  - **Diagramas de Caja (Boxplots)**: Para visualizar la distribución y identificar atípicos.

- **Métodos Estadísticos:**
  - **Z-score**: Identifica atípicos basados en desviaciones estándar de la media.
  - **Z-score Modificado**: Usa la mediana y MAD para distribuciones no normales.
  - **Rango Intercuartílico (IQR)**: Identifica atípicos basados en la dispersión de los datos.

## Etapa 5: Correlación de Variables
Examina las relaciones entre variables para identificar patrones.

### Técnicas Clave:
- **Coeficientes de Correlación:**
  - Correlación de Pearson: Valores entre -1 (fuerte negativa) y 1 (fuerte positiva), con 0 indicando ninguna correlación.

## Etapa 6: Visualización de Datos
Utiliza visualizaciones para entender y comunicar los datos.

### Bibliotecas Clave:
- **Seaborn (`sns`):**
  - Interfaz de alto nivel para gráficos estadísticos atractivos y complejos (histogramas, gráficos de dispersión, boxplots, gráficos de barras, gráficos de líneas, mapas de calor).

- **Matplotlib (`plt`):**
  - Biblioteca versátil para crear gráficos estáticos, interactivos y personalizados con control detallado.

### Tipos de Análisis:
- **Análisis Univariado:**
  - Comprender distribuciones y tendencias de variables individuales.
- **Análisis Bivariado:**
  - Explorar relaciones entre dos variables.
- **Análisis Multivariado:**
  - Analizar interacciones entre múltiples variables simultáneamente.

## Conclusión

El EDA es un proceso iterativo e interactivo que involucra resumir, visualizar y limpiar datos para descubrir patrones, detectar anomalías y formular hipótesis para análisis posteriores. Cada etapa y técnica juega un papel vital en la preparación de datos para análisis más sofisticados y en asegurar la precisión y confiabilidad de los resultados. Este análisis se realizó específicamente para la base de datos de ventas y pedidos de la empresa Tecno Nic.
