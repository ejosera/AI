# Proyect-00 - Resumen del Capitulo 1 de AI Engineering

Libro: *AI Engineering: Building Applications with Foundation Models*  
Autora: Chip Huyen  
Capitulo 1: *Introduction to Building AI Applications with Foundation Models*

---

# Idea principal

El primer capitulo explica por que ha nacido la disciplina de **AI Engineering**.

La idea central es que, desde 2020, la IA ha cambiado principalmente por una razon: **escala**. Los modelos son mas grandes, se entrenan con mas datos, requieren mas computo y tienen capacidades mucho mas generales que los modelos tradicionales.

Antes, construir una aplicacion de IA exigia normalmente crear, entrenar y operar modelos propios. Ahora, gracias a los **foundation models** disponibles como servicio, muchos equipos pueden construir aplicaciones de IA sin empezar desde cero.

Esto reduce la barrera de entrada y desplaza parte del trabajo desde el entrenamiento del modelo hacia el diseno de aplicaciones, prompts, evaluacion, integracion, experiencia de usuario y operacion del sistema.

---

# De modelos de lenguaje a foundation models

El capitulo empieza explicando los **language models**.

Un modelo de lenguaje aprende patrones estadisticos del lenguaje. Su tarea basica es predecir tokens: palabras, partes de palabras o caracteres, segun el tokenizador del modelo.

Hay dos tipos importantes:

* **Masked language models**: predicen tokens ocultos usando contexto anterior y posterior. Son utiles para tareas de comprension, clasificacion o analisis.
* **Autoregressive language models**: predicen el siguiente token usando solo el contexto previo. Son la base principal de muchos modelos generativos actuales.

La clave que permitio escalar estos modelos fue la **self-supervision**. En lugar de depender de datos etiquetados manualmente, el propio texto sirve como fuente de entrenamiento: el contexto funciona como entrada y el siguiente token funciona como etiqueta.

Esto permite entrenar modelos con enormes cantidades de datos, algo que seria inviable si cada ejemplo tuviera que etiquetarse a mano.

Los modelos de lenguaje crecieron hasta convertirse en **large language models**. Despues, al incorporar otros tipos de datos como imagenes, audio, video o codigo, evolucionaron hacia **foundation models**.

Un foundation model es un modelo general que puede servir como base para muchas aplicaciones diferentes.

---

# Que es AI Engineering

AI Engineering es el proceso de construir aplicaciones sobre modelos ya disponibles, especialmente foundation models.

No sustituye por completo al Machine Learning Engineering, pero cambia el centro de gravedad.

En el ML tradicional, gran parte del esfuerzo estaba en:

* Recolectar datos.
* Etiquetar datos.
* Entrenar modelos.
* Optimizar arquitecturas.
* Desplegar modelos propios.

En AI Engineering, gran parte del esfuerzo pasa a estar en:

* Elegir el modelo adecuado.
* Disenar prompts y flujos de interaccion.
* Conectar el modelo con datos, herramientas y APIs.
* Evaluar la calidad de las respuestas.
* Controlar coste, latencia y seguridad.
* Crear una experiencia de usuario util.
* Mantener el sistema en produccion.

El ingeniero de IA se parece mas a una mezcla entre ingeniero de software, ML engineer, product engineer y arquitecto de sistemas.

---

# Casos de uso de foundation models

El capitulo revisa varias areas donde los foundation models ya estan creando valor.

## Programacion

La generacion y asistencia de codigo es uno de los casos mas claros. Los modelos pueden autocompletar codigo, explicar errores, generar tests, ayudar con refactorizaciones y acelerar tareas repetitivas.

Esto no elimina la necesidad de entender programacion. Al contrario, exige saber revisar, validar y dirigir al modelo.

## Imagen y video

Los modelos generativos permiten crear, editar y transformar imagenes o videos. Esto afecta a diseno, marketing, videojuegos, publicidad, contenido visual y prototipado.

## Escritura

Los modelos pueden ayudar a redactar, resumir, traducir, corregir estilo, generar ideas y adaptar mensajes a distintos publicos.

El valor esta menos en reemplazar al autor y mas en acelerar partes del proceso creativo o tecnico.

## Educacion

La IA puede actuar como tutor personalizado, explicar conceptos de varias formas, generar ejercicios y adaptarse al nivel del estudiante.

El riesgo es que el estudiante use la IA para saltarse el aprendizaje en vez de profundizarlo.

## Bots conversacionales

Los chatbots son una interfaz natural para muchas aplicaciones porque permiten interactuar usando lenguaje comun.

Pero una buena aplicacion conversacional no consiste solo en conectar un modelo a una caja de texto. Necesita contexto, memoria, herramientas, control de errores, evaluacion y diseno de experiencia.

## Agregacion de informacion

Los foundation models son utiles para buscar, resumir, comparar y sintetizar informacion dispersa.

Este patron es especialmente importante para soluciones empresariales, soporte, troubleshooting, documentacion y asistentes internos.

## Organizacion de datos

Los modelos pueden extraer informacion, clasificar documentos, normalizar datos, etiquetar contenido y convertir informacion no estructurada en formatos mas utiles.

## Automatizacion de flujos de trabajo

La IA puede integrarse en procesos existentes para reducir tareas manuales: analisis, redaccion, soporte, busqueda, aprobaciones, operaciones y generacion de reportes.

---

# Antes de construir: evaluar si merece la pena

Una parte importante del capitulo es la pregunta: **deberiamos construir esta aplicacion de IA?**

No todo problema necesita IA. Antes de construir, hay que evaluar:

* Si el modelo realmente mejora el proceso.
* Que papel tendra la IA y que papel tendra el humano.
* Que nivel de error es aceptable.
* Como se medira la calidad.
* Que coste tendra operar el sistema.
* Que riesgos hay en seguridad, privacidad o cumplimiento.
* Si el producto sera defendible o facil de copiar.

La autora insiste en que muchas aplicaciones de IA parecen faciles de prototipar, pero dificiles de convertir en productos robustos.

Un demo puede funcionar con ejemplos cuidadosamente elegidos. Un sistema real debe funcionar con entradas ambiguas, usuarios impredecibles, cambios de modelo, fallos externos y restricciones de negocio.

---

# Expectativas, hitos y mantenimiento

El capitulo recomienda tratar las aplicaciones de IA como sistemas que evolucionan.

Es importante definir hitos realistas:

* Primero demostrar que el caso de uso tiene valor.
* Despues medir si el sistema funciona de forma consistente.
* Luego mejorar calidad, coste, latencia y seguridad.
* Finalmente integrarlo en flujos reales de usuario o negocio.

El mantenimiento es critico porque los sistemas basados en foundation models cambian con facilidad:

* Los modelos pueden actualizarse.
* Los prompts pueden dejar de funcionar igual.
* Los datos cambian.
* Los usuarios encuentran casos limite.
* Los costes pueden crecer.
* Las dependencias externas pueden variar.

Por eso, evaluar y monitorizar no es opcional.

---

# El nuevo stack de AI Engineering

El capitulo presenta el stack de AI Engineering como una combinacion de varias capas.

## Capa de modelo

Incluye modelos propietarios, modelos open source, APIs de modelos, hosting, inferencia y optimizacion.

En AI Engineering muchas veces no se empieza entrenando un modelo. Se empieza usando uno existente y se decide despues si hace falta fine-tuning, RAG, datos propios o un modelo especializado.

## Capa de aplicacion

Incluye prompts, orquestacion, herramientas, recuperacion de informacion, APIs, memoria, agentes, evaluacion y logica de producto.

Esta capa es donde vive gran parte del valor practico.

## Capa de producto e interfaz

Incluye chat, aplicaciones web, extensiones, integraciones en herramientas existentes, interfaces de voz o experiencias embebidas.

La interfaz importa mucho porque determina como el usuario comunica su intencion, recibe resultados, corrige errores y aporta feedback.

---

# AI Engineering vs ML Engineering

AI Engineering hereda muchas ideas del ML Engineering, pero cambia prioridades.

En ML Engineering tradicional, el modelo solia ser el centro del proyecto. Habia que entrenarlo, ajustarlo, desplegarlo y mantenerlo.

En AI Engineering, el modelo muchas veces es una dependencia externa o una pieza reutilizable. El reto esta en construir un sistema completo alrededor de el.

Diferencias importantes:

* El prototipo puede construirse mucho mas rapido.
* La evaluacion se vuelve mas dificil porque las salidas son abiertas.
* Prompt engineering aparece como una nueva disciplina practica.
* La experiencia de usuario gana importancia.
* La integracion con datos y herramientas es clave.
* El producto puede empezar antes de tener datos propios o modelos propios.

---

# AI Engineering vs Full-Stack Engineering

La autora tambien compara AI Engineering con Full-Stack Engineering.

Como ahora los modelos estan disponibles mediante APIs, los ingenieros full-stack pueden construir prototipos de IA rapidamente. Esto acerca el desarrollo de IA al desarrollo de producto.

La ventaja del perfil full-stack es que puede convertir una idea en una aplicacion usable, probarla con usuarios y obtener feedback rapido.

La ventaja del perfil ML es que entiende mejor los limites, evaluacion, datos, modelos y comportamiento probabilistico.

El perfil ideal combina ambas cosas: capacidad de construir producto y criterio tecnico sobre IA.

---

# Conceptos clave del capitulo

* **Escala**: factor principal que explica el salto reciente en capacidades de IA.
* **Token**: unidad basica procesada por un modelo de lenguaje.
* **Tokenizacion**: proceso de convertir texto en tokens.
* **Language model**: modelo que aprende patrones del lenguaje y predice tokens.
* **Self-supervision**: entrenamiento donde las etiquetas se derivan de los propios datos.
* **Large language model**: modelo de lenguaje escalado en datos, parametros y computo.
* **Foundation model**: modelo general que sirve como base para muchas aplicaciones.
* **AI Engineering**: disciplina de construir aplicaciones sobre foundation models.
* **Prompt engineering**: diseno de instrucciones y contexto para guiar el comportamiento del modelo.
* **Evaluation**: medicion sistematica de calidad, seguridad, utilidad y comportamiento.
* **AI stack**: conjunto de modelos, herramientas, datos, evaluacion, interfaz y producto.

---

# Conclusiones para mi roadmap

Este capitulo conecta directamente con el objetivo de convertirme en Azure AI Solutions Architect.

Lo importante no es solo aprender a llamar a un modelo desde una API. El objetivo real es aprender a disenar sistemas completos de IA:

* Con una arquitectura clara.
* Con datos bien integrados.
* Con evaluacion y monitorizacion.
* Con seguridad y gobierno.
* Con una experiencia de usuario util.
* Con criterios para decidir cuando usar IA y cuando no.

La leccion mas importante es que AI Engineering no consiste en "usar ChatGPT dentro de una app". Consiste en construir sistemas fiables alrededor de modelos probabilisticos.

Para proyectos como AzureSherlock, RTPA Dashboard, NSG Ninja AI o Azure Operations Copilot, esto significa que deberemos pensar siempre en:

* Que problema exacto resuelve la IA.
* Que informacion necesita el modelo.
* Como se validan sus respuestas.
* Que acciones puede ejecutar.
* Donde debe intervenir un humano.
* Como se mide si la solucion mejora el trabajo real.

---

# Resumen corto

El capitulo 1 presenta AI Engineering como una nueva disciplina impulsada por foundation models. Gracias a modelos grandes disponibles como servicio, construir aplicaciones de IA es mas accesible que antes, pero tambien aparecen nuevos retos: evaluacion, prompts, integracion, coste, latencia, seguridad, producto y mantenimiento.

La idea clave es que el valor ya no esta solo en entrenar modelos, sino en construir sistemas utiles, robustos y bien integrados alrededor de ellos.
