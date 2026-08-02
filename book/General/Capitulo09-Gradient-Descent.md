# Idea clave
Backpropagation calcula las pendientes; Gradient Descent decide cómo moverse usando esas pendientes. O dicho de otra forma Backpropagation dice hacia dónde mirar. Gradient Descent dice cuánto caminar.


El learning rate, η, es el tamaño del paso que damos al modificar los parámetros.

Nuevo parámetro = Parámetro actual - Learning Rate × Derivada del error

## ¿Qué problema resuelve Gradient Descent?
Gradient Descent resuelve el problema de cómo modificar los parámetros para reducir progresivamente el error del modelo.

## ¿Qué representa la montaña en la analogía?
La altura de la  montaña simboliza la cantidad de error. A mayor altura mas error.

# ¿Qué representan las coordenadas de un punto de la montaña?
Cada punto de la montaña representa un conjunto completo de parámetros del modelo.

## ¿Qué información aporta la derivada?
La derivada indica cómo cambia el error cuando modificamos ligeramente un parámetro.

## ¿Qué ocurre si el Learning Rate es demasiado grande?
Hace que un proceso sea muy rápido pero puede saltarse mínimos.
Por ejemplo un valle de forma de V maýuścula y estamos en uno de los puntos superiores.
Si el learning rate es muy alto acabaremos en el otro punto superior y luego volveremos al inicial. Nunca descenderemos al valle

## ¿Qué ocurre si es demasiado pequeño?
El proceso de minimizar el error puede tardar mucho. Además si la curva es como la siguiente podemos quedarnos atascados en el primer minimo y no llegar al segundo
```
\
 \
   \/\
      \/
```

## Explica con una analogía qué hace Gradient Descent.
No sé si es muy buena analogía pero en un átomo estamos en una capa exterior de la nube de electrones y queremos ir a la de mínima energia. si el gradien descent es muy pequeño podemos tardar mucho en llegar a la capa de mínima energia o incluso nunca llegar si el santo entre capa y capa es demasiado largo. Por otra parte si el gradient es muy grande nos podemos pasar la capa de mínima energia


## ¿Cuál es la diferencia entre Backpropagation y Gradient Descent?
Backpropagation calcula cómo afecta cada parámetro al error. Gradient Descent utiliza esa información para actualizar los parámetros.


## Conexiones con capítulos anteriores
El backpropagation y gradient descent nos van a ayudar a encontrar los parámetros que menor error den
Los parámetros que modifica Gradient Descent son exactamente los mismos parámetros que aprendimos en el capítulo anterior.
