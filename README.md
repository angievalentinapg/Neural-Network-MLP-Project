<h1 align='center'>Predicción de diabetes utilizando una red Perceptrón Multicapa (MLP)</h1>

<p> 
Las Redes Neuronales Artificiales (RNA) son un modelo de inteligencia artificial inspirado en el funcionamiento del cerebro humano. Su funcionamiento se basa en imitar la forma en que las neuronas biológicas procesan la información para transmitir señales. Estas redes están diseñadas para reconocer patrones, aprender de los datos y realizar tareas específicas como clasificación, predicción y reconocimiento de imágenes. Para ello, se crea un sistema de neuronas (nodo) interconectados a una estructura similar a la de un cerebro, con el fin de aprender de sus errores y mejorar continuamente.</p>

<h2>Componentes de una Red Neuronal Artificial</h2>

1. **Neuronas (o nodos):** Son las unidades básicas de procesamiento, donde neurona recibe una entrada, la procesa y produce una salida.

2. **Arquitectura de una red neuronal simple:** Una red neuronal básica tiene neuronas artificiales interconectadas en tres capas

	- **Capa de entrada:** Es la primera capa de la red y recibe los datos de entrada. Estas neuronas procesan los datos, los analizan/clasifican y esta información se pasa a la siguiente capa.
	- **Capa oculta:** Esta capa toma su entrada de la capa de entrada o de otras capas ocultas. Estas capas realizan cálculos complejos y transformaciones sobre los datos para ser entregados a la siguiente capa. Las RNA pueden tener una o varias capas ocultas.
	- **Capa de salida:** Es la última capa que proporciona el resultado final del procesamiento de la red. Esta puede tener una o varias neuronas de salida, dependiento del problema que se esté analizando. </p>

3. **Pesos:** Cada conexión entre neuronas tiene un peso asociado, el cual es un conjunto de parámetros adaptativos, donde estos se utilizan como multiplicadores de las neuronas de entrada y, finalmente, dichos productos se suman para obtener la combinación lineal de las entradas, esto determina la importancia de la entrada. 

4. **Sesgos:** Son errores sistemáticos o una desviación del resultado verdadero o deseado, que puede conducir a resultados injustos o inexactos. Estos valores se suman a la entrada ponderada antes de aplicar la función de activación. 

5. **Función de activación:** Las funciones de activación introducen no linealidad en la red, permitiendo que pueda aprender y representar relaciones complejas entre entradas y salidas. Estas funciones transforman la señal de entrada de una neurona en una señal de salida que pasa a la capa siguiente. Ejemplos comunes son la función sigmoide, ReLU (Rectified Linear Unit) y tanh (tangente hiperbólica). 


<h2>Perceptrón Multicapa (MLP)</h2>

El Perceptrón Multicapa (MLP, por sus siglas en inglés) es una RNA que se utiliza en el aprendizaje supervisado. Esta red es capaz de realizar tareas de clasificación y regresión, por lo cual, puede ser utilizada para problemas en los que la relación entre las entradas y las salidas no es lineal. Su objetivo es identificar los valores óptimos para los parámetros puedan clasificar lo mejor posible.

El algoritmo de entrenamiento utilizado se basa en la propagación hacia atrás (backpropagation), que ajusta los pesos de las conexiones de la red para minimizar el error de predicción entre las salidas producidas por la red y las salidas deseadas. Este proceso se realiza como una “caja negra” que tiene entradas, parámetros de ajuste y salidas. Una MLP se debe entrenar con datos para encontrar el ajuste perfecto de estos parámetros. De esta manera, se reciben las variables de los registros, toma el primer registro, entrega resultados y hace un ajuste; luego recibe las variables del segundo registro, entrega resultados y nuevamente hace un ajuste; y así por cada uno de los registros. Cada ajuste o iteración es conocido como una época.

<h2>Arquiectura empleada en el modelo de predicción de diabetes</h2>

Para este caso, se tiene un problema de clasificación binaria, donde el modelo definido es una red neuronal conectada (densa) con la siguiente arquitectura:

- **Capa de entrada:** Recibe 8 características de entrada.
- **Primera capa oculta:** 16 neuronas, activación ReLU.
- **Segunda capa oculta:** 32 neuronas, activación ReLU.
- **Tercera capa oculta:** 16 neuronas, activación ReLU.
- **Cuarta capa oculta:** 8 neuronas, activación ReLU.
- **Capa de salida:** 1 neurona, activación sigmoide.

Al ser un problema de clasificación binaria donde se debe predecir la presencia o no de diabetes (0 y 1), se emplea una función de activación sigmoide donde la neurona de salida se puede interpretar como una probabilidad.

<p align="center"> 
  <img src="https://github.com/angievalentinapg/Neural-Network-MLP-Project/blob/main/Architecture.jpg" alt="RNA" width="861" height="337"/>
  <p align="center"> <b>Figura 1.</b> Arquitectura de la MLP implementada.</p>
</p>

<h2>Lenguaje y librerías utilizadas</h2>

<p align="center"> 
    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/>
    <img src="https://www.vectorlogo.zone/logos/tensorflow/tensorflow-icon.svg" alt="tensorflow" width="40" height="40"/>
    <img src="https://matplotlib.org/stable/_static/logo_light.svg" alt="matplotlib" width="70" height="30"/>
    <img src="https://raw.githubusercontent.com/devicons/devicon/2ae2a900d2f041da66e950e4d48052658d850630/icons/pandas/pandas-original.svg" alt="pandas" width="40" height="40"/>
    <img src="https://upload.wikimedia.org/wikipedia/commons/0/05/Scikit_learn_logo_small.svg" alt="scikit_learn" width="40" height="40"/>
    <img src="https://seaborn.pydata.org/_images/logo-mark-lightbg.svg" alt="seaborn" width="40" height="40"/>  
    <img src="https://upload.wikimedia.org/wikipedia/commons/3/31/NumPy_logo_2020.svg" alt="numpy" width="70" height="40"/>
</p>

----

<h3>Referencias</h3>

- AWS. ¿Qué es una red neuronal?. [En línea]. Disponible en: https://aws.amazon.com/es/what-is/neural-network/
- IBM. Arquitectura (Perceptrón multicapa). [En línea]. Disponible en: https://www.ibm.com/docs/es/spss-statistics/saas?topic=perceptron-architecture-multilayer
