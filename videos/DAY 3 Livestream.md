# Kaggle Generative AI Intensive - Día 3: Agentes de IA Generativa (Resumen Híbrido)

## Bienvenida e Introducción (Paige Bailey)

* **Ponente:** Paige Bailey (Lead Developer Relations, Google DeepMind)
* Más de 250,000 personas conectadas en todo el mundo.
* Día 3 enfocado en **Agentes de IA Generativa**.
* **Objetivo:** Cómo incorporar agentes inteligentes en proyectos de ingeniería de software.
* Agradecimiento al equipo de moderadores, logísticos y producción por su dedicación.

## Descripción General del Día 3 (Anant Nawalgaria)

* **Ponente:** Anant Nawalgaria (Google DeepMind)
* Día 1: Modelos fundacionales + prompt engineering.
* Día 2: Embeddings y bases de datos vectoriales.
* Día 3: Agentes de IA → piezas autónomas que pueden observar, razonar, actuar y aprender.
* Recursos recomendados:
  * Whitepaper sobre agentes.
  * Podcast generado con NotebookLM.
  * Notebooks interactivos en Kaggle.

## ¿Qué es un Agente de IA Generativa?

* Es una entidad computacional que:
  * Observa su entorno.
  * Toma decisiones.
  * Realiza acciones de forma autónoma.
  * Aprende con el tiempo.
* Inspirados en la inteligencia humana, pero especializados en tareas computacionales.
* Elementos clave:
  * Memoria (corto/largo plazo).
  * Razonamiento.
  * Planificación.
  * Interacción (natural language I/O).
  * Herramientas externas (API, bases de datos, navegadores, etc.).

## Ejemplos y Aplicaciones

* Asistentes personales (tipo GPT con plugins).
* Sistemas de soporte al cliente automatizados.
* Exploración de información en entornos complejos.
* Ejecución de workflows automáticos (RPA potenciado por LLMs).
* Agentes que escriben código, resumen documentos, crean pipelines, etc.

## Arquitectura Típica de un Agente

1. **Observación / Entrada:**
   * Texto natural, datos estructurados o sensores.
2. **Procesamiento / Razonamiento:**
   * Uso de LLM para interpretar el input.
   * Algoritmos de planificación (ej. ReAct, AutoGPT, BabyAGI).
3. **Toma de decisiones:**
   * Determinar el próximo paso o acción.
4. **Acción:**
   * Ejecutar código, llamar a una API, buscar información, etc.
5. **Memoria / Registro:**
   * Guardar lo aprendido para uso futuro.

## Técnicas y Frameworks Clave

* **LangChain** y **Semantic Kernel**: Frameworks para construir agentes sobre LLMs.
* **ReAct**: Interleaving de razonamiento y acción.
* **Toolformer**: Entrenamiento de LLMs para usar herramientas externas.
* **AutoGPT / BabyAGI**: Agentes que se auto-refinan y generan subobjetivos.
* **Planning with Code Execution**: Capacidad de ejecutar código dinámicamente en notebooks o entornos seguros.

## Consideraciones de Diseño

* ¿El agente necesita recordar cosas?
* ¿Qué herramientas debe poder usar?
* ¿Requiere acceso a la web o bases de datos?
* ¿Debe actuar en nombre del usuario? ¿Hasta qué punto?

## Riesgos y Retos Éticos

* **Alucinaciones**: decisiones equivocadas por respuestas inventadas.
* **Seguridad**: acceso a APIs, ejecución de código.
* **Sesgo**: reflejo de datos o instrucciones problemáticas.
* **Supervisión**: agentes que actúan sin suficiente monitoreo.

## Code Labs del Día 3

### Code Lab 1: Agente Simple de Tareas con LangChain

* Crear un agente que reciba tareas escritas por el usuario.
* Interpretar la tarea y planificar una secuencia de pasos.
* Ejecutar herramientas básicas (búsqueda, calculadora, resumen de texto).
* Usar memoria simple para almacenar el historial.

### Code Lab 2: Agente Interactivo con API Externas

* Crear un agente que pueda:
  * Buscar información online.
  * Llamar APIs reales (ej. clima, moneda, Wikipedia).
  * Mostrar resultados al usuario.
* Uso de ReAct + herramienta de búsqueda.

### Code Lab 3: Multi-Agente para Resolución de Problemas

* Crear múltiples agentes especializados:
  * Uno para análisis de datos.
  * Otro para visualización.
  * Otro para interpretación y presentación.
* Orquestar colaboración entre agentes para resolver un problema complejo.
