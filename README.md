#  Generador de Imágenes con Replicate y Optimización de Prompts con OpenChat 3.5

Bienvenido a mi repositorio. Aquí te presento un proyecto completo donde combino la potencia de **Replicate** para generar imágenes a partir de texto con un modelo **LLM gratuito** (OpenChat 3.5) para optimizar los prompts antes de enviarlos al generador de imágenes.

##  Descripción General

En este proyecto he creado un flujo automatizado que:
1. Solicita al usuario un **token de Replicate** para evitar que mi clave quede expuesta.
2. Permite introducir un prompt inicial.
3. Optimiza ese prompt utilizando un modelo LLM (OpenChat 3.5), completamente gratuito y accesible.
4. Genera imágenes utilizando el modelo personalizado que tengo alojado en Replicate.
5. Descarga, muestra y guarda la imagen generada.

---

## 🛠️ Tecnologías Utilizadas

He utilizado las siguientes tecnologías y bibliotecas:

- 🐍 **Python** como lenguaje principal.
- 📦 `replicate` para comunicarme con la API de Replicate.
- 🤖 `transformers` y `huggingface_hub` para cargar y utilizar el modelo LLM de OpenChat 3.5.
- 🖼️ `PIL` para manejar las imágenes generadas.
- 📊 `matplotlib` para visualizarlas directamente en el notebook.
- ☁️ `requests` para descargar las imágenes desde la URL de Replicate.

---

##  Estructura de Archivos

- `Project06_replicate_image_generator_with_token_request.ipynb`: Notebook completo con el flujo descrito.
- `README.md`: Este archivo con la documentación.
- `imagen_generada.png`: Ejemplo de imagen generada (opcional, si quieres subirla).

---

##  Explicación Paso a Paso

### 1️⃣ Solicitud del Token de Replicate
Para proteger mi cuenta, no incluyo el token directamente en el código. En su lugar, pido al usuario que lo introduzca manualmente al ejecutar el notebook. Así me aseguro de que no queda expuesto.

### 2️⃣ Configuración de la Biblioteca `replicate`
Una vez tengo el token, configuro la variable de entorno `REPLICATE_API_TOKEN` para que `replicate` lo utilice de forma segura.

### 3️⃣ Definición del Prompt Inicial
Permito al usuario introducir un primer prompt, que suele ser una descripción breve de lo que quiere generar.

### 4️⃣ Optimización del Prompt con OpenChat 3.5
Para mejorar la calidad de la imagen generada, paso el prompt inicial a **OpenChat 3.5**, un modelo de lenguaje gratuito que me devuelve una versión optimizada del prompt, mucho más detallada y lista para un generador de imágenes.

### 5️⃣ Generación de Imágenes con Replicate
Con el prompt optimizado, utilizo el modelo **franfernandez93/generador_imagen_ia** alojado en Replicate. Configuro parámetros como la resolución, el formato y la calidad.

### 6️⃣ Descarga y Visualización
Si la generación es exitosa, descargo la(s) imagen(es) desde las URLs proporcionadas por Replicate, las muestro directamente en el notebook y guardo una copia local llamada `imagen_generada.png`.

### 7️⃣ Manejo de Errores
Incluyo manejo de errores básico para asegurarme de que si algo falla (por ejemplo, si el token es incorrecto o el modelo no responde), el usuario recibe un mensaje claro.

---

## ⚠️ Nota de Seguridad

- Este notebook **no guarda tokens ni claves en el archivo**.
- El usuario debe proporcionar el token cada vez que ejecute el notebook.
- El modelo LLM utilizado (OpenChat 3.5) es **completamente gratuito y accesible sin autenticación**.

---

##  Cómo Ejecutarlo

1. Clona este repositorio:
    ```bash
    git clone https://github.com/tu-usuario/tu-repo.git
    ```
2. Abre el notebook en Google Colab o en tu entorno local.
3. Instala las dependencias:
    ```bash
    pip install replicate transformers huggingface_hub pillow matplotlib
    ```
4. Ejecuta cada celda siguiendo las instrucciones.
5. Introduce tu token de Replicate cuando se te solicite.
6. Sigue el flujo para introducir el prompt inicial y observar el resultado optimizado y la imagen generada.

---

## 🤝 Contribuciones

Siéntete libre de abrir un Pull Request o sugerir mejoras. Este es un proyecto educativo y siempre hay espacio para aprender.

---

## 📬 Contacto

Si tienes alguna duda o sugerencia, puedes contactarme a través de GitHub.

---

¡Gracias por visitar este repositorio!
