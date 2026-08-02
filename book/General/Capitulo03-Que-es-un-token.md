# tokenizador
```
Texto

↓

Tokens

↓

IDs

↓

Embeddings

↓

Modelo (El modelo nunca ve el texto original. Solo ve embeddings.)
```


# ¿Qué es un token?
Es la unidad básica de información con la que trabaja el modelo.
Un texto se divide en tokens que pueden ser palabras, partes de palabras, signos de puntuación, etc.

# ¿Por qué un modelo no trabaja directamente con palabras? y # ¿Qué ventajas tiene dividir palabras largas en varios tokens?
En español kas palabras pueden tener sufijos o prefijos que matizan el significado de las palabras. Además hay palabras que tienen una raiz común que des da un significado parecido.
Trabajar con tokens permite reutilizar patrones comunes entre palabras distintas, reducir el tamaño del vocabulario y representar mejor palabras desconocidas o poco frecuentes.

# ¿Qué papel desempeña el tokenizador?
Divide un texto en tokens y les asigna un ID.

# ¿Por qué el identificador numérico de un token no representa su significado?
El ID es un identificador mientras que el significado viene dado por los embeddings.

# ¿Por qué Azure OpenAI cobra por tokens y no por palabras?
El coste computacional depende del número de tokens que el modelo procesa, no del número de palabras escritas. y una palabra puedo equivaler a uno o varios tokens

# Ideas clave del día
- Un token no es necesariamente una palabra.
- El tokenizador transforma texto en tokens y estos en IDs.
- El ID solo identifica al token; no contiene su significado.
- Los embeddings convierten esos IDs en representaciones matemáticas que el modelo puede procesar.
- El modelo nunca trabaja directamente con texto, sino con esas representaciones.
- En Azure OpenAI, el consumo y el contexto se miden en tokens.