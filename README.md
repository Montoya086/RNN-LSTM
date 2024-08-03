# RNN-LSTM
 
## Preguntas
### Parte 1
**¿Qué interpretación le da a la separación de las graficas de training y validación?**

En esta gráfica se puede observar que, como es esperado, ambas tienen una disminución en la perdida respecto a las 
épocas. Se puede observar que en el entrenamiento la perdida es mucho mayor que durante la validación, esto se espera
de un modelo el cual tiene overfit, por lo que la validación no logrará generalizar de forma adecuada los datos.

**¿Cree que es un buen modelo basado solamente en el loss?**

Al observar la grafica se puede observar que no es un buen modelo debido a que este experimenta bastante overfitting,
pero esto no significa que no pueda realizar predicciones bastante acertadas.

**¿Cómo deberían de verse esas gráficas en un modelo ideal?**

En un modelo ideal, ambas curvas deberían de tener mucho menos espacio entre si. Esto indicaría que el modelo fue 
entrenado correctamente y este puede procesar y aprender de datos que nunca habían sido ingresados sin problema.
### Parte 2
**¿Qué modelo funcionó mejor? ¿RNN tradicional o el basado en LSTM? ¿Por qué?**

Basándonos en los resultados obtenidos, el modelo basado en RNN funciona mucho mejor a pesar de que puede ser mas ineficiente de entrenar.
En dichos resultados se puede observar que el modelo RNN tradicional tiene menor dificultad en encontrar los cambios entre "a" y "b", mientras que el modelo LSTM tiene problemas al hacer dichos cambios, colocando "EOS" en posiciones incorrectas.

**Observen la gráfica obtenida arriba, ¿en qué es diferente a la obtenida a RNN? ¿Es esto mejor o peor? ¿Por qué?**

Se puede observar que el modelo RNN tradicional tiene una pendiente de perdida mucho menos pronunciada, y este se estabiliza en las ultimas épocas. 
Por otro lado el basado en LSTM tiene una pendiente más pronunciada, lo cual puede indicar un mejor ajuste a los datos de entrenamiento. Este segundo modelo también presenta una cantidad mayor de osilaciones, lo cual puede causar inestabilidad en el modelo, lo cual puede hacerla mucho más propensa a errores.

**¿Por qué LSTM puede funcionar mejor con secuencias largas?**

Esto se debe a que los modelos LSTM están diseñados para poder memorizar y olvidar datos de forma controlada para garantizar un mejor desempeño con cadenas de gran tamaño.

### Parte 3
**Compare las graficas obtenidas en el LSTM "a mano" y el LSTM "usando PyTorch, ¿Cuál cree que es mejor? ¿Por qué?**

Se puede observar que el modelo LSTM de PyTorch posee una curva de perdida mucho más pronunciada, lo que indica que es mucho más eficiente que la realizada a mano.
El modelo de PyTorch, al igual que el realizado a mano, posee oscilaciones, pero estas son mucho menos pronunciadas lo cual no debería de ser un problema significativo.
Este modelo posee un menor espacio entre las gráficas, lo cual indica un menor overfit con respecto a las anteriores. Esto se puede ver reflejado en el resultado obtenido, el cual es mucho mejor que el obtenido anteriormente.

**Compare la secuencia target y la predicha de esta parte, ¿en qué parte falló el modelo?**

En este modelo, se puede observar que logró predecir casi a la perfección la secuencia target, pero tuvo un error a la hora de realizar la transición entre los caracteres, ya que realizó dicha transición antes de lo debido.

**¿Qué sucede en el código donde se señala "NOTA 1" y "NOTA 2"? ¿Para qué son necesarias estas líneas?**

Los comentarios que señalan NOTA 1 y NOTA 2 son líneas donde llaman el método net.eval() y net.train() respectivamente.
Estas líneas son necesarias para cambiar el estado de la red neuronal, ya que net.eval() se utiliza para evaluar la red neuronal
y net.train() se utiliza para entrenar la red neuronal. Es importante cambiar el estado de la red neuronal ya que
algunas capas se comportan distinto dependiendo el modo en el que se encuentren.