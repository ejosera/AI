Un embedding es una representación matemática que sitúa un concepto dentro de un espacio donde la distancia refleja relaciones aprendidas durante el entrenamiento.

Palabras con varios significados puede tener varios mapas.

El significado representado por un token cambia según el contexto, aunque el embedding inicial del token sea el mismo.

Embedding + atención -> representación 

## ¿Qué problema resuelven los embeddings?
Los embeddings representan en "un mapa n-dimensional" la relación entre palabras. A menor distancia mayor relación.

# ¿Por qué un ID numérico no es suficiente para representar el significado de una palabra?
El ID es una etiqueta sin significado. Es muy difícil sino imposible definit todos los matices de una palabra en un ID.

# Explica con tus palabras qué representa un embedding.
Es la estructura matemática que relaciona las conceptos.

# ¿Por qué dos palabras con significados parecidos suelen tener embeddings cercanos?
Palabras con significados cercanos se relacionan con palabras similares por lo que su embedding será similar.

# ¿Qué papel juega el contexto en la creación y uso de los embeddings?
El contexto modifica la representación del concepto para adaptarla al significado que tiene dentro de esa frase.

# ¿Por qué los embeddings son fundamentales para RAG y Azure AI Search?
Porque dan flexibilidad a las busquedas y no solo buscar por cadena de texto igual sino por significado