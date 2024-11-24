# NLP - Clasificación Automática de Tickets

## Índice

- [Índice](#índice)
- [Introducción](#introducción) 
  - [Métodos Utilizados](#métodos-utilizados)
  - [Tecnologías](#tecnologías)
- [Descarga y Configuración](#descarga-y-configuración)
  - [Requisitos Previos](#requisitos-previos)
  - [Cómo Ejecutar](#cómo-ejecutar)
- [Declaración del Problema](#declaración-del-problema)
  - [Objetivo Comercial](#objetivo-comercial)
  - [Preparación de Datos:](#preparación-de-datos)
  - [Construcción y Evaluación del Modelo](#construcción-y-evaluación-del-modelo)
  - [Conclusiones](#conclusiones)

## Introducción

Actualmente se dispone de una variedad vasta de datos relacionados a diversas industrias que pueden ser analizados y considerados como un dataset para aplicar los modelos de Machine Learning, Deep Learning o Inteligencia Artificial.

A lo largo de este documento se resume la aplicación del Procesamiento del Lenguaje Natural, más conocido como NLP, el cual es una rama de Ciencias de la Computación, específicamente de la Inteligencia Artificial, la cual brinda a las computadoras la capacidad de entender como los humanos se comunican (escriben y hablan).

La aplicación del NLP se hará al conjunto de datos (formato .json) que contiene las quejas de los clientes en función de los productos y servicios de una empresa. Debido a que estos datos no se encuentran etiquetados, se requiere aplicar alguna técnica para analizar patrones y clasificar los tickets en cinco grupos según sus productos/servicios.

	* Tarjetas de crédito / Tarjetas preparadas
	* Servicios de cuentas de banco
	* Reportes de robos 
	* Préstamos hipotecarios y otros préstamos
	* Otros

### Métodos Utilizados

Algoritmo de aprendizaje:
	Factorización de matrices no negativas (NMF): Es un algoritmo de aprendizaje automático que se utiliza para descomponer una matriz no negativa.

Modelos de Machine Learning:
	- Regresión Logística
	- Árbol de Decisión
	- Bosque Aleatorio
	- Naive Bayes

### Tecnologías
	- Software: Google Colaboratory
	- Lenguaje de programación: Python
	- Bibliotecas o librerías de análisis y manipulación de datos:
		Pandas
		NumPy
	- Bibliotecas o librerías de NLP:
		nltk
		nltk.tokenize
		nltk.corpus
		nltk.stem
	- Bibliotecas de código abierto para NLP:
		SpaCy, ofrece una amplia gama de funciones
		PyCaret, simplifica el proceso de creación, evaluación e implementación de los modelos
	- Modelo de lenguaje
		en_core_web_sm, divide el texto en tokens individuales
	- Herramientas de visualización de datos
		Matplotlib
		Seaborn
		plotly

## Descarga y Configuración
### Requisitos Previos

Este proyecto necesita Google Colaboratory para la ejecución.

### Cómo Ejecutar

Puede descargar el código fuente clonando este repositorio usando Git:

1. Abra su aplicación Terminal favorita (Unix, Linux o Macos), como Terminal, Comando, Consola, iTerm2, etc.

2. Clone el repositorio

```
[[git clone <GITHUB_REPO_URL>](https://github.com/georgevallejos/MDSv5_ML-P2-Clasificacion-Automatica-de-Tickets-Grupo-5.git)]
https://github.com/georgevallejos/MDSv5_ML-P2-Clasificacion-Automatica-de-Tickets-Grupo-5.git
```

3. Abra el archivo notebook ** NLP - Clasificacion Automatica de Tickets.ipynb ** en Google Colaboratory


## Declaración del Problema

Los datos del dataset reflejan distintas quejas de los clientes en función de los productos y servicios, lo que implica una revisión individual de las quejas lo que ocasiona que la atención no sea oportuna; por lo tanto, este inconveniente puede subsanarse con la estratificación de las quejas en grupos específicos.

### Objetivo Comercial

Segregar los tickets de quejas en las categorías más relevantes para brindar al cliente una resolución oportuna.

Aplicar modelos supervisados de Machine Learning.

### Preparación de Datos:

1. Importar el dataset (formato .json)
   Los datos están en formato JSON y se convierte a un dataframe.
2. Limpieza de Datos y Análisis de Datos Faltantes.
   Inspección del dataframe
   Imprimir las columnas
   Asignar nuevos nombres de las columnas
   Asignar NAN en lugar de los datos faltantes en la columna de quejas
3. Procesamiento de texto
   Cambiar el texto en minúsculas
   Eliminar el texto entre corchetes
   Depurar la puntuación
   Eliminar las palabras que contienen números 

   Lematizar los textos
   Extraer las etiquetas POS del texto lematizado    
4. Análisis exploratorio de datos (EDA)
   Visualizar los datos en función a la longitud de caracteres
   Tomando una nube de palabras, encuentre las top 40 palabras que se presenten con mayor frecuencia
   Encontrar los mejores unigramas, bigramas y trigramas por frecuencia entre las quejas 
   Aplicar la métrica TF-IDF (medida de la importancia de una palabra en un documento en comparación con un corpus de documentos más grandes)
   Implementar la técnica no supervisada (NMF)
5. Modelado de temas
   Se requiere adoptar el enfoque de prueba y error con el fin de encontrar la mejor cantidad de tópicos para el modelo NMF.
6. Construcción de modelos mediante aprendizaje supervisado
   Esta sección consiste en la clasificación automática de cualquier nueva queja
7. Entrenamiento y evaluación de modelos
8. Inferencia de modelos

### Conclusiones

Regresión Logística
Árbol de Decisión
Bosque Aleatorio

#### Regresión Logística

#### Árbol de Decisión

#### Bosque Aleatorio

