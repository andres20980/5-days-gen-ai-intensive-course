Introducción y Conceptos Básicos

¿Qué son los LLMs? Los Modelos Lingüísticos Grandes (LLMs) son sistemas avanzados de inteligencia artificial (redes neuronales profundas) entrenados con enormes cantidades de texto. Son capaces de procesar, entender y generar texto similar al humano para tareas como traducción, resumen, respuesta a preguntas, generación de contenido creativo y razonamiento. [Source 10-12, 9]
Importancia: Están cambiando fundamentalmente cómo interactuamos con la información y la tecnología, mejorando tareas complejas de Procesamiento del Lenguaje Natural (NLP) y permitiendo nuevas aplicaciones. [Source 9, 16-17] Pueden adaptarse a tareas específicas mediante fine-tuning (ajuste fino) con menos datos y recursos que entrenar desde cero. [Source 18-19] La ingeniería de prompts ayuda a guiar su comportamiento. [Source 20]
Arquitectura Transformer: El Corazón de los LLMs

Base: La arquitectura Transformer (introducida en 2017) superó a las Redes Neuronales Recurrentes (RNNs) gracias a su capacidad de procesar secuencias en paralelo mediante el mecanismo de auto-atención (self-attention), lo que permite capturar dependencias a largo plazo y entrenar más rápido. [Source 29, 34-36, 41]
Componentes Clave:
Entrada y Embeddings: El texto se normaliza, tokeniza (divide en palabras/subpalabras), se convierte en vectores numéricos (embeddings) y se le añade codificación posicional para entender el orden de las palabras. [Source 59-64]
Atención Multi-Cabeza (Multi-Head Attention): Es el mecanismo crucial. Permite al modelo ponderar la importancia de diferentes palabras en la secuencia para entender relaciones (ej: a qué se refiere un pronombre). Usa vectores de Consulta (Q), Clave (K) y Valor (V). Múltiples "cabezas" de atención permiten capturar diferentes tipos de relaciones simultáneamente. [Source 66-67, 69, 71-75, 84-86]
Capas Feedforward y Normalización: Añaden complejidad computacional y ayudan a estabilizar el entrenamiento. [Source 90-93, 97-101]
Encoder-Decoder vs. Decoder-Only: La arquitectura original tenía un encoder (procesa entrada) y un decoder (genera salida). [Source 43-45] Sin embargo, muchos LLMs modernos son decoder-only, simplificando la arquitectura para generar texto directamente desde la entrada. [Source 115-116, 120]
Mixture of Experts (MoE): Una técnica arquitectónica donde múltiples sub-modelos ("expertos") se especializan en diferentes partes de los datos. Una "red de enrutamiento" (gating network) decide qué expertos activar para cada entrada, mejorando la eficiencia computacional (activación dispersa). [Source 121-123, 126, 131-132, 136]
Entrenamiento y Fine-Tuning

Pre-entrenamiento: Es la fase inicial y más costosa. El modelo aprende patrones del lenguaje prediciendo la siguiente palabra en grandes corpus de texto no etiquetado (aprendizaje no supervisado). [Source 435-436, 438] La preparación de datos (limpieza, tokenización) es clave. [Source 165-169]
Fine-Tuning (Ajuste Fino): Después del pre-entrenamiento, el modelo se especializa en tareas o comportamientos específicos (seguir instrucciones, dialogar, ser más seguro) usando conjuntos de datos más pequeños y específicos. [Source 439-441, 445]
SFT (Supervised Fine-Tuning): Entrenar con ejemplos de prompt y respuesta deseada. [Source 440, 447-449]
RLHF (Reinforcement Learning from Human Feedback): Alinear el modelo con las preferencias humanas. Se entrena un "modelo de recompensa" basado en feedback humano (ej: qué respuesta es mejor) y luego se usa para guiar el ajuste del LLM. RLAIF usa feedback de IA en lugar de humano. [Source 453-454, 456-458, 460, 464-466]
PEFT (Parameter-Efficient Fine-Tuning): Técnicas como LoRA o Soft Prompting que ajustan solo un pequeño subconjunto de parámetros, ahorrando muchos recursos computacionales y permitiendo cambiar fácilmente la especialización del modelo. [Source 468-473, 476-481]
Evolución de los Modelos

Tendencias: Ha habido una rápida evolución desde modelos con millones de parámetros a billones, y de entrenar con millones de tokens a trillones. [Source 424-425] El escalado de datos y parámetros ha mejorado el rendimiento y ha llevado a comportamientos emergentes (ej: aprendizaje zero-shot/few-shot). [Source 426]
Hitos Clave:
GPT-1 y BERT: Pioneros en pre-entrenamiento no supervisado (GPT-1, decoder-only) y comprensión bidireccional del contexto (BERT, encoder-only). [Source 190-192, 218-220]
GPT-2 y GPT-3: Demostraron los beneficios del escalado masivo en parámetros y datos, mejorando la coherencia y las capacidades few-shot. [Source 225, 228-229, 234-235, 242-244]
InstructGPT: Mostró la importancia del fine-tuning (SFT y RLHF) para seguir instrucciones y mejorar la seguridad. [Source 250-252]
Chinchilla: Descubrió que para un presupuesto computacional dado, es óptimo escalar tanto el tamaño del modelo como el tamaño del conjunto de datos de forma similar, no solo el tamaño del modelo. [Source 283-286, 288-291]
Familias Notables:
LaMDA (Google): Enfocado en aplicaciones de diálogo. [Source 259-261]
PaLM/PaLM 2 (Google): Modelos muy grandes, eficientes en escala. [Source 294-296, 298-300]
Gemini (Google): Familia de modelos multimodales (texto, imagen, audio, video), con diferentes tamaños (Ultra, Pro, Nano, Flash), usando MoE y contexto largo. [Source 302-305, 307-308, 312-318, 328-330]
Gemma (Google): Familia de modelos abiertos y ligeros basados en la tecnología Gemini. [Source 344-345, 348-350, 353-355]
Llama (Meta): Familia de modelos abiertos, con versiones ajustadas para chat (Llama 2, 3.2). [Source 358-360, 362-364, 367-368]
Mixtral (Mistral AI): Modelo abierto basado en MoE, eficiente en inferencia. [Source 371-374]
OpenAI 01 / DeepSeek: Modelos enfocados en razonamiento complejo, usando RL. [Source 378-382, 384-387]
Otros: Existe un ecosistema creciente de modelos abiertos y comerciales. [Source 406, 419-420]
Uso de LLMs

Ingeniería de Prompts: El arte de diseñar la entrada (prompt) para obtener la salida deseada. Incluye dar instrucciones claras, ejemplos (few-shot), o guiar el razonamiento paso a paso (chain-of-thought). Zero-shot es dar solo la instrucción. [Source 490, 494-495, 497-505]
Técnicas de Muestreo: Controlan cómo el modelo elige la siguiente palabra, afectando la creatividad y diversidad. Ejemplos: Greedy (la más probable), Temperature (ajusta aleatoriedad), Top-K/Top-P (elige entre las K más probables o cuya probabilidad acumulada suma P). [Source 491, 506-508, 509, 512-515]
Evaluación: Es crucial evaluar el rendimiento en tareas específicas, usando datos relevantes y métricas adecuadas, a menudo combinando evaluación humana con autoraters basados en LLMs. [Source 521, 524-527, 529-531, 533-535]
Aceleración de la Inferencia

Necesidad: Modelos más grandes son más lentos y caros de usar (inferencia). Hay un equilibrio entre calidad, latencia y coste. [Source 547-551]
Métodos con Aproximación:
Cuantización: Reducir la precisión numérica de los pesos del modelo (ej: de 32 bits a 8 o 4 bits), ahorrando memoria y acelerando cálculos, con posible impacto mínimo en la calidad. [Source 581-586]
Destilación: Entrenar un modelo más pequeño ("estudiante") para imitar el comportamiento de uno más grande ("profesor"), obteniendo eficiencia con buena calidad. [Source 593-596, 599]
Métodos sin Pérdida de Calidad:
Flash Attention: Optimiza el cálculo de la atención para reducir movimientos de datos entre memorias (IO Aware). [Source 602-607]
Prefix Caching: Reutilizar cálculos de atención (KV Cache) para partes de la entrada que no cambian entre peticiones (ej: en un chat). [Source 608-611, 619]
Speculative Decoding: Usar un modelo pequeño y rápido ("borrador") para predecir varios tokens a la vez, que luego son verificados en paralelo por el modelo principal, acelerando la generación. [Source 624-630, 635]
Batching y Paralelización: Técnicas estándar para procesar múltiples peticiones juntas (batching) o dividir el cálculo en más hardware (paralelización). [Source 639-641, 644-648]
Aplicaciones

Los LLMs se usan en una amplia gama de tareas:
Código y Matemáticas: Generación, compleción, refactorización, traducción, testing y explicación de código. Avances recientes en resolución de problemas matemáticos y de programación competitiva (AlphaCode 2, FunSearch, AlphaGeometry). [Source 659-668, 669-678]
Traducción Automática: Traducciones más fluidas y contextuales. [Source 679-680]
Resumen de Texto: Crear resúmenes concisos y relevantes de documentos largos. [Source 686-687]
Respuesta a Preguntas (QA): Entender la intención y dar respuestas precisas, a menudo mejoradas con sistemas de búsqueda (RAG). [Source 691-692, 695-696]
Chatbots: Conversaciones más naturales y dinámicas. [Source 697-699]
Generación de Contenido: Crear texto creativo (artículos, correos, guiones) con coherencia. [Source 701-704]
Análisis de Texto: Clasificación, análisis de sentimiento, extracción de temas. [Source 711-716, 719-721, 726-728]
Aplicaciones Multimodales: Procesar y generar combinaciones de texto, imágenes, audio y video para tareas creativas, educativas, de accesibilidad, etc. [Source 730-740]
Conclusión Clave

Los LLMs basados en Transformers han evolucionado rápidamente gracias al escalado de datos y parámetros. El fine-tuning permite especializarlos, la ingeniería de prompts guía sus respuestas, y las técnicas de optimización de inferencia los hacen más eficientes. Sus aplicaciones son vastas y continúan expandiéndose. [Source 744, 748-757]