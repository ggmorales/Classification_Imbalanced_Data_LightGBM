Se realiza una predicción de fraudes en transacciones con tarjeta de crédito. La base de datos original fue extraida de Kaggle y está altamente desbalanceada, pues presenta transacciones que ocurrieron en dos días, 
donde tenemos 492 fraudes de un total de 284,807 transacciones. Solo contiene variables de entrada numéricas que son el resultado de una transformación PCA, ya que por confidencialidad no se muestran las variables reales.

Para el análisis se utiliza el algoritmo LightGBM, un algoritmo basado en árboles de decisión que utiliza la técnica de gradient boosting, donde combina arboles de decisión sencillos, de manera que cada nuevo miniárbol
va intentar corregir los errores del árbol anterior. Este algoritmo, a diferencia de otros algoritmos de “boosting” que dividen el árbol de acuerdo a sus niveles de profundidad, va a dividir el árbol hoja por hoja. Se ha 
optado por este algoritmo ya que tiene una gran compatibilidad con grandes conjuntos de datos, obteniendo grandes resultados con datos desbalanceados y caracterizandose especialmente por su gran velocidad de entrenamiento.

En el análisis se hace frente al desbalanceo de los datos creando nuevos datos sintéticos en el conjunto de entramiento mediante una técnica de over-sampling.
