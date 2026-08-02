Attention permite que cada palabra decida qué información del resto del contexto necesita para comprender su propio significado.

Las palabras de una frase se observan entre sí para decidir cuáles son relevantes.

## atención y embeddings
Attention calcula cuánto debe influir cada palabra del contexto en la representación de otra palabra
```
Embedding inicial # posición de los tokens en n-dimensiones

↓

Capa Attention 1 # crea nueva repesentación según el contexto 

↓

Representación 1 # hidden representation, contextual representation o hidden state.

↓

Capa Attention 2

↓

Representación 2

↓

Capa Attention 3

↓

Representación 3

↓

...

↓

Representación final
```


## ¿Qué problema resolvió Attention respecto a modelos anteriores?
Attention permitió que las palabras midieran la relación con las palabras de la frase, tanto si están a continuación como si están algo mas lejos.
Antes del Transformer había un problema llamado dependencias a largo plazo.

## Explica con tus palabras qué significa que una palabra "preste atención" a otra.
Significa lo importante que una palabra enconcreto para su significado o acción que toma como predecir el siguiente token

## ¿Por qué Attention permite entender mejor frases largas?
Porque relaciona palabras que no tienen que estar juntas.

## ¿Cómo modifica Attention los embeddings iniciales?
Modifica la representación de los embeddings teniendo en cuenta el contexto

# ¿Qué relación existe entre Attention y el funcionamiento de un sistema RAG?
En un sistema RAG, Attention ayuda al modelo a identificar qué partes del contexto recuperado son más relevantes para responder la pregunta del usuario.

## ¿Por qué el artículo Attention Is All You Need supuso un cambio tan importante en la historia de la IA?
Porque permitió el uso de significados mas exactos en las palabras

# conceptos
Hay un embedding inicial (estático) y después una sucesión de representaciones contextuales (dinámicas).