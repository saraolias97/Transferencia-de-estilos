# 🎨 Transferencia de Estilo con Redes Neuronales Convolucionales (CNN) 🖼️

¡Bienvenido a la documentación de mi proyecto de **Transferencia de Estilo**!

Este trabajo explora la fascinante capacidad de las **Redes Neuronales Convolucionales (CNN)** para fusionar el **contenido de una imagen** (por ejemplo, una foto) con el **estilo artístico de otra** (por ejemplo, una pintura famosa).

---

## 💡 Conceptos Centrales

El método se basa en el algoritmo propuesto por *Gatys et al.* y requiere la comprensión de dos elementos clave que la CNN extrae de las imágenes:

- **Representación de Contenido:**  
  Se captura a partir de las activaciones de las capas superiores de la CNN.

- **Representación de Estilo:**  
  Se obtiene mediante la **matriz de Gram** de las activaciones de las capas intermedias, midiendo las correlaciones entre los *feature maps*.

---

## 🛠 Tecnologías y Método

El proyecto fue desarrollado utilizando el **framework de Python** y bibliotecas de **Machine Learning** enfocadas en *Deep Learning*.

---

## 📊 Algoritmo y Arquitectura

La red neuronal utiliza una arquitectura **VGG-19** preentrenada, aunque se realiza una modificación al **no emplear las capas Fully Connected**.

---

## 🧪 Experimentos Realizados

Se llevaron a cabo varios experimentos para analizar la robustez y los desafíos del algoritmo, buscando optimizar la imagen generada:

1. **Variación de Estilo y Contenido:**  
   Ajuste de los pesos (`α` y `β`) que controlan la importancia relativa entre la pérdida de estilo (`L_estilo`) y la pérdida de contenido (`L_contenido`).

2. **Variación del Orden de las Capas:**  
   Se alteró la selección de las capas de la CNN para calcular las pérdidas de estilo y contenido.

3. **Inicialización del Descenso de Gradiente:**  
   Se probó inicializar la imagen generada con la imagen de contenido original vs. una imagen inicializada con ruido.

4. **Transferencia de Estilo Fotorrealista:**  
   Exploración de técnicas para transferir estilos manteniendo un alto grado de realismo fotográfico.

---

## ⚠️ Conclusiones y Desafíos Principales

El proyecto concluye que, si bien la transferencia de estilo es poderosa, presenta dos grandes desafíos:

- **Fuga de Contenido (*Content Leakage*):**  
  Al buscar una fidelidad muy alta al estilo, se produce una pérdida significativa del contenido original, haciendo que la imagen resultante no se parezca a la fuente.

- **Ajuste de Parámetros:**  
  Resulta difícil encontrar un conjunto de hiperparámetros (`α` y `β`) que funcionen óptimamente para cualquier par de imágenes, lo que requiere un ajuste manual para cada caso.

---

## ⭐ Resultados

> ¡Echa un vistazo al archivo para poder ver el código y los resultados de los experimentos! 🚀
