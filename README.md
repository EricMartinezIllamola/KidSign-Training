# KidSign-Training

## ¿Qué es KidSign?

KidSign es una aplicación web de juegos educativos para niños.

KidSign persigue tres objetivos:
- Ofrecer a los centros educativos una herramienta complementaria para que los niños aprendan el abecedario y los números en varios idiomas (Inglés y Español por el momento).

- Dar a conocer, entre los más pequeños, la existencia de personas con discapacidad auditiva y el leguaje de signos que utilizan para comunicarse. Enseñando el abecedario y los números en Lenguaje de Signos Americano (ASL).

- Conseguir que los niños aprendan, a la vez que juegan y se divierten.

El proyecto está formado por tres partes (frontend, backend y data), este repositorio contiene la parte de data.

Otros links de interés:

- Aplicacción web: 

- Codigo frontend: 

- Codigo backend: 

## ¿Training?

Para crear la aplicación de detección de signos a tiempo real, hemos entrenado varios modelos de Machine Learning. En concreto, el objetivo era obtener tres modelos distintos: uno para detectar números, otro para detectar letras y otro para detectar tanto números como letras.

## Proceso y Tecnologias

- Para entrenar los modelos hemos utilizado Python, concretamente TensorFlow. 

- En la mayoria de casos, también hemos utilizado instancias de notebooks de Google Cloud (CPU o GPU), para entrenar los modelos en menos tiempo.

- Por último, hemos utilizado TensorFlow.js tanto para convertir los modelos a formato JavaScript, como para utilizarlos en nuestra aplicación web (React).

## Contenido del Repositorio

Cada una de las carpetas (num, alphabet y global) contiene:

- Un README general: con links del dataset utilizado y de los dos modelos seleccionados (en formato JavaScript).

- Una carpeta por cada modelo entrenado (seleccionado o no seleccionado): README resumen, notebooks con todos los detalles y el modelo en formato Python (sólo en el caso de los números, en los otros casos los modelos pesaban demasiado para colgarlos).

## Modelo

El entrenamiento de los modelos toma como referencia, y punto de partida, los resultados del Proyecto Traductor de Lengua de Signos. 

Repositorio proyecto referencia: https://github.com/ecabestadistica/sign-language-translator-python-opencv.git

En este repositorio se puede encontrar información relativa al entrenamiento de dos modelos, uno capaz de detectar los números y el otro las letras. Los dos modelos con un nivel de acierto considerable (val_acc = 0.91 y 0.85 respectivamente).

Destacar cuatro aspectos que hemos incorporado del proyecto de referencia antes mencionado:

- Datasets: hemos utilizado los mismos datasets, aunque con variaciones.

- ImageDataGenerator: lo hemos utilizado para cargar y preprocesar las imágenes por lotes.

- Transferencia de conocimiento con VGG19: VGG19 es un modelo pre-entrenado con más de un millón de imágenes, del cual hemos congelado las 6 primeras capas, para entrenar el resto.

Información extra sobre la transferencia de conocimiento con VGG19: https://koushik1102.medium.com/transfer-learning-with-vgg16-and-vgg19-the-simpler-way-ad4eec1e2997

- Hiperparámetros: SGD (stochastic gradient descent) como optimizador, 0.02 de learning rate y bach size de 32 para el modelo de los números y 64 para las letras.

A partir de aquí, nuestros objetivos eran: mejorar el nivel de acierto de los modelos, crear un nuevo modelo capaz de detectar tanto números como letras y transformar los modelos para poderlos utilizar con React.

## Conclusiones

De todos los hiperparámetros que hemos ido modificando, destacar tres:

- Monitor (¿Accuracy o Validation Accuracy?): 

- Número de neuronas de la última capa densa (antes de la softmax): 

- Número de iteraciones (epoch): 