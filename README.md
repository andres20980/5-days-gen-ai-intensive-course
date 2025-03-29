# 5-Day Gen AI Intensive Course - Recursos Personales

## Descripción General

Este repositorio contiene mis notas personales, ejemplos de código (si aplica) y recursos acumulados durante mi participación en el curso intensivo de 5 días sobre Inteligencia Artificial Generativa (probablemente ofrecido por Google/Kaggle). El objetivo es organizar los materiales y seguir el progreso a lo largo del curso.

## Información del Curso (Según lo recopilado)

* **Nombre:** 5-Day Gen AI Intensive Course
* **Duración:** 5 Días
* **Tema Principal:** Inteligencia Artificial Generativa (Gen AI)
* **Formato:** Tareas diarias (codelabs, whitepapers, podcasts), livestreams diarios en YouTube, soporte comunitario en Discord, proyecto final (capstone).
* **Plataformas Clave:** Kaggle, Google AI Studio, Discord, YouTube.

## Contenido del Repositorio

Actualmente, este repositorio incluye:

* **`README.md`**: Este archivo de descripción.
* **`RESOURCES.md`**: Una lista curada con enlaces importantes para la configuración del curso, documentación, livestreams y canales de comunicación (Discord). **[Accede a los Recursos aquí](./RESOURCES.md)**
* **`LICENSE`**: El repositorio utiliza la Licencia MIT. **[Ver Licencia](./LICENSE)**
* **`.gitignore`**: Archivo que especifica qué ficheros debe ignorar Git (importante para mantener secretos fuera del repositorio).
* **`.env`** (Local, no en Git): Archivo para almacenar claves API u otros secretos necesarios para ejecutar código o interactuar con servicios (como Google AI Studio o Kaggle API). **Este archivo está explícitamente ignorado por Git gracias a `.gitignore` y no debe subirse.**

*(Se podrían añadir directorios más adelante, como `/codelabs`, `/notebooks`, `/notes`, `/capstone` a medida que avance el curso).*

## Configuración Local (Para mi uso)

1.  **Clonar (si es necesario):**
    ```bash
    git clone [https://github.com/andres20980/5-days-gen-ai-intensive-course.git](https://github.com/andres20980/5-days-gen-ai-intensive-course.git)
    cd 5-days-gen-ai-intensive-course
    ```
2.  **Crear archivo `.env` local:** Si el curso o los codelabs requieren claves API (p. ej., para AI Studio), estas deben guardarse en un archivo llamado `.env` en la raíz de este repositorio. Sigue las instrucciones del curso o de `RESOURCES.md` para obtener las claves necesarias.
    * *Ejemplo de contenido para `.env`:*
        ```dotenv
        # Ejemplo: Reemplazar con claves reales
        AI_STUDIO_API_KEY=TU_CLAVE_DE_AI_STUDIO_AQUI
        # KAGGLE_API_KEY=TU_CLAVE_DE_KAGGLE_SI_ES_NECESARIA
        ```

## Estado

Repositorio en desarrollo activo durante la duración del curso.
