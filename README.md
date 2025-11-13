# 🎬 SentimentScope: Análisis de Sentimientos con Transformers en Reseñas de IMDB

## 🧠 Introducción al Proyecto

**SentimentScope** es un proyecto de *Deep Learning* desarrollado para **CineScope**, una empresa del sector del entretenimiento dedicada a ayudar a las audiencias a descubrir películas y series que realmente disfrutarán.

El objetivo principal es construir y ajustar un modelo basado en **Transformers** capaz de comprender el sentimiento de los usuarios (positivo o negativo) a partir de reseñas de películas del conjunto de datos **IMDB**.
Este modelo busca mejorar los sistemas de recomendación de CineScope mediante una comprensión más profunda del lenguaje y una personalización más precisa.

---

## 🎯 Objetivos del Proyecto

* Desarrollar un **modelo Transformer** adaptado para la **clasificación binaria de sentimientos**.
* Entrenar y evaluar el modelo con el **dataset de IMDB**, garantizando una alta precisión.
* Implementar una **arquitectura eficiente en PyTorch** con una canalización clara de entrenamiento, validación y prueba.
* Contribuir al perfeccionamiento del motor de recomendaciones mediante insights derivados del análisis de sentimientos.

---

## 🧩 Componentes Principales de SentimentScope

1. **Preparación de Datos**

   * Limpieza, tokenización y división del conjunto de datos en *train*, *validation* y *test*.
   * Uso de *subword tokenization* basada en **BERT (uncased)** para equilibrar eficiencia y cobertura léxica.

2. **Arquitectura del Modelo Transformer**

   * Adaptación de una arquitectura *Transformer Encoder* para tareas de clasificación.
   * Inclusión de una **capa de pooling** para condensar las representaciones de tokens en un vector único.
   * Añadido de una **capa densa final** que produce dos *logits*: positivo y negativo.

3. **Carga y Procesamiento de Datos**

   * Implementación de un **DataLoader de PyTorch** para optimizar el flujo de datos durante el entrenamiento y evaluación.

4. **Entrenamiento y Validación**

   * Definición de funciones personalizadas para el cálculo de la pérdida (*loss function*) y la optimización (*optimizer*).
   * Entrenamiento mediante un enfoque por **épocas**, garantizando un aprendizaje progresivo y estable.

5. **Pruebas y Evaluación**

   * Evaluación del modelo sobre datos no vistos.
   * Cálculo de métricas de rendimiento como **accuracy**, **precision**, **recall** y **F1-score**.

---

## ⚙️ Tecnologías Utilizadas

* **Lenguaje:** Python 3.x
* **Framework principal:** PyTorch
* **Transformers:** Biblioteca `transformers` de Hugging Face
* **Tokenización:** `BertTokenizer`
* **Procesamiento y análisis:** NumPy, Pandas
* **Visualización:** Matplotlib, Seaborn
* **Dataset:** IMDB Reviews Dataset (50,000 reseñas etiquetadas)

---

## 🔍 Diferencias Clave con Modelos Generativos

| Aspecto                 | Modelos Generativos                         | Modelo de Clasificación (SentimentScope)      |
| ----------------------- | ------------------------------------------- | --------------------------------------------- |
| **Tarea principal**     | Predicción del siguiente token              | Predicción del sentimiento del texto completo |
| **Estructura de datos** | Secuencias continuas con ventana deslizante | Reseñas independientes con etiquetas binarias |
| **Tokenización**        | A nivel de carácter                         | Subword (*BERT-based-uncased*)                |
| **Salida**              | Probabilidad por token                      | Vector de logits (positivo/negativo)          |
| **Entrenamiento**       | Muestreo continuo                           | Entrenamiento por épocas completas            |

---

## 🧪 Flujo de Trabajo

1. **Carga del dataset IMDB**
2. **Preprocesamiento y tokenización**
3. **Configuración del modelo Transformer**
4. **Definición de funciones de entrenamiento y validación**
5. **Ejecución del entrenamiento**
6. **Evaluación sobre datos de prueba**
7. **Análisis de resultados y visualización de métricas**

---

## 📊 Resultados Esperados

* Precisión superior al **90%** en el conjunto de prueba.
* Curvas de pérdida y precisión estables a lo largo de las épocas.
* Interpretabilidad de resultados mediante *attention visualization* (opcional).

---

## 💡 Aprendizajes Clave

* Comprensión de la adaptación de Transformers para tareas de clasificación.
* Dominio del flujo completo de **entrenamiento supervisado en PyTorch**.
* Manejo eficiente de grandes volúmenes de texto y optimización de *tokenizers*.

---

## 🧰 Próximos Pasos

* Implementar técnicas de **fine-tuning** con modelos preentrenados como *BERT-base-uncased*.
* Extender la clasificación a múltiples sentimientos (*multi-class classification*).
* Integrar el modelo en una API REST con *FastAPI* o *Flask* para uso en producción.

---

## 👨‍💻 Autor

**Jeffersson Hermano**
Estudiante de Economía, Ciencia de Datos y Big Data
Apasionado por la estadística, la programación y la inteligencia artificial aplicada a problemas reales.

📍 *Perú*
📧 [Tu correo o LinkedIn opcional]

---

¿Quieres que te agregue también un bloque de ejemplo de código (por ejemplo, cómo instanciar el modelo y entrenarlo) al final del README para hacerlo más completo? Puedo incluirlo con formato Markdown listo para GitHub.
