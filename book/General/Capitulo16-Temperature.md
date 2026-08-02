# idea clave
Temperature controla cuánto influye la probabilidad en la elección del siguiente token.
Temperature controla la diversidad de las respuestas.

¿Cuándo usar Temperature baja?
precisión y reproducibilidad.

Cuando quieres:
- código;
- matemáticas;
- configuraciones de Azure;
- contratos;
- documentación técnica.

¿Cuándo usar Temperature alta?
Aquí la creatividad tiene valor.

Cuando quieres:
- escribir una novela;
- generar ideas;
- hacer brainstorming;
- poesía;
- nombres para un proyecto.


```batch
Texto
↓

Transformer
↓

Logits
↓

Temperature
↓

Softmax

↓

Probabilidades
```

entre los logits y la selección del siguiente token.



## ¿Qué problema resuelve Temperature?
Permite que la elección del siguiente token tenga mas variedad

## ¿Qué ocurre cuando Temperature es muy baja?
Se busca una respuesta con la máxima probabilidad

## ¿Qué ocurre cuando es muy alta?
Se pueden dar respuestas con menor probabilidad

## ¿Por qué Temperature no modifica el conocimiento del modelo?
Temperature solo cambia la forma de elegir el siguiente token.


## ¿Qué tipos de tareas suelen beneficiarse de Temperature baja?
Tareas en las que se busca exactitud o predictibilidad

## ¿Qué tipos de tareas suelen beneficiarse de Temperature alta?
Tareas que buscan creatividad

## Explica una analogía propia para Temperature.
Es un poco cogido por los pelos, pero a mas alcohol el comportamiento es mas impredecible y a menos alcohol mas predecible.

## ¿Cómo se relaciona Temperature con Softmax y las probabilidades?
Temperature modifica la distribución de probabilidades generada a partir de los logits. Una temperatura baja concentra la probabilidad en los tokens más probables; una temperatura alta reparte más la probabilidad entre distintas opciones.