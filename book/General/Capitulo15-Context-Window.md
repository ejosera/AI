## ideas clave
La Context Window es la cantidad máxima de tokens que el modelo puede considerar simultáneamente durante una inferencia.

Dependiendo del sistema, las partes más antiguas pueden dejar de estar disponibles o resumirse.

La Context Window no determina lo que el modelo sabe. Determina la cantidad de información que puede utilizar al mismo tiempo.

## ¿Por qué importa tanto?
que Attention compara los tokens entre sí.
Si un token queda fuera de la ventana...
Attention ya no puede relacionarlo con los nuevos.

## ¿Qué es la Context Window?
La Context Window es el número máximo de tokens sobre los que Attention puede operar simultáneamente durante una inferencia.

## ¿Por qué se mide en tokens y no en palabras?
Porque attention trabaja con tokens, uno de los primeros pasos es convertir palabras en tokens

## ¿Qué ocurre cuando una conversación supera la Context Window?
Que hay cierta información del contexto no disponible para attention de forma directa. Hay modelos que puede hacer resumenes

## ¿Qué relación existe entre Context Window y Attention?
Context windows limita la cantidad de tokens con los que attention puede trabajar.

## ¿Por qué una ventana más grande mejora muchas tareas?
Porque permite a attention tener acceso a mas tokens para la representación
Permite relacionar información que está más separada dentro del documento o conversación.

## ¿Por qué no podemos aumentar la Context Window indefinidamente?
Porque aumenta cuadraticamente los recursos necesarios

## Explica una analogía propia para la Context Window.
Es como la capacidad de atención o mejor memoria de trabajo de alguien. Una persona con poca capacidad de atencion no podrá recordad el hilo de la conversación de hace un rato.

## ¿Cómo se relaciona este capítulo con In-Context Learning?
Una ventana mayor permite proporcionar más contexto y más ejemplos, lo que puede mejorar el In-Context Learning.