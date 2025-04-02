# Kaggle Generative AI Intensive - Sesión Día 1: Modelos Fundacionales y Prompt Engineering (Resumen Híbrido)

## Bienvenida e Introducción (Presentador Inicial)

* Bienvenidos a la nueva edición del curso intensivo de IA Generativa de Kaggle.
* Más de un cuarto de millón de desarrolladores conectados para aprender sobre:
    * APIs de Gemini
    * AI Studio
    * Vertex AI
    * Otras funcionalidades de IA de Google Cloud.

## Mensaje de Jeff Dean (Chief Scientist, Google)

* **Ponente:** Jeff Dean.
* **Puntos Clave:**
    * Entusiasmo por la participación en el curso.
    * Comparación con el año anterior: 150,000 desarrolladores vs. más de 200,000 este año.
    * Gran potencial de los modelos generativos para crear utilidades, entretenimiento y transformar información entre modalidades.
    * Las capacidades de los modelos aumentan rápidamente, ofreciendo a los desarrolladores bloques de construcción más sofisticados para crear cosas interesantes.
    * El objetivo del curso es enseñar a usar estas herramientas y ver qué crean los participantes.

## Descripción General del Curso Intensivo (Presentador Inicial)

* **Duración:** 5 días.
* **Organizado por:** Kaggle.
* **Componentes:**
    * Tareas diarias (assignments).
    * Discusión en Discord.
    * Livestreams / Sesiones "Ask Me Anything" (AMA) como esta.
* **Temas Cubiertos durante los 5 días:**
    * Modelos Fundacionales (Día 1).
    * Embeddings y Bases de Datos Vectoriales (Día 2).
    * Agentes (Día 3).
    * Modelos Específicos de Dominio.
* **Enfoque del Día 1:** Modelos Fundacionales y Prompt Engineering.
* **Actividades del Día 1:**
    * Escuchar el episodio resumen del podcast (creado con NotebookLM).
    * Leer los whitepapers correspondientes.
    * Completar el code lab de Kaggle (Anant hará una demostración).

## Agradecimiento a los Moderadores

* Un gran agradecimiento al equipo de moderadores por su trabajo respondiendo preguntas en Discord y ayudando a seleccionar preguntas para la sesión de Q&A.

## Sesión de Preguntas y Respuestas (Q&A) con Expertos

### Participantes Expertos:

* Logan Kilpatrick
* Warren Barkley
* Kieran Melan
* Arena Ziggler
* Matt Boso

---

### Pregunta 1: AI Studio

> **Pregunta:** Háblennos un poco sobre AI Studio. ¿Qué capacidades desbloquea para los desarrolladores y cómo cierra la brecha entre la investigación más reciente de Google DeepMind y las herramientas de Google Cloud?

* **Respuesta (Logan K.):**
    * AI Studio está diseñado para ser la vía rápida para acceder a los últimos modelos Gemini y de IA generativa de Google/DeepMind.
    * Es ideal para desarrolladores que quieren probar rápidamente si una idea es factible con los modelos Gemini.
    * Permite obtener código (Python, JavaScript, etc.) con un solo clic para empezar a construir la idea.
    * También facilita obtener una clave API para empezar a usar la API rápidamente.
    * Acelera el proceso desde la idea hasta la construcción con Gemini.
* **Respuesta (Matt B.):**
    * A menudo se pregunta por qué existen AI Studio y Vertex AI. Vertex es una plataforma MLOps empresarial completa (con Model Garden, etc.), mientras que AI Studio es una experiencia mucho más simple para empezar rápidamente con los modelos de Google.
    * Se busca una experiencia de desarrollador unificada (SDKs unificados) para que no tengas que reescribir código si pasas de AI Studio a Vertex AI.
    * Hay valor en tener ambos productos para diferentes casos de uso (inicio rápido vs. empresa).
* **Recurso:** Se puede probar en [ai.google.dev](https://ai.google.dev/).

---

### Pregunta 2: Evolución del Prompt Engineering

> **Pregunta:** ¿Cómo ha evolucionado el prompt engineering desde los primeros días de los LLMs (ej. PaLM 2, GPT-3)? ¿Cómo creen que evolucionará, especialmente con el auge de los modelos multimodales?

* **Respuesta (Kieran M.):**
    * Los primeros LLMs no estaban diseñados específicamente para las tareas actuales; eran modelos probabilísticos para predecir el siguiente token.
    * Las técnicas iniciales (Chain of Thought, Few-shot prompting, Personas) fueron más "descubiertas" mediante prueba y error que diseñadas.
    * En paralelo, se ha trabajado mucho en el "instruction tuning" (enseñar a los modelos cómo comportarse) para hacerlos más intuitivos y fáciles de usar.
    * El futuro apunta a técnicas más "diseñadas" e intencionales.
    * **Para usuarios finales (ej. App Gemini):** El objetivo es que no se requiera prompt engineering. El modelo debería entender peticiones razonables o pedir clarificación.
    * **Para desarrolladores:** El objetivo es simplificar el proceso. Que Gemini pida clarificaciones durante el desarrollo, no en producción. Emergerán patrones de diseño (como en la programación tradicional) para construir aplicaciones con LLMs.
    * **Multimodalidad:** Las técnicas de prompting no deberían cambiar fundamentalmente. Aún estamos en etapas tempranas. Ejemplo: Al usar Gemini por voz, las prompts son menos "perfectas" (con "ums", correcciones) pero el rendimiento sigue siendo impresionantemente coherente.

---

### Pregunta 3: Tendencias en Vertex AI y Enterprise AI

> **Pregunta:** Vertex AI evoluciona rápidamente. Mirando hacia adelante, ¿cuáles son las tendencias clave emergentes en IA empresarial que más les entusiasman y cómo se posiciona Vertex AI para ayudar a las empresas a aprovecharlas?

* **Respuesta (Warren B.):**
    * Hemos pasado de la simple automatización de procesos y extracción de datos no estructurados a capacidades más profundas de **comprensión y razonamiento**.
    * Los modelos más recientes, especialmente con frameworks agénticos, pueden realizar tareas tipo "investigación profunda".
    * Ejemplo: Un agente que, al no tener la información más reciente, usa una herramienta para buscar en la web y traer esa información al análisis.
    * Esto facilita análisis comparativos y profundos que antes eran difíciles. Vertex AI está enfocado en habilitar estas capacidades avanzadas para empresas.
    * Las empresas están yendo más allá de la simple búsqueda y comprensión de datos no estructurados.
* **Respuesta (Arena Z.):** (Implícito en la conversación posterior) La evaluación de estos flujos agénticos complejos es un área clave en la que las empresas están pensando y Vertex AI está trabajando.

---

### Pregunta 4: Futuro de los Modelos Fundacionales (1-3 años)

> **Pregunta (Para todos):** Mirando a 1-3 años, ¿qué tarea o capacidad específica creen que los modelos fundacionales desbloquearán que hoy parece difícil o imposible? A la inversa, ¿qué limitaciones inherentes creen que persistirán? (Respuestas breves)

* **Respuesta (Matt B.):** La forma en que construimos y usamos software cambiará radicalmente, de maneras que aún no imaginamos. (3 años en IA son como 100 años humanos).
* **Respuesta (Logan K.):** La generación de código y la ingeniería de software seguirán avanzando. **Limitación:** Los modelos seguirán siendo deficientes si no se les da suficiente contexto. No harán milagros con preguntas básicas sin información. Quizás aprendan a pedir más contexto.
* **Respuesta (Arena Z.):** En evaluación (evals), habrá menos problemas para automatizar flujos, pero **limitación:** seguirá siendo crucial proporcionar al modelo los criterios de evaluación y lo que se considera "bueno". El modelo no puede adivinarlo.
* **Respuesta (Kieran M.):** Espero que el "prompt engineering" como lo conocemos hoy sea cosa del pasado. **Limitación:** Los modelos nunca leerán la mente. Los usuarios tendrán que ser más claros y específicos en sus intenciones.
* **Respuesta (Warren B.):** **Limitación:** La dificultad para las empresas (especialmente grandes) de moverse rápidamente y adaptarse al ritmo vertiginoso de la evolución de los modelos. Mantenerse al día y diseñar sistemas ágiles para adoptar lo último seguirá siendo un desafío.

---

### Pregunta 5 (Comunidad - donna.oie): Eficiencia Energética en IA

> **Pregunta:** ¿Cómo se pueden optimizar el diseño de sistemas de IA y el prompt engineering para mejorar la eficiencia energética, el rendimiento computacional (velocidad, precisión) y reducir el impacto ambiental, manteniendo la calidad del output?

* **Respuesta (Logan K.):**
    * **Caching de Prompts:** Algunas APIs ofrecen formas de cachear prompts para evitar recálculos.
    * **APIs Batch:** Permiten agrupar tareas y aprovechar cómputo inactivo, aplanando el uso y mejorando la eficiencia.
    * **Programación Consciente (Futuro):** Se podría imaginar un futuro donde las tareas batch se ejecuten preferentemente cuando los centros de datos usen energías renovables.
    * **Modelos más Pequeños:** (Añadido por el moderador) Usar modelos más pequeños y eficientes (como los modelos abiertos o versiones "flash") reduce la huella.
    * **Computación On-Device:** Ejecutar modelos en el dispositivo evita la comunicación con servidores.

---

### Pregunta 6 (Comunidad - Channing Ogden): Evaluación de "Judge Models" y Sesgo

> **Pregunta:** ¿Cómo se pueden seleccionar y personalizar eficientemente los "modelos jueces" (judge models) para minimizar el sesgo acumulado y los problemas de precisión, generando confianza sin depender únicamente de evaluaciones repetidas?

* **Respuesta (Arena Z.):**
    1.  **Buena Base:** Usar un modelo juez potente (estado del arte) y aplicar técnicas básicas para mitigar sesgos (ej. multi-sampling para no depender de una sola respuesta, invertir el orden en comparaciones pareadas para evitar sesgo posicional).
    2.  **Evaluar al Juez:** Tratar al juez como otra aplicación LLM. Realizar una evaluación (aunque sea pequeña) para verificar si su juicio se alinea con el de expertos humanos en *tus* datos específicos.
    3.  **Prompt Engineering para el Juez (Si hay desalineación):** Asegurarse de que los criterios de evaluación dados al juez sean claros y específicos. A menudo hay criterios implícitos que no se explicitan.
    4.  **Técnicas Avanzadas (Si el prompting no basta):**
        * Si el dataset es muy diverso, quizás se necesiten rúbricas por ítem en lugar de criterios universales.
        * Considerar fine-tuning del modelo juez si los datos son muy específicos (último recurso).

---

### Pregunta 7 (Comunidad - sarar42): Definición de Prompt Engineering

> **Pregunta:** ¿Escribir el prompt apropiadamente es prompt engineering, o configurar el número de tokens, temperatura, top-p es prompt engineering, o ambos? ¿Qué es exactamente?

* **Respuesta (Anant N.):**
    * El **Prompt** es la entrada al modelo (como las 'features' en ML tradicional).
    * Los **Parámetros de Generación/Decodificación** (temperatura, top-p, top-k, tokens máximos) operan a nivel de la salida, controlando cómo se seleccionan los tokens para optimizar la respuesta para una tarea dada, manteniendo la entrada fija.
* **Respuesta (Matt B.):** Prompt engineering es un poco un "arte". Implica experimentación (probar prompts, modelos, parámetros) hasta encontrar la configuración óptima para tu escenario. Es un proceso iterativo.
* **Respuesta (Kieran M.):** Independientemente del nombre (prompt engineering, LLM engineering), son todas las "perillas" que un desarrollador debe considerar y ajustar. Se espera que la necesidad de ajustar parámetros como la temperatura disminuya en el futuro a medida que los modelos mejoren, pero entender su efecto (ej. temperatura -> balance creatividad/predictibilidad) es clave hoy.
* **Recurso:** El whitepaper de Prompt Engineering tiene una sección sobre "Automated Prompt Engineering".

---

### Pregunta 8: Reducción de Alucinaciones en Gemini

> **Pregunta:** La alucinación es un gran desafío. Técnicas como RAG y prompt engineering ayudan, pero ¿cuáles son los métodos más efectivos que Google usa en Gemini para minimizar salidas incorrectas o engañosas? ¿Hay compensaciones entre reducir alucinaciones y la creatividad del modelo?

* **Respuesta (Kieran M.):**
    * Reducir alucinaciones (o mejorar la "factuality") es un área clave de enfoque.
    * **Dos Escenarios:**
        1.  **Respuesta Basada en Contexto Proporcionado:** (RAG, responder sobre documentos dados, Experiencia Generativa en Search). El modelo basa su respuesta en información que se le da. Es inherentemente más fácil de verificar y controlar.
        2.  **Respuesta Basada en Conocimiento Interno:** (Datos de entrenamiento, "memoria" del modelo). Más propenso a errores si el conocimiento es lejano o incorrecto.
    * **Estrategias Efectivas:**
        * **Grounding (Anclaje):** La mejor estrategia. Forzar al modelo a basar su respuesta en fuentes proporcionadas. Vertex AI ofrece "Search Grounding". Dar referencias verificables.
        * **Prompting Explícito:** Indicar en el prompt los requisitos de factuality.
        * **Pasos de Verificación Explícitos:** Añadir un paso donde el LLM (u otro sistema) verifica la respuesta contra criterios o fuentes. Se puede combinar con auto-corrección.
        * **Temperatura Baja:** Usar temperatura=0 para respuestas más determinísticas y menos propensas a "inventar".
    * **Trade-off Creatividad vs. Factuality:** Sí existe. Es difícil escribir un poema muy creativo que sea estrictamente factual. Ajustar la temperatura es clave: alta para creatividad (más probabilidad de tokens menos probables), baja para factuality. Hay que encontrar el balance adecuado para cada caso de uso.

---

## Resumen de Contenido y Code Labs (Presentado por Anant)

### Resumen de Whitepapers Día 1

* **Modelos Fundacionales:**
    * Arquitectura Transformer y mecanismo de atención.
    * Entrenamiento en grandes corpus, contexto largo.
    * Variaciones: Mixture of Experts (MoE) para eficiencia y calidad.
    * Evolución: De BERT/PaLM a Gemini, modelos abiertos. Impulsado por escala de datos y tamaño del modelo.
    * Fases de Entrenamiento: Pre-entrenamiento (general), Supervised Fine-Tuning (SFT) (seguir instrucciones), RLHF (alinear con preferencias humanas - utilidad, seguridad).
    * Adaptación Eficiente: Parameter-Efficient Fine-Tuning (PEFT) para ajustar modelos grandes de forma económica.
    * Optimización: Quantization, Distillation, Speculative Decoding para velocidad y eficiencia.
* **Prompt Engineering:**
    * Parámetros de generación (Temperatura, Top-P, Top-K): Balancear predictibilidad y creatividad.
    * Técnicas de Prompting: Zero-shot, Few-shot (con ejemplos).
    * Estructura del Prompt: Instrucciones de sistema, contexto, asignar un rol.
    * Problemas Complejos: Chain of Thought, Step-by-step prompting para razonamiento.
    * Evaluación: Uso de LLMs como jueces, mejores prácticas.

### Resumen de Code Lab 1: Introducción a Prompt Engineering con Gemini

* Uso básico de `Gemini 2.0 Flash`.
* Prompting simple (single-turn) vs. conversacional (multi-turn con historial).
* Selección de modelos (incluyendo modelos tuneados).
* Ajuste de Parámetros de Generación:
    * `max_output_tokens` (límite duro).
    * `temperature` (aleatoriedad).
    * `top_p`, `top_k` (restringir selección de tokens).
* Exploración de Técnicas de Prompting:
    * Zero-shot, One-shot, Few-shot.
    * Restringir salida a enumeraciones.
    * Modo JSON para salida estructurada.
    * Chain of Thought, ReAct.

### Resumen de Code Lab 2: Evaluación y Salida Estructurada

* **Evaluación con LLM como Juez:**
    * Configurar contexto (ej. un PDF técnico).
    * **Evaluación Puntual (Pointwise):** Crear un prompt detallado para que un LLM evalúe la respuesta de otro LLM según rúbricas específicas, dando una puntuación (1-5) y razonamiento.
    * **Evaluación por Pares (Pairwise):** Dar al LLM juez dos respuestas a un mismo prompt y pedirle que elija la mejor (más útil cuando la evaluación puntual resulta en empates).
    * **Generación Múltiple:** Generar varias respuestas del juez para asegurar que la puntuación no es por ruido/aleatoriedad.
* **Importancia:** Evaluar respuestas es crucial para tareas específicas.

---

## Pop Quiz

1.  **¿Qué configuración de Gemini controla el grado de aleatoriedad en la selección del siguiente token predicho?**
    * (a) Temperatura
    * (b) Top-K
    * (c) Top-P
    * (d) Output token count
    * **Respuesta Correcta: (a) Temperatura**

2.  **¿Cuál de las siguientes NO es una técnica usada para acelerar la inferencia en LLMs?**
    * (a) Quantization (Cuantización)
    * (b) Distillation (Destilación)
    * (c) Flash Attention
    * (d) Fine-tuning
    * **Respuesta Correcta: (d) Fine-tuning** (Fine-tuning adapta el modelo, no acelera directamente la inferencia)

3.  **¿Cuál de las siguientes es una característica única de la familia de modelos Gemini?**
    * (a) Fueron los primeros en introducir pre-entrenamiento no supervisado.
    * (b) Pueden soportar entradas multimodales.
    * (c) Son "decoder-only".
    * (d) Pueden soportar una ventana de contexto de hasta 2 millones de tokens.
    * **Respuesta Correcta: (d) Pueden soportar una ventana de contexto de hasta 2 millones de tokens.** (Nota: La multimodalidad nativa también fue una característica destacada en su lanzamiento inicial, pero la ventana de contexto larga es más distintiva frente a otros modelos en el momento de la transcripción).

4.  **¿Cómo mejora RLHF (Reinforcement Learning from Human Feedback) a los LLMs?**
    * (a) Entrenando el modelo en un dataset masivo de texto no etiquetado.
    * (b) Usando un modelo de recompensa para incentivar la generación de respuestas preferidas por humanos.
    * (c) Reduciendo el número de parámetros para inferencia más rápida.
    * (d) Convirtiendo el modelo en una red neuronal recurrente.
    * **Respuesta Correcta: (b) Usando un modelo de recompensa para incentivar la generación de respuestas preferidas por humanos.**

5.  **¿Qué técnica mejora las habilidades de razonamiento de un LLM al indicarle que produzca pasos de razonamiento intermedios?**
    * (a) Zero-shot prompting
    * (b) Step-back prompting
    * (c) Self-consistent prompting
    * (d) Chain of Thought prompting
    * **Respuesta Correcta: (d) Chain of Thought prompting**

6.  **(Bonus) ¿Cuál es la memoria GPU mínima necesaria para la inferencia en un modelo de 3 mil millones (3B) de parámetros usando precisión flotante estándar?**
    * (a) 3 GB
    * (b) 6 GB
    * (c) 12 GB
    * (d) 24 GB
    * **Respuesta Correcta: (c) 12 GB** (Regla general: ~4 bytes por parámetro para FP32, 3B * 4 bytes ≈ 12 GB).

---

## Recursos y Herramientas Mencionadas

* **Plataformas/APIs:**
    * Kaggle
    * Gemini APIs (incluyendo Gemini 2.0 Flash, modelos Pro)
    * AI Studio ([ai.google.dev](https://ai.google.dev/))
    * Vertex AI
    * Google Cloud
    * Discord (para la comunidad del curso)
    * NotebookLM (mencionado para crear el podcast resumen y para interactuar con whitepapers)
* **Modelos Mencionados/Implícitos:**
    * Familia Gemini (Flash, Pro, mencionada ventana de 2M tokens)
    * PaLM 2, GPT-3 (como ejemplos tempranos)
    * BERT (como ejemplo temprano)
    * Modelos Abiertos (mencionados en general)
* **Conceptos/Técnicas Clave:**
    * Modelos Fundacionales
    * Prompt Engineering
    * Multimodalidad
    * Embeddings / Bases de Datos Vectoriales (mencionados como temas futuros)
    * Agentes / Frameworks Agénticos (mencionados como tema futuro y en Q&A)
    * Arquitectura Transformer, Mecanismo de Atención, Mixture of Experts (MoE)
    * Fases de Entrenamiento: Pre-training, Supervised Fine-Tuning (SFT), RLHF
    * Parameter-Efficient Fine-Tuning (PEFT)
    * Parámetros de Generación: Temperatura, Top-P, Top-K, Max Output Tokens
    * Técnicas de Prompting: Zero-shot, Few-shot, Chain of Thought (CoT), Personas, Step-back, Self-consistency, ReAct, Modo JSON, Restringir salida a enumeraciones.
    * Grounding / Anclaje (RAG, Search Grounding)
    * Evaluación de LLMs: LLM-as-judge (Modelo Juez), Evaluación Puntual (Pointwise), Evaluación por Pares (Pairwise), Rúbricas, Multi-sampling, Sesgo Posicional.
    * Optimización de Inferencia: Quantization, Distillation, Speculative Decoding, Flash Attention, Caching de Prompts, APIs Batch.
    * Factuality / Reducción de Alucinaciones.
* **Recursos del Curso:**
    * Whitepapers (Modelos Fundacionales, Prompt Engineering, Automated Prompt Engineering)
    * Podcast Resumen Diario
    * Code Labs en Kaggle