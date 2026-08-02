# idea clave
Una Loss Function dcnvierte una predicción en un número.
Ese número será el que Gradient Descent intentará minimizar.
Backpropagation no intenta minimizar el número de errores. Intenta minimizar la función de pérdida.

```bash
Forward Pass

↓

Predicción

↓

Loss Function

↓

Número

↓

Backpropagation

↓

Gradient Descent
```

## ¿Qué problema resuelve una Loss Function?
Cuantificar el error de la predicción

## ¿Por qué no basta con saber si una respuesta es correcta o incorrecta?
Si manejamos información binaria (verdadero o falso) sabemos si hemos acertado o no. Pero si somos capaces de medir el error, podemos saber lo cerca que estamos del valor real.

## ¿Qué información produce una Loss Function?
Produce un valor numérico que cuantifica el error entre la predicción y el objetivo.

## ¿Por qué existen distintas funciones de pérdida?
Porque no todos los problemas son iguales. Predecir una temperatura, clasificar una imagen o generar texto requieren formas diferentes de medir el error.

## ¿Qué papel juega la Loss Function en el entrenamiento?
La Loss Function genera el error que Backpropagation utilizará para calcular las derivadas y que Gradient Descent intentará minimizar.

## Explica una analogía propia para una Loss Function.
Es como la retroalimentación negativa en sistemas electrónicos, bueno no realmente pero en el sentido que  cuantifico el valor real y el obtenido y eso me puede ayuda a mejorar mis parametros via backpropagation y gradient desent

## ¿Cómo se relacionan Forward Pass, Loss Function, Backpropagation y Gradient Descent?
1. Forward Pass utiliza los parámetros actuales para generar una predicción.
2. La Loss Function calcula el error de esa predicción.
3. Backpropagation calcula cómo ha contribuido cada parámetro a ese error.
4. Gradient Descent actualiza los parámetros para intentar reducir el error.
