● Descripción del dataset personalizado. 
El dataset contiene información extraída de archivos ejecutables de Windows, tanto maliciosos como benignos. Se utilizaron características híbridas, que incluyen contenido binario hexadecimal y llamadas a bibliotecas DLL (Dynamic Link Libraries). 
A continuación, se detallan características clave del dataset: 
Tamaño: 373 muestras (301 maliciosas, 72 benignas) 
Desbalance: Prevalencia de muestras maliciosas 
Características: 531 características representadas como F_1 a F_531 
Etiqueta: Columna indicando si el archivo es malicioso o no (true para malware)

● Técnicas de aprendizaje automático utilizadas y justificación de su elección. 
Random Forest (RF) 
Modelo de aprendizaje supervisado , utiliza datos etiquetados para "aprender" cómo clasificar datos no etiquetados. se utiliza para resolver problemas de regresión y clasificación, lo que lo convierte en un modelo diverso y ampliamente utilizado.

Decisión Tree (DT) 
Es una técnica de aprendizaje supervisado que se puede utilizar tanto para problemas de clasificación como de regresión, pero sobre todo se prefiere para resolver problemas de clasificación. Es un clasificador estructurado en árbol, donde los nodos internos representan las características de un conjunto de datos, las ramas representan las reglas de decisión y cada nodo hoja representa el resultado.

Support Vector Machine Learning (SVM) 
Es un tipo de algoritmo de aprendizaje supervisado que se utiliza en el aprendizaje automático para resolver tareas de clasificación y regresión; Las SVM son particularmente buenas para resolver problemas de clasificación binaria, que requieren clasificar los elementos de un conjunto de datos en dos grupos.
El objetivo de un algoritmo de máquina de vectores de soporte es encontrar la mejor línea posible, o límite de decisión, que separe los puntos de datos de diferentes clases de datos. Este límite se denomina hiperplano cuando se trabaja en espacios de características de alta dimensión. La idea es maximizar el margen, que es la distancia entre el hiperplano y los puntos de datos más cercanos de cada categoría, facilitando así la distinción de clases de datos.

Para el ejercicio se seleccionó el modelo Random Forest y Support Vector Machine Learning 

● Resultados del entrenamiento y la evaluación del modelo. 

● Análisis crítico de los resultados del modelo. 

● Interpretación del modelo y características más relevantes


