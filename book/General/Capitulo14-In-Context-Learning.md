# ideas clave
El modelo podía aprender durante la conversación.
No ha cambiado ningún parámetro.

```
Prompt

↓

Tokens

↓

Attention

↓

Nueva representación contextual
```

Zero-Shot, One-Shot y Few-Shot
zero-shot: no se da ejemplos
one-shot: se da un ejemplo, es mas fácil para el modelo enterder el formato
Few-Shot: se proporcionan varios ejemplos para que el modelo deduzca mejor el patrón de la tarea.


Sin Attention... No existiría el In-Context Learning.

Durante la inferencia, un LLM no cambia sus parámetros. Cambia la forma en que utiliza esos parámetros gracias al contexto.

El In-Context Learning existe porque Attention reconstruye continuamente esa representación contextual usando el prompt actual.

## ¿Qué es el In-Context Learning?
Es la capacidad del modelo para adaptarse a una tarea utilizando únicamente el contexto, sin modificar sus parámetros.

## ¿Por qué fue una sorpresa para los investigadores?
Porque no se había diseñado esa capacidad

## ¿Qué diferencia hay entre aprender durante el entrenamiento y aprender en contexto?
Aprender durante el entrenamiento modifica los parámetros mientras que según en el contexto se basa en reconstruir la representación contextual.

## ¿Qué significan Zero-Shot, One-Shot y Few-Shot?
El número de ejemplos que se da en el contexto al modelo

## ¿Qué papel juega Attention en el In-Context Learning?
Attention selecciona qué información del contexto es relevante para resolver la tarea actual.

## ¿Por qué los parámetros no cambian durante una conversación?
Los parámetros son valores fijos de cada modelo. Una vez entrenado no cambian

## Explica una analogía propia para el In-Context Learning.
Oí una historia donde había unos chimpaces en un zoo. Se puso comida en lo alto de una cuerda y cada vez que uno de ellos intentaba trepar por la cuerda los cuidadores los reciaban con agua fria.
Cuando ya los chimpances no intentaban trepar por miedo al agua fueron cambiando un chimpance de la jaula por otro nuevo. Este inmediatemente intentaba trepas pero sus compañeros se lo impedian.
Al tiempo ya no quedó ningún chimpance que hab´ia sido mojado con agua fria pero los chimpances no intentaban trepar por la cuerda.

Estos nuevos chimpances habían aprendido algo por el comportamiento de sus compañeros anteriores

## ¿Cómo se relaciona este capítulo con Embeddings y Attention?
Attention utiliza los embeddings iniciales para construir una nueva representación contextual adaptada al prompt.