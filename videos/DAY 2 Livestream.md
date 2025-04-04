# Kaggle Generative AI Intensive - Sesión Día 2: Embeddings y Bases de Datos Vectoriales (Resumen Híbrido)

## Bienvenida e Introducción (Paige Bailey)

* **Ponente:** Paige Bailey (Líder de Developer Relations Engineering, Google DeepMind).
* ¡Bienvenidos de nuevo al segundo día del curso intensivo de IA Generativa de Kaggle!
* Más de 250,000 desarrolladores de todo el mundo conectados.
* **Temas de hoy:** Embeddings y Bases de Datos Vectoriales.
* **Recordatorio Día 1:** El contenido sobre Modelos Fundacionales y Prompt Engineering (incluyendo la grabación de YouTube) está disponible para consulta.
* Menciones a herramientas clave: Modelos Gemini, AI Studio, Vertex AI, y otros productos de Google.
* Gran respuesta y participación en YouTube, Discord, etc.

## Descripción General del Curso y Día 2

* **Curso:** Intensivo de 5 días sobre IA Generativa.
* **Organizado por:** Kaggle en colaboración con Google Cloud y Google DeepMind.
* **Estructura:** Un recorrido rápido por temas clave del espacio de IA Generativa.
* **Hoy (Día 2):** Embeddings y Bases de Datos Vectoriales.
* **Actividades del Día 2:**
    * Escuchar el episodio resumen del podcast (generado por NotebookLM).
    * Leer el whitepaper sobre "Embeddings and Vector Stores/Databases".
    * Completar los Code Labs en Kaggle (Anant hará una demostración más tarde).

## Agradecimiento a los Moderadores y Equipo

* Agradecimiento especial a los moderadores por su trabajo incansable en Discord respondiendo preguntas y asegurando el éxito del curso.
* Mención especial a Brenda Flynn y Kunal por la producción y gestión de escenario.

## Resumen del Currículum Día 2 (Anant)

* **Ponente:** Anant Nawalgaria (Google DeepMind).
* **Objetivo:** Resumir los whitepapers de hoy para preparar la sesión de Q&A.

### Whitepaper: Embeddings y Bases de Datos Vectoriales

* **¿Qué son los Embeddings?**
    * Representaciones vectoriales numéricas de datos (texto, imágenes, etc.).
    * Mapean datos diversos a un espacio semántico común.
    * La distancia en este espacio actúa como proxy de la similitud semántica.
    * Útiles para comparar datos y como representación rica para modelos/tareas posteriores.
* **Tipos de Embeddings:**
    * **Texto:** Evolución desde Word2Vec hasta modelos contextuales (BERT, Gemini).
    * **Imagen y Multimodales:** Para representar y comparar diferentes tipos de datos.
    * **Datos Estructurados y Grafos:** También pueden ser embebidos.
* **Entrenamiento de Embeddings:**
    * A menudo usan "dual encoders" y "contrastive loss" para agrupar ítems similares.
* **Evaluación de Embeddings:**
    * Usar métricas (Precision, Recall) y benchmarks estándar para medir la calidad.
* **Búsqueda Vectorial Eficiente:**
    * La búsqueda lineal es inviable para miles de millones de vectores.
    * Se usan algoritmos **ANN (Approximate Nearest Neighbor)** como SCAN y HNSW.
    * Estos algoritmos sacrifican una mínima precisión por ganancias masivas en velocidad.
* **Bases de Datos Vectoriales:**
    * Diseñadas específicamente para almacenar, gestionar y consultar embeddings eficientemente a escala, utilizando algoritmos ANN.
* **Aplicaciones:**
    * Búsqueda semántica.
    * Sistemas de recomendación.
    * **RAG (Retrieval-Augmented Generation):** Los embeddings se usan en la fase de recuperación (retrieval) para encontrar contexto relevante, que luego se pasa al LLM para generar respuestas más factuales y ancladas (grounded).

## Sesión de Preguntas y Respuestas (Q&A) con Expertos

### Participantes Expertos:

* **Patricia Florissi** (Office of the CTO, Google Cloud)
* **Alan Li** (Google Cloud Databases)
* **Xiaoqi Ren** (Vertex AI)
* **Howard Zhou** (Google DeepMind)
* **Andre Araujo** (Google DeepMind)
* **Chuck Sugnet** (Vertex AI)
* **Anant Nawalgaria** (Google DeepMind)

---

### Pregunta 1: Avances y Mejores Prácticas en Embeddings

> **Pregunta:** Crear embeddings efectivos es crucial. ¿Cuáles son los últimos avances o mejores prácticas para generar embeddings que capturen significados semánticos matizados, especialmente para dominios especializados o datos multimodales? ¿Cuánto impacta la elección del modelo de embedding en el rendimiento de la búsqueda vectorial posterior?

* **Respuesta (Andre A.):**
    * **Avance: Integrar LLMs en el desarrollo de embeddings:**
        * Usar LLMs pre-entrenados como "backbone" para inicializar el modelo de embedding, aprovechando su comprensión multilingüe y multimodal.
        * Usar LLMs para curar datasets de entrenamiento o generar ejemplos de alta calidad. (Ver reporte técnico de Gemini Embedding).
    * **Multimodalidad (Imágenes):** Abordar la falta de conciencia espacial ("spatial awareness"). El equipo de Andre introdujo **TIPS** (Text-Image Pretraining with Spatial awareness), un nuevo embedding potente (paper en ICLR, código y modelos disponibles).
    * **Impacto en Rendimiento:** ¡Muy significativo! Especialmente en RAG, si no se recuperan los documentos correctos, el LLM no podrá responder bien. La calidad del embedding puede ser un cuello de botella. Depende de la aplicación (tamaño del índice, similitud de datos con el entrenamiento del embedding). ¡Elegir con cuidado!
* **Respuesta (Howard Z.):**
    * **Técnica Matryoshka Embedding:** Permite entrenar un embedding de alta dimensión (ej. 1000) de forma que subconjuntos más cortos (ej. los primeros 200 floats) también sean embeddings válidos en el mismo espacio. Permite elegir la dimensionalidad a almacenar según la necesidad, optimizando el almacenamiento.
    * **Curación de Datos con LLMs:** Es crucial. Permite filtrar ejemplos de baja calidad, determinar pasajes positivos/negativos relevantes para retrieval y generar datasets sintéticos ricos.
    * **Modelos Multimodales como Puente:** Modelos como E5-v usan LLMs multimodales para mapear diferentes modalidades (imagen, texto) a un espacio de embedding compartido. Luego, el espacio se organiza principalmente con información textual. Esta técnica es poderosa y la tendencia es que modelos únicos multimodales se vuelvan más relevantes y precisos.

---

### Pregunta 2: Bases de Datos Vectoriales Integradas vs. Dedicadas (AlloyDB)

> **Pregunta:** Al integrar capacidades de búsqueda vectorial en sistemas de BD existentes (ej. AlloyDB) vs. usar BD vectoriales dedicadas, ¿cuáles son las principales compensaciones arquitectónicas en cuanto a rendimiento (latencia, throughput), costo, consistencia de datos y facilidad de uso para desarrolladores construyendo RAG o búsqueda semántica? (Y una breve descripción de AlloyDB).

* **Respuesta (Alan L.):**
    * **AlloyDB:** Base de datos de GCP, 100% compatible con PostgreSQL, con innovaciones arquitectónicas para mayor rendimiento que el open-source. Incorpora búsqueda vectorial nativa.
    * **Compensaciones:**
        * **Rendimiento:** Aunque importante, los requisitos no relacionados con el rendimiento son cada vez más relevantes. Las BD existentes con búsqueda vectorial integrada (como AlloyDB con SCAN, algoritmo de Google usado en Search/YouTube) a menudo funcionan bien para el 90% de los casos y son competitivas con BD vectoriales dedicadas.
        * **Ubicación de Datos y Complejidad:** Considerar dónde residen los *otros* datos necesarios (ej. filtros). Si están en la misma BD operacional (AlloyDB) o data lakehouse (BigQuery), usar la capacidad vectorial integrada simplifica:
            * **Consultas Unificadas:** Combinar búsqueda vectorial, filtros, joins en una sola consulta (SQL).
            * **Consistencia de Datos:** Evita problemas de sincronización entre sistemas.
            * **Menor Costo Operacional:** Evita ETLs complejos y gestión de múltiples sistemas.
        * **BD Vectoriales Dedicadas (ej. Vertex AI Vector Search):** Tienen sentido cuando:
            * Los datos son mayormente no estructurados (video, imágenes, documentos) y no residen ya en una BD/DW.
            * Se necesita exprimir el último 10% de rendimiento (aunque puede implicar tradeoffs como mayor costo o consistencia más laxa).
        * **Otros Factores (Madurez):** Las BD existentes suelen tener características empresariales más maduras (seguridad, compliance, fiabilidad, backup, HA) que los sistemas especializados más nuevos.
        * **Conclusión:** Evaluar los requisitos de *toda* la aplicación.

---

### Pregunta 3: Impacto Estratégico de Embeddings/Vectores en Arquitecturas Empresariales

> **Pregunta:** Desde un punto de vista estratégico, ¿cómo ven el impacto del panorama en rápida evolución de embeddings y BD vectoriales en las arquitecturas de datos empresariales y los tipos de aplicaciones impulsadas por IA que las empresas pueden construir? ¿Cuáles son los desafíos clave (costo, estandarización, brecha de talento) que enfrentan las organizaciones al adoptar estas tecnologías a escala?

* **Respuesta (Patricia F.):**
    * **Impacto Profundo (Cambio de Paradigma):** Pasamos de optimizar para "exact match" (SQL en datos estructurados) a optimizar para similitud/proximidad en múltiples dimensiones y modalidades (texto, imagen, video, audio). Se pueden crear múltiples índices por BD, optimizados por tarea.
    * **Impacto Arquitectónico:** Necesidad de (re)aprender a ingerir, organizar, gestionar y acceder a nuevas modalidades de datos (semi/no estructurados). Entender la variedad de mecanismos de indexación y sus tradeoffs (precisión, rendimiento, escalabilidad).
    * **Impacto en Desarrollo:** Demanda una comprensión más profunda del significado de los embeddings.
    * **Impacto en Experiencia de Usuario:** Necesidad de reimaginar la UX para aprovechar la recuperación de datos multimodales complejos.
    * **Desafíos Clave:**
        * **Costo:** Infraestructura para desplegar y mantener BD vectoriales.
        * **Estandarización:** Falta de estándares universales para embeddings e interfaces de BD dificulta integración/interoperabilidad.
        * **Brecha de Talento:** (¡Este curso ayuda a cerrarla!).
        * **Escalabilidad/Rendimiento:** Manejar miles de millones de vectores con baja latencia.
        * **Gobernanza/Seguridad/Compliance:** No deben descuidarse.
        * **Integración:** Conectar BD vectoriales con sistemas relacionales y aplicaciones existentes es complejo.
    * **Optimismo:** La representación multimodal vía embeddings será la **base de las arquitecturas empresariales modernas**.

---

### Pregunta 4: Técnicas Avanzadas de Búsqueda Vectorial (Más allá de Coseno/Euclidiana)

> **Pregunta:** Más allá de la similitud de coseno o distancia euclidiana estándar, ¿qué técnicas o estrategias de indexación más sofisticadas (ej. incorporar filtrado de metadatos, enfoques de búsqueda híbrida, reranking) están demostrando ser más efectivas para mejorar la relevancia y precisión de los resultados de búsqueda vectorial en aplicaciones del mundo real? ¿Cómo se incorporan en plataformas como Vertex AI?

* **Respuesta (Chuck S.):**
    * **Importancia de la Evaluación:** Antes de añadir complejidad, evaluar si es necesario para tu caso de uso con un buen benchmark/dataset.
    * **Búsqueda Híbrida (Hybrid Search):** Muy efectiva. Combina búsqueda semántica (embeddings, captura sinónimos/relaciones) con búsqueda tradicional por palabras clave (keyword, captura coincidencias literales exactas). Vertex AI Vector Search soporta ambos (sparse + dense). Se puede implementar con paquetes como BM25. Se volverá más complejo con multimodalidad.
    * **Reranking:** Útil para refinar la lista final de resultados, especialmente al combinar múltiples métodos de retrieval o al querer priorizar ciertas fuentes (ej. FAQs oficiales vs. notas comunitarias). Considerar el presupuesto de latencia.
    * **Filtrado (Filtering):** Puede reducir drásticamente la latencia al eliminar documentos irrelevantes al inicio. Crucial a escala.
    * **Facilidad de Uso / Mantenimiento:** Considerar características como inserciones en streaming (streaming inserts) para evitar reconstruir índices constantemente. Evaluar si la plataforma elegida es fácil de usar, monitorear, si cumple requisitos de privacidad/seguridad y si la organización puede mantenerla y escalarla.

---

### Pregunta 5 (Comunidad - Cyclone D.): Actualización de Modelos de Embedding

> **Pregunta:** Para los modelos de embedding, ¿cómo actualizo a modelos más nuevos cuando están disponibles? ¿Necesito volver a procesar todos los datos de la base de datos con el nuevo modelo, o hay una forma mejor?

* **Respuesta (Chuck S.):**
    * **Malas noticias:** Sí, generalmente necesitas re-generar todos tus embeddings al cambiar de modelo. No son compatibles entre sí.
    * **Importancia de la Evaluación:** Es crucial tener buenas evaluaciones para verificar que la versión del modelo de consulta coincide con la del índice y para medir el impacto (calidad, latencia, rendimiento bajo carga).
    * **Estar Preparado para Iterar:** Los modelos mejoran rápidamente; querrás poder adoptar esas mejoras.
* **Respuesta (Howard Z.):**
    * **Investigación Activa:** Se está investigando activamente cómo mapear eficientemente embeddings antiguos a nuevos para facilitar las actualizaciones ("Leave no one behind"). Hay resultados prometedores, pero aún no están desplegados a gran escala.

---

### Pregunta 6: Impacto de usar diferentes modelos para documentos y queries en RAG

> **Pregunta:** En sistemas RAG, ¿qué impacto potencial podría surgir en la precisión de la recuperación o la calidad de las respuestas generadas por el LLM si se usan diferentes modelos de embedding para los documentos y las consultas?

* **Respuesta (Xiaoqi R.):**
    * **Crítico:** Es **esencial usar el mismo modelo de embedding** para generar los embeddings de los documentos y de las consultas.
    * **Razón:** Cada modelo mapea los datos a su propio espacio vectorial específico. Usar modelos diferentes resultaría en que las consultas y los documentos estén en espacios incompatibles, haciendo que las medidas de distancia (similitud) no reflejen relaciones semánticas reales y la recuperación sea incorrecta.

---

### Pregunta 7: Mantener Relevancia en RAG con Datos Dinámicos (System Drift)

> **Pregunta:** En un sistema RAG, la indexación se realiza por adelantado sobre el dataset de la aplicación. ¿Cómo asegura el sistema que los resultados de la consulta sigan siendo relevantes para el contexto actual en una aplicación dinámica o en tiempo real después del despliegue?

* **Respuesta (Anant N.):**
    * Medir el "drift" (cambio en la distribución de embeddings o rendimiento) es crítico (usando evaluaciones).
    * La combinación de embeddings Matryoshka (permitiendo usar dimensiones menores) y ventanas de contexto grandes en LLMs (permitiendo recuperar más documentos, tolerando algunos falsos positivos) puede hacer el proceso más eficiente, enfocándose más en "recall" que en "precision@K".
* **Respuesta (Patricia F.):**
    * **Objetivo:** Cerrar la brecha entre índice estático y datos cambiantes.
    * **Estrategias de Actualización:**
        * **Indexación Incremental:** Añadir nuevos datos sin reconstruir todo el índice.
        * **HNSW:** Maneja inserciones eficientemente.
        * **Advanced IVF:** Mayor throughput de actualización.
        * **Buffers en Memoria + Fusión en Background:** Técnica común en BD vectoriales.
        * **Change Data Capture (CDC):** Automatiza triggers de actualización desde las fuentes de datos.
    * **Consideración:** La indexación continua consume recursos.
    * **Alternativa: Real-time RAG / No-index RAG:** Consultar fuentes de datos en vivo directamente en el momento de la consulta, transformando la query al formato nativo de la fuente. Bypassa la necesidad de índices precalculados.
    * **Balance:** Siempre hay un trade-off entre costo, rendimiento, precisión, escalabilidad y frescura de los datos.
* **Respuesta (Alan L.):**
    * **Consistencia Transaccional:** En BD operacionales (como AlloyDB), las escrituras confirmadas son visibles inmediatamente para lecturas posteriores (incluyendo actualizaciones de índice), evitando datos obsoletos y simplificando el desarrollo.
    * **Innovación:** Trabajo en manejo automático de drift en la distribución del índice.
* **Aporte (Paige B.):** La API de Gemini tiene una función para anclar (ground) la respuesta en resultados de Google Search recientes, similar al enfoque de consultar fuentes en vivo mencionado por Patricia.

---

### Pregunta 8 (Comunidad - Andy G.): Precisión de Modelos Multimodales vs. Single-Modales para Embeddings

> **Pregunta:** ¿Cómo se compara la precisión de un único modelo multimodal para embeddings de imagen y texto con el uso de modelos separados de modalidad única?

* **Respuesta (Andre A.):**
    * **Asunción:** La pregunta se refiere a búsqueda *dentro* de una misma modalidad (ej. texto-texto o imagen-imagen). Si es búsqueda *cruzada* (texto-imagen), se *necesita* un modelo multimodal.
    * **No Necesariamente Peor:** Un modelo multimodal no es intrínsecamente peor para tareas unimodales. De hecho, el entrenamiento multimodal (ej. con pares imagen-texto de la web) permite aprovechar mucha más supervisión que el entrenamiento unimodal (ej. solo imágenes con etiquetas manuales costosas).
    * **Factores:** Depende de los datos de entrenamiento, tamaño del modelo.
    * **Tendencia:** Hacia modelos más grandes y capaces que funcionan bien en múltiples modalidades.
    * **Knowledge Distillation:** Se puede usar para crear modelos más pequeños y especializados a partir de uno grande multimodal.
* **Respuesta (Howard Z.):**
    * **Uso de LLMs Multimodales como Puente:** Técnicas como E5-v usan un LLM multimodal para mapear todas las entradas a un espacio compartido, y luego organizan ese espacio principalmente con datos textuales. Esto transfiere la estructura semántica a otras modalidades.
    * **Evolución:** Modelos "dual encoder" (como CLIP) fueron estado del arte, pero modelos únicos multimodales (PaLM-e, E5-v) están alcanzando e incluso superando su precisión, incluso en tareas unimodales.

---

## Resumen de Code Labs Día 2 (Anant)

### Code Lab 1: Construcción de un Sistema RAG Básico

* **Pasos:**
    1.  Crear datos sintéticos (párrafos).
    2.  Usar ChromaDB (BD vectorial open-source en memoria).
    3.  Generar embeddings de los párrafos usando la API de Gemini.
    4.  Indexar (persistir) los embeddings en ChromaDB.
    5.  Realizar una consulta (query) en lenguaje natural.
    6.  ChromaDB genera el embedding de la query y recupera los K documentos más similares (fase de retrieval).
    7.  Usar los documentos recuperados como contexto para un LLM (Gemini Flash) para generar la respuesta final (fase de generation).

### Code Lab 2: Explorando Similitud Semántica con Embeddings

* **Pasos:**
    1.  Definir frases sintéticas.
    2.  Generar embeddings para cada frase usando el modelo Gecko de Google.
    3.  Calcular la similitud semántica (coseno) entre todos los pares de embeddings.
    4.  Visualizar las similitudes en un mapa de calor (heatmap).
* **Observación:** Frases con significado similar aparecen con colores más oscuros (similitud cercana a 1), mientras que frases diferentes tienen colores más claros (similitud cercana a 0). La diagonal es máxima (comparación consigo mismo).

### Code Lab 3: Clasificación usando Embeddings como Features (Keras)

* **Concepto:** Usar embeddings no solo para búsqueda, sino como características (features) ricas en semántica para modelos de machine learning downstream.
* **Pasos:**
    1.  Cargar dataset de clasificación de texto (Newsgroup).
    2.  Preprocesar los datos.
    3.  Generar embeddings para los textos usando un modelo de embedding con `task_type='CLASSIFICATION'`.
    4.  Construir un modelo de clasificación simple en Keras que toma los embeddings como entrada.
    5.  Añadir una o dos capas clasificadoras encima de los embeddings.
    6.  Entrenar **solo** las capas añadidas (eficiente, ya que los embeddings pre-entrenados capturan mucha información).
* **Resultado:** Se obtiene un buen rendimiento en la clasificación con poco esfuerzo de entrenamiento.

---

## Pop Quiz

1.  **¿Para qué aplicación los embeddings NO son los más adecuados?**
    * (a) Retrieval Augmented Generation (RAG)
    * (b) Sistemas simples basados en reglas (Simple rule-based systems)
    * (c) Detección de anomalías (Anomaly detection)
    * (d) Sistemas de recomendación (Recommender systems)
    * **Respuesta Correcta: (b) Sistemas simples basados en reglas**

2.  **¿Cuál de las siguientes es una ventaja principal de SCAN sobre otros algoritmos ANN?**
    * (a) Es ampliamente open-source y disponible.
    * (b) Está diseñado para datos de alta dimensionalidad y tiene excelentes tradeoffs velocidad-precisión.
    * (c) Solo devuelve coincidencias exactas.
    * (d) Se basa en una técnica de hashing simple y tiene bajo costo computacional.
    * **Respuesta Correcta: (b) Está diseñado para datos de alta dimensionalidad y tiene excelentes tradeoffs velocidad-precisión.**

3.  **¿Cuáles son algunas de las principales debilidades de los modelos Bag-of-Words para generar embeddings de documentos?**
    * (a) Ignoran el orden de las palabras y los significados semánticos.
    * (b) Son computacionalmente caros y requieren grandes cantidades de datos.
    * (c) No pueden usarse para búsqueda semántica o descubrimiento de temas.
    * (d) Solo son efectivos para documentos cortos y no capturan dependencias a largo alcance.
    * **Respuesta Correcta: (a) Ignoran el orden de las palabras y los significados semánticos.**

4.  **¿Cuál de los siguientes es un desafío común al usar embeddings para búsqueda y cómo puede abordarse?**
    * (a) No pueden manejar grandes datasets; hay que usar datasets más pequeños.
    * (b) Siempre son superiores a la búsqueda tradicional; no hay necesidad de combinar.
    * (c) Pueden no capturar bien información literal; combinar con búsqueda de texto completo (full-text search).
    * (d) Cambian demasiado frecuentemente; hay que prevenir actualizaciones.
    * **Respuesta Correcta: (c) Pueden no capturar bien información literal; combinar con búsqueda de texto completo.**

5.  **¿Cuál es la ventaja principal de usar Locality Sensitive Hashing (LSH) para búsqueda vectorial?**
    * (a) Garantiza encontrar los vecinos más cercanos exactos.
    * (b) Reduce el espacio de búsqueda agrupando ítems similares en "hash buckets".
    * (c) Es el único método que funciona para vectores de alta dimensión.
    * (d) Siempre proporciona el mejor tradeoff entre velocidad y precisión.
    * **Respuesta Correcta: (b) Reduce el espacio de búsqueda agrupando ítems similares en "hash buckets".**

---

## Recursos y Herramientas Mencionadas

* **Plataformas/APIs:**
    * Kaggle
    * Modelos/APIs Gemini
    * AI Studio ([ai.google.dev](https://ai.google.dev/))
    * Vertex AI (incluyendo Vertex AI Vector Search)
    * Google Cloud
    * Google DeepMind
    * Discord (para la comunidad del curso)
    * NotebookLM (generador del podcast, interactuar con whitepapers)
* **Bases de Datos / Búsqueda Vectorial:**
    * Bases de Datos Vectoriales (concepto general)
    * AlloyDB (BD compatible Postgres con búsqueda vectorial integrada)
    * ChromaDB (BD vectorial open-source en memoria)
    * Algoritmos ANN: SCAN, HNSW, IVF (Advanced Inverted File), LSH (Locality Sensitive Hashing)
    * Búsqueda Híbrida (Keyword + Semántica)
    * Reranking
    * Filtrado (Filtering)
* **Modelos / Embeddings:**
    * Familia Gemini (Flash, Pro)
    * Modelos de Embedding (Gecko, Gemini Embedding Model)
    * Modelos Multimodales (PaLM-e, E5-v, TIPS)
    * Modelos Dual Encoder (CLIP, Align)
    * Modelos de Texto Tempranos (Word2Vec, BERT)
    * Embeddings Matryoshka
* **Conceptos/Técnicas Clave:**
    * Embeddings (Texto, Imagen, Multimodal, Estructurado, Grafo)
    * Similitud Semántica (Distancia Coseno, Euclidiana)
    * RAG (Retrieval-Augmented Generation)
    * Entrenamiento de Embeddings (Dual Encoders, Contrastive Loss)
    * Evaluación de Embeddings (Precision, Recall, Benchmarks)
    * Drift (Data Drift, Concept Drift, Embedding Drift)
    * Indexación (Incremental, HNSW, IVF)
    * Consistencia de Datos (Transaccional vs. Eventual)
    * Knowledge Distillation
    * Bag-of-Words (como técnica antigua de representación)
* **Datasets:**
    * Newsgroup Text Dataset
* **Bibliotecas/Herramientas:**
    * Keras (para el code lab de clasificación)
    * BM25 (mencionado como algoritmo de keyword search)
* **Recursos del Curso:**
    * Whitepapers (Embeddings and Vector Stores/Databases)
    * Podcast Resumen Diario
    * Code Labs en Kaggle