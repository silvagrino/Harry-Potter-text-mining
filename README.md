9# Harry-Potter-text-mining



📚 Análisis de Texto de la Saga de Harry Potter 🧙‍♂️

[INTRO DE IMPORTANCIA E HITOS DE HP]

Descripción del Proyecto
Este proyecto realiza un análisis del texto completo de los siete libros de la saga Harry Potter mediante técnicas de minería de datos 
y procesamiento de lenguaje natural (PLN). El objetivo principal es extraer patrones, identificar palabras clave y explorar características 
lingüísticas que permitan una comprensión más profunda de esta icónica obra literaria.

A través del uso de R y librerías especializadas, este análisis se desarrolla utilizando métodos de preprocesamiento de texto, 
extracción de temas, análisis de redes semánticas y más.

Objetivos del Proyecto
Procesar y limpiar los textos de los libros para convertirlos en datos estructurados listos para análisis.
Identificar palabras frecuentes, temas recurrentes y asociaciones de términos clave.
Visualizar patrones en el texto mediante gráficas, nubes de palabras y diagramas.
Proponer nuevos enfoques analíticos, incluyendo análisis de sentimientos, modelado de tópicos y análisis de complejidad textual.


# 1. Preguntar

Como cambia la saga a traves de los 7 años en que transcurre esta obra literaria?
Cuales son los principales personajes en cada entrega ademas de HP?
Que tienen que decir las asociaciones de palabras con respecto a los sentimientos que los acompañan?
Hay ciertos personajes que estan mas relacionados con ciertos sentiemientos o moods?
Que analisis extras y conclusiones podemos sacar mediante la mineria de texto aplicada en este analisis?
Analizar la frecuencia de palabras relacionadas con emociones y temas a lo largo de los capítulos.


asociaciones DIFERNCIA?
asosaciones

# 2. Preparar


1. Preparación de Datos

Fuente de Datos: Archivo pdf de la saga completa de libros Harry Potter

Constituido por 7 archivo [DESCRIPCION DEL DATASET]


### Para preparar los datos aplicaré un Enfoque ROCCC:

Reliable/Confiablilidad: Libros escritos por la autora JK Rowling. 

Original/Originalidad: Datos originales obtenidos directamente de los libros

Comprehensive/Integralidad: Gran cantidad de datos, muchas descripciones todas partes de las descripciones de los videos alojados en youtube

Current/Actuales: Exitosa saga estrenada en --- qe finalizo con su ultimo libro en ---

Cited/Citación: [?????????]

### El dataset tiene limitaciones:

El Tamaño de la muestra 

Inconsistencia en distribución de datos ?


Método de registro ?

Fechas de registro ?

##### LA REDACCION TIENE QUE SER DIFERENTE, NO ES UN DATASET COMO EN LOS ANTERIORES CASOS. TIENE QE SER UNA DESCRIPCION DE LOS LUBROS Y SU IMPACTO E INFLUENCIA.



# 3. Procesar

Empiezo a limpiar el dataset , preparandolo para ha


### PONER CODIGO FINAL DONDE CARGO TODOS LOS ARCHIVOS Y LES HAGO SU RESPECTIVO CORPUS A C/U


Preprocesamiento de Texto:
Los textos son procesados para:

Convertirlos a minúsculas.
Eliminar puntuación y números.
Remover palabras irrelevantes (stopwords) en español.
Crear corpora para su análisis.

2. Análisis Exploratorio

Análisis de Frecuencia:




# 4. Analisis


## FRECUENCIA DE CADA LIBRO Y FRECUENCIA DE TODA LA SAGA

Palabras más frecuentes en cada libro.
Comparación de frecuencias entre los libros.

Gráficas de barras de las palabras más frecuentes.
Nubes de palabras para destacar términos clave.



3. Minería de Texto Avanzada

### Análisis de Redes Semánticas:


### Modelado de Tópicos:

Uso de LDA (Latent Dirichlet Allocation) para identificar temas latentes.



###  Análisis de Sentimientos:
Evaluar emociones y polaridad en los textos.

```
library(syuzhet)

# Análisis de sentimientos
emociones <- get_nrc_sentiment(unlist(libros[[1]]))
barplot(colSums(emociones), las = 2, col = rainbow(10),
        main = "Distribución de emociones en el libro 1")
```

###################################################################

El análisis de sentimientos con el paquete syuzhet puede complementar tu trabajo actual al explorar
las emociones y polaridades presentes en los textos

El paquete syuzhet incluye el lexicón NRC, que evalúa 8 emociones (alegría, tristeza, miedo, etc.) y la polaridad (positivo/negativo).

### Integra con tus análisis previos
Relaciona emociones con temas (LDA)
- Examina si los temas latentes identificados con LDA están asociados con emociones particulares.
Ejemplo:
 Tema "magia" puede tener más emociones de "alegría".
 Tema "oscuridad" puede asociarse con "miedo" o "tristeza".
- Temporalidad de emociones (opcional)
Si tienes datos temporales (capítulos o escenas), podrías mapear cómo cambian las emociones a lo largo de los libros usando funciones
como get_sentiment para calcular un puntaje de sentimiento continuo.

#### Personajes principales y emociones y polaridades asociadas.

¿Qué puedes obtener de este análisis?
Distribución emocional: Cómo varían las emociones (miedo, tristeza, alegría, etc.) en cada libro.
Tono general: Identificar si un libro es más positivo o negativo en términos emocionales.
Evolución narrativa: Analizar cómo las emociones cambian a lo largo de la saga, reflejando el desarrollo de la trama.

## 4. Posibilidades de Análisis Adicional

Estudio de la evolución narrativa: Analizar la frecuencia de palabras relacionadas con emociones y temas a lo largo de los capítulos.
Análisis estilístico: Examinar la complejidad sintáctica (longitud promedio de oraciones, uso de adjetivos, etc.).
Comparativas temáticas: Comparar el uso de palabras clave entre personajes principales.
Generación de resúmenes automáticos: Extraer resúmenes utilizando algoritmos de agrupación.




Visualización:
ggplot2, wordcloud, igraph
Análisis avanzado:
topicmodels, syuzhet
