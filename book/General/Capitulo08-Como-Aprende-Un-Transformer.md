# Idea clave
Un modelo no aprende reglas. Aprende valores numéricos que terminan comportándose como si hubieran aprendido reglas.


Arquitectura = la ecuación
Conocimiento = los parámetros de esa ecuación

# Fase de entrenamiento
```
Texto
↓
Predicción
↓
Error
↓
Modificar parámetros
↓
Modelo ligeramente mejor
↓
Repetir miles de millones de veces
```

# Fase de inferencia (usar ChatGTP)
```
Texto
↓
Tokens
↓
Embeddings
↓
Attention
↓
Heads
↓
Nueva representación
↓
Predicción
```

# ¿Qué sabe un Transformer justo después de ser creado?
Justo después de ser creado no sabe nada. Sus parámetros se inicializan con valores (normalmente pequeños y casi aleatorios), por lo que sus predicciones son prácticamente aleatorias. Durante el entrenamiento esos parámetros se ajustan para reducir el error.

# ¿Qué es un parámetro?
Un parámetro es un valor numérico que determina cómo transforma la información el modelo. Durante el entrenamiento esos valores se ajustan para reducir el error.

# ¿Qué significa entrenar un modelo?
Significa iterar el modelo comparandolo con la realidad para ajustar los parámetros para reducir el error.

# ¿Cómo aprende el modelo si nadie le escribe reglas?
Mediante el ajuste de los parámetros y comprobando el error. Se itera una y otra vez para minimizar el error.

# ¿Dónde está almacenado el conocimiento?
El conocimiento está almacenado en los valores de los parámetros del modelo.

# Explica con una analogía qué representan los parámetros.
Una receta tiene ingredietes y los parametros son la cantidad de cada ingrediente

# ¿Cuál es la diferencia entre la arquitectura del Transformer y el conocimiento del modelo?
La arquitectura sería la formula del transformer y el conocimiento serían los parámetros bien ajustados

## Conexiones con capítulos anteriores
- Los embeddings son parámetros entrenables.
- Las matrices WQ, WK y WV también son parámetros entrenables.
- Multi-Head Attention funciona gracias a esos parámetros.
- Durante la inferencia esos parámetros permanecen fijos.