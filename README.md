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

**Observen la gráfica obtenida arriba, ¿en qué es diferente a la obtenida a RNN? ¿Es esto mejor o peor? ¿Por qué?**

**¿Por qué LSTM puede funcionar mejor con secuencias largas?**

### Parte 3
**Compare las graficas obtenidas en el LSTM "a mano" y el LSTM "usando PyTorch, ¿cuál cree que es mejor? ¿Por qué?**

**Compare la secuencia target y la predicha de esta parte, ¿en qué parte falló el modelo?**

**¿Qué sucede en el código donde se señala "NOTA 1" y "NOTA 2"? ¿Para qué son necesarias estas líneas?**
