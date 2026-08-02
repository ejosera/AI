# idea clave
Forward Pass → produce una predicción.

Backpropagation → calcula cuánto ha contribuido cada parámetro al error.

Gradient Descent → actualiza los parámetros usando esa información.

Repetir millones de veces.


forward pass
```
Texto
↓
Embeddings
↓
Attention
↓
Heads
↓
Predicción
↓
Error
```

backpropagation
```
Error
↑
Predicción
↑
Heads
↑
Attention
↑
Embeddings
```


## ¿Qué problema resuelve Backpropagation?
PPermite calcular eficientemente cómo afecta cada parámetro al error reutilizando cálculos entre capas consecutivas.

## ¿Por qué sería inviable calcular una derivada independiente para cada parámetro?
Tendría un gran coste de tiempo y calculo

## ¿Qué es el Forward Pass?
Es el recorrido hacia delante de la red para obtener una predicción. Al comparar esa predicción con el valor real se calcula el error.

## ¿Qué es el Backward Pass?
Es el proceso para averiguar la contribución de cada parámetro al error.

## ¿Qué información viaja durante el Backward Pass?
Durante el Backward Pass viaja el gradiente (la información sobre cómo cambia el error). Cada capa utiliza ese gradiente y lo transforma antes de enviarlo a la capa anterior.

## ¿Qué papel juega la regla de la cadena?
Permite dividir un calculo complejo en muchos mas fáciles

## Explica Backpropagation usando una analogía propia.
En una cadena de montaje. Se mide el error del producto final (forward pass) y luego se va de atras adelante para ver que puesto produce mas error

## ¿Cómo trabajan juntos Forward Pass, Backpropagation y Gradient Descent?
Forward Pass

↓

Obtiene una predicción

↓

Calculamos el error

↓

Backpropagation calcula las derivadas

↓

Gradient Descent actualiza los parámetros

↓

Nuevo Forward Pass

↓

...