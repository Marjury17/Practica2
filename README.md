1.	Descripción del dataset personalizado. 
El dataset contiene información extraída de archivos ejecutables de Windows, tanto maliciosos como benignos. Se utilizaron características híbridas, que incluyen contenido binario hexadecimal y llamadas a bibliotecas DLL (Dynamic Link Libraries). 
A continuación, se detallan características clave del dataset: 
Tamaño: 373 muestras (301 maliciosas, 72 benignas) 
Desbalance: Prevalencia de muestras maliciosas 
Características: 531 características representadas como F_1 a F_531 
Etiqueta: Columna indicando si el archivo es malicioso o no (true para malware)
 Nota: Las características binarias se representan numéricamente por simplicidad (F_1, F_2, etc.)

2.	Técnicas de aprendizaje automático utilizadas y justificación de su elección. 
Random Forest (RF) 
es un modelo de aprendizaje supervisado ; utiliza datos etiquetados para "aprender" cómo clasificar datos no etiquetados. se utiliza para resolver problemas de regresión y clasificación, lo que lo convierte en un modelo diverso y ampliamente utilizado.

Decisión Tree (DT) 
Es una técnica de aprendizaje supervisado que se puede utilizar tanto para problemas de clasificación como de regresión, pero sobre todo se prefiere para resolver problemas de clasificación. Es un clasificador estructurado en árbol, donde los nodos internos representan las características de un conjunto de datos, las ramas representan las reglas de decisión y cada nodo hoja representa el resultado.

Support Vector Machine Learning (SVM) 
Es un tipo de algoritmo de aprendizaje supervisado que se utiliza en el aprendizaje automático para resolver tareas de clasificación y regresión; Las SVM son particularmente buenas para resolver problemas de clasificación binaria, que requieren clasificar los elementos de un conjunto de datos en dos grupos.
El objetivo de un algoritmo de máquina de vectores de soporte es encontrar la mejor línea posible, o límite de decisión, que separe los puntos de datos de diferentes clases de datos. Este límite se denomina hiperplano cuando se trabaja en espacios de características de alta dimensión. La idea es maximizar el margen, que es la distancia entre el hiperplano y los puntos de datos más cercanos de cada categoría, facilitando así la distinción de clases de datos.

Para el ejercicio se seleccionó el modelo Random Forest y Support Vector Machine Learning, por sus siguientes características.
Random Forest: es menos sensible a ruido y datos atípicos debido a su capacidad para promediar múltiples árboles de decisión.
SVM: es más sensible a ruido y datos atípicos, ya que intenta encontrar el hiperplano que mejor separa las clases y puede verse afectado por puntos de datos extremos.
Random Forest: proporciona importancias de características que indican la contribución de cada característica a la predicción, pero puede ser difícil de interpretar debido a la complejidad de múltiples árboles.
SVM: proporciona vectores de soporte que son las instancias más cercanas al hiperplano de separación. Esto puede proporcionar una interpretación más clara de cómo se toman las decisiones de clasificación.
Random Forest: puede manejar eficazmente conjuntos de datos con muchas características debido a la selección aleatoria de subconjuntos de características en cada árbol.
SVM: puede funcionar bien en espacios de características de alta dimensión, pero puede volverse computacionalmente costoso a medida que aumenta el número de características.
Random Forest: puede ser más rápido de entrenar y predecir en conjuntos de datos grandes en comparación con SVM, especialmente cuando se utilizan pocos árboles y características.
SVM: el tiempo de entrenamiento y predicción puede ser más largo, especialmente en conjuntos de datos grandes o con kernels no lineales.
Random Forest: los parámetros clave incluyen el número de árboles, la profundidad máxima del árbol y el número mínimo de muestras requeridas para dividir un nodo.
SVM: los parámetros clave incluyen el tipo de kernel (lineal, RBF, polinomial), el parámetro de regularización C y los parámetros específicos del kernel (como el coeficiente gamma en el kernel RBF).

3.	Resultados obtenidos
Modelo Random Forest
Para el modelo se usó el parámetro del número de árboles de decisión que se utilizarán en el Bosque Aleatorio. En este caso, se están utilizando 10 árboles, para este caso el modelo de aprendizaje tuvo una precisión del 0.97.
Precision:
La precisión mide la proporción de las instancias clasificadas como positivas que son realmente positivas. 
Para la clase 0 (no malicioso), la precisión es del 100%. Esto significa que todas las instancias que el modelo predijo como clase 0, el 100% de ellas eran realmente no malicioso.
Para la clase 1 (maliciosos), la precisión es del 89%. Esto indica que el 89% de las instancias que el modelo predijo como clase 1 eran realmente malicioso, mientras que el 11% eran falsos positivos.
Recall:
El recall mide la proporción de las instancias que realmente son positivas y que el modelo predijo correctamente como positivas. 
Para la clase 0, el recall es del 97%. Esto significa que el 97% de las instancias que realmente eran de la clase 0 fueron identificadas correctamente por el modelo.
Para la clase 1, el recall es del 100%. Esto indica que todas las instancias que realmente eran de la clase 1 fueron identificadas correctamente por el modelo.
F1-score:
El F1-score es la media armónica de la precisión y el recall. Proporciona una medida única del rendimiento del modelo que tiene en cuenta tanto la precisión como el recall.
Para la clase 0, el F1-score es del 98%. Esto indica un buen equilibrio entre precisión y recall para la clase 0.
Para la clase 1, el F1-score es del 94%. Esto también indica un buen equilibrio entre precisión y recall para la clase 1.
En conclusión, estos resultados indican que el modelo de Random Forest tiene un buen rendimiento en la clasificación de ambas clases, con altas precisiones y recalls. Sin embargo, el rendimiento es ligeramente mejor para la clase 0 en comparación con la clase 1.
AUC-ROC
Es una métrica utilizada para evaluar la calidad de un modelo de clasificación binaria. La curva ROC (Receiver Operating Characteristic) es una representación gráfica que muestra la relación entre la tasa de verdaderos positivos (TPR) y la tasa de falsos positivos (FPR) en diferentes umbrales de clasificación.
Un valor de AUC-ROC cercano a 1 indica un modelo con un excelente rendimiento, mientras que un valor de 0.5 indica un modelo que clasifica las instancias al azar.

Para los modelos seleccionados el valor de AUC-ROC es de 0.9833 por lo cual el modelo tiene un rendimiento muy bueno en la tarea de clasificación binaria, con una alta capacidad para distinguir entre clases positivas y negativas.

Support Vector Machine Learning (SVM)
Al aplicar el modelo SVM, se tuvo el mismo resultado que el modelo Random Forest, por lo cual se puede concluir que los dos modelos tienen una muy buena capacidad de distinguir una clasificación binaria.

