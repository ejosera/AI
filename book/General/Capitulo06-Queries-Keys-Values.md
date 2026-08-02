Cada embedding se transforma mediante tres matrices (WQ, WK y WV) para generar una Query, una Key y un Value.
- Query (Q)
- Key (K)
- Value (V)

token: banco
Q: necesito contexto. Banco de financiero o de parque?
La Query representa el tipo de información que esa palabra necesita del resto del contexto.

Key: Qué información puedo aportr?
token: dinero
Key: Tengo información relacionado con finanzas

Value: Qué información entregaré si alguien me presta atención?
```
                 Query

      ¿Qué necesito encontrar?

                  │

                  ▼

          Comparar con todas

              las Keys

                  │

                  ▼

      ¿Quién se parece más?

                  │

                  ▼

      Leer sus Values

                  │

                  ▼

      Construir nueva representación
```

Ejemplo
Ingresé dinero en el banco
Q: Busco información económica
K: Busco el key adecuado
    Key                 Value
    ingresé             movimiento económico
    dinero              finanzas
    banco               ambigua
    parque              naturaleza   

Atención da mas peso a ingresé y dinero
Query y Key calculan el peso a dar a cada palabra.
La información viene de los values

```
Texto

↓

Tokens

↓

Embeddings transformaciónes WQ, WK y WV

↓

Q K V

↓

Comparar Q con K

↓

Pesos

↓

Combinar Values

↓

Nueva representación

↓

Siguiente capa
```


## ¿Qué función tiene una Query?
Una query es el objeto que queremos obtener

## ¿Qué función tiene una Key?
La Key describe qué tipo de información ofrece una palabra para que otras puedan decidir si les resulta útil.

## ¿Qué función tiene un Value?
Aporta la información que se combinará para construir la nueva representación.

## ¿Por qué se necesitan los tres?
Query y Key se usan para dar mayor o menor peso a las palabras
Value se usa para modificar la representación del "embedding" 

## Explica con una analogía propia cómo funciona el mecanismo QKV.
Q: Busco información de "cabo" 
K: Busco palabras con relación con cabo

Q + K asignan pesos

V devuelve información según los pesos dados para crear la nueva representación del embedding

## ¿Cómo se conecta este capítulo con embeddings y Attention?
Es el mecanismos por el que attentión crea una nueva representación del embedding

## ¿Por qué el modelo no necesita reglas escritas por un humano para decidir dónde prestar atención?
El modelo crea el embedding que a su vez genera KQV

## Qué ocurre realmente
El embedding inicial no cambia directamente.

Primero se transforma en Query, Key y Value.

Después Query y Key calculan cuánto debe influir cada palabra.

Finalmente los Values se combinan usando esos pesos para crear una representación contextual nueva.