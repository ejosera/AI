# idea clave
El transformer crear una puntuación, logit, para cada token
Softmax convierte el logit en probabilidades
Cross entropy compara probabilidades predichas con las esperadas y calcula el valor de la Loss Function.

```bash
Forward Pass

↓

Logits

↓

Softmax

↓

Probabilidades

↓

Cross Entropy

↓

Loss

↓

Backpropagation

↓

Gradient Descent
```

## ¿Qué son los logits?
Los logits son las puntuaciones que el Transformer asigna a cada token antes de convertirlas en probabilidades.

## ¿Por qué los logits no pueden considerarse probabilidades?
Porque pueden tomar cualquier valor (positivo, negativo o muy grande) y no cumplen las propiedades de una probabilidad: no están entre 0 y 1 ni suman 1.

## ¿Qué problema resuelve Softmax?
Convierte las puntuaciones del modelo en una distribución de probabilidad cuya suma es 1.

## ¿Por qué las probabilidades son más útiles que elegir directamente una palabra?
Una palabra nos da un resultado, una probabilidad no da el resultado y la certeza que se tiene.

## ¿Qué relación existe entre Softmax y la Loss Function?
Softmax convierte logits en probabilidades y La Loss Function utiliza esas probabilidades para calcular un número que representa el error del modelo.

## ¿Por qué un modelo que asigna un 99% a la respuesta correcta es mejor que otro que asigna un 30%, aunque ambos acierten?
Porque ambos aciertan, pero el modelo del 99 % está mucho más seguro de la respuesta correcta. Cross Entropy premia esa confianza cuando está justificada.

## Explica una analogía propia para Softmax.
En una posición de ajedrez se puede razonar sobre cual es la siguiente jugada, softmax da las probabilidades de cada una las jugadas posibles

## ¿Cómo se integra Softmax dentro del entrenamiento de un Transformer?
Softmax convierte los logits en probabilidades. Cross Entropy compara esas probabilidades con la distribución objetivo y calcula el error que utilizarán Backpropagation y Gradient Descent.