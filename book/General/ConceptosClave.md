# Conceptos clave
## Que es un embedding
Un embedding no es un diccionario de significados.
Los conceptos cercanos aparecen próximos en el espacio vectorial.
El contexto influye en la representación final de un concepto.
La búsqueda semántica funciona gracias a los embeddings.

## funcionamiento
Frase: [Ingresé] [dinero] [en] [el] [banco]

Cada palabra tiene un embedding inicial
Ingresé  → E1
Dinero   → E2
En       → E3
El       → E4
Banco    → E5

Cada embeding genera un KQV
Q1 K1 V1
Q2 K2 V2
...
Q5 K5 V5

Contruyo la nueva representación de banco
Su Query (Q5) compara con todas las Keys.
```
Q5

↓

K1 → peso 0.30
K2 → peso 0.50
K3 → peso 0.05
K4 → peso 0.02
K5 → peso 0.13
```

Attention crea la nueva representación
```
Nueva representación de "banco"
=
0.30 · V1
+
0.50 · V2
+
0.05 · V3
+
0.02 · V4
+
0.13 · V5
```