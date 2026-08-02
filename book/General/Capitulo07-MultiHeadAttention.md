```
                 Embedding

                     │

      ┌──────────────┼──────────────┐

      │              │              │

    Head1         Head2         Head3

      │              │              │

  Attention     Attention     Attention

      │              │              │

      └──────────────┼──────────────┘

                     │

            Concatenar resultados

                     │

             Transformación final

                     │

          Nueva representación
```
cada Head termina especializándose espontáneamente durante el entrenamiento.
Head 1 = gramática
Head 2 = nombres propios
Head 3 = emociones

## ¿Qué problema intenta resolver Multi-Head Attention?
Multi-Head Attention permite que varias atenciones trabajen en paralelo, especializándose de forma espontánea en distintos tipos de relaciones del lenguaje.

## ¿Por qué una única Attention puede no ser suficiente?
Porque una frase puede contener simultáneamente relaciones gramaticales, semánticas, temporales, causales, etc., y una única Attention puede tener dificultades para captarlas todas a la vez.

# ¿Qué ventaja aporta tener varias Heads trabajando en paralelo?
Permite capturar distintos tipos de relaciones al mismo tiempo, generando una representación contextual más rica.

# ¿Cómo se combinan los resultados de las distintas Heads?
Se concatenan en un único vector

# ¿Quién decide en qué se especializa cada Head?
No se decide. Se autoespecializan ellos mismo durante el aprendizaje

# Explica una analogía propia que represente Multi-Head Attention.
Son como un grupo de amigos que juegan al baloncesto. Nadie les asigna una posición al principio, pero con el tiempo cada uno descubre en qué es mejor: uno termina siendo base, otro pívot y otro escolta. Juntos forman un equipo mucho más eficaz que si todos intentaran hacer exactamente lo mismo.

## Idea clave
Una única forma de observar una frase no suele ser suficiente. Multi-Head Attention utiliza varias perspectivas simultáneamente para construir una representación contextual más completa.