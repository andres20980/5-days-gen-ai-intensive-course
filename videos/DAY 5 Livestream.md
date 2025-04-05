# Kaggle Generative AI Intensive - Día 5: MLOps para IA Generativa (Resumen Híbrido)

## Bienvenida e Introducción (Paige Bailey)

* **Ponente:** Paige Bailey (Engineering Lead, Developer Relations – Google DeepMind)
* Último día del curso intensivo de IA Generativa de Kaggle.
* Más de 250,000 desarrolladores han participado durante la semana.
* Día 5 centrado en **cómo llevar aplicaciones de IA generativa a producción**, usando buenas prácticas de MLOps.
* Agradecimiento especial al equipo de moderación y operaciones, en especial a Brenda Flynn y Kal.

## Descripción General del Día 5 (Anant Nawalgaria)

* **Ponente:** Anant Nawalgaria (Google DeepMind)
* Repaso de los días anteriores:
  * **Día 1:** Fundamentos + Prompt Engineering.
  * **Día 2:** Embeddings y búsqueda vectorial.
  * **Día 3:** Agentes de IA.
  * **Día 4:** Modelos específicos de dominio.
* **Día 5:** Enfoque en **escalar, monitorear y mantener** sistemas de IA generativa en producción.
* Se trabajará con herramientas de **Vertex AI**, MLOps y pipelines automatizados.

## ¿Qué es MLOps para IA Generativa?

* MLOps = Machine Learning + DevOps.
* Conjunto de prácticas para:
  * Entrenar, desplegar, versionar y monitorear modelos.
  * Automatizar tareas repetitivas.
  * Asegurar calidad, reproducibilidad y escalabilidad.
* Para IA Generativa, implica desafíos únicos:
  * **Alucinaciones** y veracidad.
  * **Evaluación subjetiva**.
  * Uso de APIs de terceros y herramientas externas.

## Componentes Clave de un Pipeline de MLOps

1. **Ingesta de Datos**
   * Preparar y limpiar datos de entrenamiento / fine-tuning.
2. **Entrenamiento y Evaluación**
   * Puede implicar LoRA, prompt tuning, embeddings...
3. **Versionado**
   * Modelos, datasets, prompts, código → todos deben versionarse.
4. **Despliegue**
   * En Vertex AI u otros entornos productivos.
   * Modelos como servicio (API).
5. **Monitoreo y Logging**
   * Tasa de errores, latencia, distribución de inputs.
   * Métricas personalizadas (e.g. groundedness, toxicidad, etc.).
6. **Actualización y Reentrenamiento**
   * Basado en feedback, nuevos datos, cambios de contexto.

## Herramientas Destacadas

* **Vertex AI Pipelines**: para definir flujos reproducibles de ML.
* **Vertex AI Model Registry**: gestión de versiones de modelos.
* **Vertex AI Experiments**: comparación de entrenamientos y parámetros.
* **Vertex AI Endpoints**: para servir modelos en producción.
* **BigQuery, GCS, Pub/Sub**: para almacenamiento y procesamiento de datos.

## Evaluación de Modelos de IA Generativa

* Métricas tradicionales no siempre aplican (accuracy, F1...).
* Nuevas métricas:
  * **Groundedness**: ¿está basada la respuesta en fuentes reales?
  * **Factualidad**, **Toxicidad**, **Relevancia**, **Diversidad**.
* Evaluación humana o semi-automatizada a través de LLMs.
* Uso de técnicas como A/B testing en producción.

## Mejores Prácticas

* Separar entornos (desarrollo, staging, producción).
* Hacer pruebas con usuarios reales antes del despliegue total.
* Implementar fallback si el modelo falla (e.g. respuestas por reglas).
* Definir alertas ante desviaciones de comportamiento.
* Documentar todo (datasets, parámetros, experimentos, decisiones).

## Code Labs del Día 5

### Code Lab 1: Crear un Pipeline en Vertex AI

* Automatizar desde carga de datos hasta evaluación.
* Definir pasos con Vertex Pipelines.
* Almacenar outputs intermedios en GCS.

### Code Lab 2: Desplegar un modelo como API

* Tomar un modelo entrenado.
* Servirlo en Vertex AI como endpoint REST.
* Hacer consultas desde una app externa.

### Code Lab 3: Monitoreo en Producción

* Recoger métricas en tiempo real.
* Configurar alertas si el modelo responde lento o fuera de rango.
* Evaluar ejemplos mal clasificados o problemáticos.

---

## Cierre y Próximos Pasos

* Finaliza el curso intensivo de 5 días.
* Revisión de herramientas vistas:
  * Gemini APIs, embeddings, vector search, agentes, Vertex AI.
* Se invita a continuar explorando:
  * Notebooks en Kaggle.
  * Comunidad en Discord.
  * Whitepapers, podcasts y cursos adicionales de Google Cloud.
* **Mensaje final:** construir con IA generativa es posible, accesible y transformador — ahora es el momento ideal para empezar.

---

## Recursos

* Kaggle
* Google Cloud (Vertex AI, AI Studio)
* Gemini APIs
* Hugging Face Transformers
* Discord de la comunidad
* NotebookLM para análisis de documentos
