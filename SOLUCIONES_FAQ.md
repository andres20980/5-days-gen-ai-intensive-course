# Solución de Problemas y Preguntas Frecuentes (Día 0)

Información extraída de la guía oficial del curso para resolver dudas comunes.
Fuente: [https://www.kaggle.com/code/markishere/day-0-troubleshooting-and-faqs/](https://www.kaggle.com/code/markishere/day-0-troubleshooting-and-faqs/)

## Preguntas Frecuentes (FAQ)

* **¿Cómo envío el trabajo del curso?**
    No es necesario enviar las tareas diarias. La insignia del curso de Kaggle se otorgará al participar activamente (ejecutando los codelabs que "Copias y ejecutas") y al completar el proyecto final opcional.

* **¿Cuánto tiempo tengo para hacer el trabajo del curso?**
    Se recomienda seguir el ritmo diario para poder participar en las discusiones de Discord y los livestreams con preguntas relevantes. Sin embargo, no hay una obligación estricta de completar las tareas en el mismo día.

* **¿Se me cobrará por usar esta clave API (AI Studio/Gemini)?**
    Por defecto, AI Studio te configura en el nivel gratuito (*free tier*). Puedes verificar el estado y los límites de tu clave API directamente en la página de gestión de claves API dentro de AI Studio.

## Errores Comunes y Soluciones

* **"Este número de teléfono no se puede verificar en Kaggle"**
    * Asegúrate de que tu número de teléfono no esté registrado en ninguna lista "No Llamar" (Do Not Call registry).
    * Verifica que has introducido correctamente el código de país y el código de área.

* **"Sin acceso a Internet" (dentro de un Notebook de Kaggle)**
    * Asegúrate de haber iniciado sesión correctamente en tu cuenta de Kaggle.
    * Verifica que tu número de teléfono está validado en tu perfil de Kaggle (ver FAQ sobre verificación).
    * Comprueba que la opción de "Internet" está habilitada en la configuración del propio Notebook de Kaggle (Settings -> Internet -> On).

* **"ResourceExhausted: 429 Se ha agotado el recurso" (Error de API Gemini)**
    * Este error indica que has superado la cuota de solicitudes por minuto para el modelo de API Gemini que estás utilizando (cada modelo tiene su propia cuota).
    * **Solución:** Espera aproximadamente 60 segundos y vuelve a intentar realizar la solicitud a la API.

* **"InvalidArgument" o Clave API no válida (Error de API Gemini)**
    * Suele ocurrir si no has copiado la clave API completa o si has incluido caracteres adicionales (como espacios) al copiarla/pegarla.
    * **Solución:** Vuelve a copiar cuidadosamente tu clave API desde AI Studio y asegúrate de que esté completa y exacta en tu código o variable de entorno.

* **Mensaje: "Nota: es posible que debas reiniciar el kernel para usar los paquetes actualizados"**
    * Este mensaje aparece a menudo después de usar `pip install` en un notebook.
    * **Solución:** En el contexto de este curso, generalmente puedes ignorar este mensaje. No es necesario reiniciar el kernel después de las instalaciones de paquetes indicadas en los codelabs.
