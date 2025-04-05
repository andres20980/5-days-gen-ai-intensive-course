# Kaggle Generative AI Intensive - Día 4: Modelos de Lenguaje Específicos de Dominio (Resumen Híbrido)

## Bienvenida e Introducción (Paige Bailey)

* **Ponente:** Paige Bailey (Google DeepMind)
* Bienvenida al Día 4 del curso intensivo de IA Generativa de Kaggle.
* Más de 250.000 desarrolladores participando en todo el mundo.
* Curso patrocinado por Kaggle, con apoyo de Google Cloud, Google DeepMind, Alphabet.
* Día 4 enfocado en **Modelos de Lenguaje Específicos de Dominio**.
* Agradecimiento a moderadores y equipo de operaciones (mención especial a Brenda Flynn y Kel Perk).

## Repaso de los Días Anteriores (Anant Nawalgaria)

* **Día 1:** Modelos fundacionales, técnicas de ajuste y prompt engineering.
* **Día 2:** Embeddings y bases de datos vectoriales.
* **Día 3:** Agentes de IA y su arquitectura.
* **Día 4:** Cómo adaptar modelos de lenguaje para dominios específicos.

## Introducción a los Modelos Específicos de Dominio

* En lugar de usar un modelo generalista, a veces conviene afinar modelos para tareas o dominios concretos (medicina, derecho, finanzas, etc.).
* Permiten:
  * Mejor rendimiento en tareas específicas.
  * Reducción de coste computacional.
  * Personalización de respuestas según el contexto del negocio.
* Técnicas destacadas:
  * **Fine-tuning** (ajuste completo del modelo).
  * **LoRA (Low-Rank Adaptation)**: más eficiente, adapta pequeñas capas.
  * **In-Context Learning (few-shot)**: sin modificar pesos, sólo ejemplos.

## Estrategias de Adaptación

* **Instrucción Tuning:** Afinar el modelo con datasets basados en instrucciones (e.g. FLAN).
* **Dataset Curado del Dominio:** Recopilar ejemplos reales y representativos.
* **Evaluación Continua:** Validar si el modelo mejora tras cada iteración.

## Buenas Prácticas

* Comenzar con modelos pre-entrenados robustos.
* Usar LoRA si se cuenta con recursos limitados.
* Controlar sobreajuste: evitar que el modelo memorice el dataset.
* Medir calidad con métricas específicas del dominio (accuracy, BLEU, F1, etc.).
* Validación humana en entornos sensibles (médico, legal).

## Aplicaciones

* Chatbots especializados (soporte técnico, legal, financiero...).
* Análisis de textos jurídicos o científicos.
* Clasificación de documentos según jerga sectorial.
* Generación de informes clínicos.
* Traducción técnica o profesional adaptada al sector.

## Riesgos y Consideraciones Éticas

* **Sobreespecialización:** puede limitar la capacidad del modelo para responder fuera de contexto.
* **Bias del dominio:** si los datos del sector están sesgados, el modelo también lo estará.
* **Validación crítica en áreas sensibles:** medicina, derecho, seguridad.
* **Gobernanza y control de versiones:** mantener trazabilidad de cambios y datasets usados.

## Code Labs del Día 4

### Code Lab 1: Fine-Tuning con un Dataset Médico

* Cargar un modelo base (ej. T5 o BERT).
* Aplicar fine-tuning con ejemplos de preguntas clínicas.
* Evaluar el rendimiento con ejemplos de validación.

### Code Lab 2: Clasificador Legal con Embeddings + Modelo Ligero

* Generar embeddings de documentos jurídicos.
* Usar un modelo simple para clasificar (SVM o Red Neuronal ligera).
* Evaluar resultados y ajuste fino según necesidades del despacho.

### Code Lab 3: Traducción Técnica con LoRA

* Aplicar LoRA sobre un modelo multilingüe.
* Usar textos técnicos como dataset de entrenamiento.
* Comparar resultados con traducción automática generalista.

---

## Recursos y Herramientas

* **Frameworks utilizados:**
  * Hugging Face Transformers
  * LoRA / PEFT (Parameter-Efficient Fine-Tuning)
  * TensorFlow / PyTorch
* **Plataformas:**
  * Kaggle Notebooks
  * Google Colab
  * Vertex AI (para entrenamiento y despliegue)
* **Modelos recomendados:**
  * BERT, RoBERTa, T5, FLAN-T5
  * Gemini para casos multimodales

---

## Reflexión Final

* Adaptar modelos al dominio permite obtener soluciones más precisas y útiles.
* No siempre hace falta fine-tuning costoso: LoRA e In-context learning pueden ser muy efectivos.
* Evaluar y validar constantemente es clave para mantener calidad y seguridad.
