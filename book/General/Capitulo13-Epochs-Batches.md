# ideas clave
Gradient Descent no actualiza los parámetros después de ver todo Internet. Los actualiza ddespués de procesar pequeños grupos de ejemplos llamados batches (o mini-batches).

# Definiciones
Dataset: Todo el conjunto de entrenamiento.
Batch: Un grupo de ejemplos procesados antes de actualizar los parámetros.
Mini-Batch: En la práctica, cuando hablamos de Deep Learning, casi siempre Batch y Mini-Batch significan lo mismo: un subconjunto del dataset que se procesa antes de hacer una actualización.
Una epoch consiste en recorrer una vez todo el dataset.

```batch
Dataset
↓
Batch 1
↓
Actualizar parámetros
↓
Batch 2
↓
Actualizar parámetros
↓
...
↓
Último batch
↓
Fin de una Epoch
```

```bash
Epoch 1
↓
Epoch 2
↓
Epoch 3
↓
...
```

Batch muy pequeño
Ventajas:
- aprende rápido;
- necesita poca memoria.
- actualizaciones más frecuentes.

Inconvenientes:
- mucho ruido;
- aprendizaje menos estable.

Batch enorme
Ventajas:
- gradientes muy estables.

Inconvenientes:
- muchísima memoria;
- actualizaciones menos frecuentes.

# Relación con los temas anteriores
```bash
Batch

↓

Forward Pass

↓

Softmax

↓

Cross Entropy

↓

Backpropagation

↓

Gradient Descent

↓

Actualizar parámetros

↓

Siguiente Batch
```


## ¿Qué es un dataset?
Es el conjunto completo de datos

## ¿Qué es un batch?
Un subconjunto de un dataset

## ¿Qué es una epoch?
Es el proceso de todo un dataset

## ¿Por qué no entrenamos con un único ejemplo cada vez?
Entrenar de ejemplo en ejemplo requiere muy poca memoria y es rápido pero no es un aprendizaje homogéneo
Produce gradientes muy ruidosos porque cada ejemplo puede apuntar en una dirección distinta.


## ¿Por qué no entrenamos con todo el dataset de una vez?
Tardía mucho tiempo y necesitaría muchos recursos

## ¿Qué ventajas e inconvenientes tiene un batch grande y uno pequeño?
Un batch pequeño requiere  menos tiempo y memoria que uno grande pero por otra parte su aprendizje puede tener mas ruido

## Explica una analogía propia para epochs y batches.
un batch es como una lección de este curso de IA, el dataset sería todo el curso y un epoch sería como hacer el curso una vez del principio al final

## ¿Cómo encajan batches, epochs, Forward Pass, Backpropagation y Gradient Descent en el entrenamiento?
Para cada batch se realiza un Forward Pass, se calcula la Loss, se ejecuta Backpropagation y finalmente Gradient Descent actualiza los parámetros. Tras procesar todos los batches se completa una epoch.

# Proceso completo
```bash
Texto

↓

Tokens

↓

Embeddings

↓

Attention

↓

Multi-Head

↓

Representación contextual

↓

Logits

↓

Softmax

↓

Cross Entropy

↓

Backpropagation

↓

Gradient Descent

↓

Actualizar parámetros

↓

Nuevo Batch

↓

Nueva Epoch
```