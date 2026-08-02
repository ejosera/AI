# ¿Cómo puede un modelo que solo predice el siguiente token parecer inteligente?
Para predecir bien el lenguaje, el modelo termina aprendiendo una representación del mundo. Son modelos que han aprendido representaciones extremadamente ricas del lenguaje y del conocimiento.   

# ¿Por qué un modelo que solo predice el siguiente token necesita aprender tanto sobre el mundo?
Para predecir el siguiente token hace falta todo un contexto del tema en cuestión. Este contexto no solo son datos, sino sus relaciones, las jerarquiás, las dependencias. Hace falta toda una estructura complementaria a los datos para "dar sentido" y poder predecir el token siguiente.

# ¿Qué diferencia existe entre memorizar un texto y construir una representación interna del conocimiento?
Memorizar un texto es básicamente guardar datos. Una representación interna es poder construir un modelo interno que permita inferir información nueva.

## ¿Qué papel juega el contexto en un LLM?
Un LLM es mas que nada el modelo que permite acceder por ejemplo a un texto pero además con sus relaciones con otros elementos. Con la información del texto en si mismo, el contexto que le hayan dado y toda la estructura del modelo sobre jerarquía de datos, relaciones, etc. El LLM estima una distribución de probabilidad sobre todos los posibles tokens siguientes y, a partir de esa distribución, selecciona uno siguiendo una determinada estrategia (por ejemplo, el más probable o uno suficientemente probable).

# ¿Crees que la predicción puede dar lugar a comportamientos que parezcan razonamiento? ¿Por qué?
Por supuesto que se puede. Tanto la inteligencia artificiál como la natural, ambas obtienen un punto de partida a partir de texto y su contexto y basandose en todas las reglas que han aprendidd producen "razonamiento". He puesto razonamiento entre comillas porque no hay 100% de conocimiento como funciona el cerebro humano pudiendo ser que ambas inteligencia trabajen de formas similares o no.

# ¿Qué implicaciones tiene esto para diseñar aplicaciones sobre Azure OpenAI?
Para trabajar con Azure OpenAI hay que tener basarse mas en un buen contexto que en la confianza de la IA en su razonamiento