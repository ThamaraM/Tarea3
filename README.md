# Tarea 3: Variables Aleatorias Múltiples
Modelos Probabilísticos de señales y sistemas.

Thamara Montero Montoya. B64577.

Asignaciones de la tarea 3.


# Curva de ajuste para las funciones de densidad marginales de X y Y.
En las imágenes que se muestran a continuación es posible observar las funciones de densidad marginales tanto de X como de Y. Estas imágenes se obtuvieron gracias a las herramientas para analizar datos de Python.



![](ajustex.png) ![](ajustey.png)




Considerando el comportamiento de ambas curvas observable en la sección 4. las cuales tienen tendencia a tener simetría en el origen se busca ajustar la curva a una distribución normal, la cual se puede definir mediante la siguiente ecuación matemática:



<p align="center">
  <img src="https://render.githubusercontent.com/render/math?math={ f }_{ x }\left( x \right) =\frac { 1 }{ \sqrt { 2\pi { \sigma  }_{ x }^{ 2 } }  } { e }^{ \left\lfloor \frac { -{ \left( x-{ \mu  }_{ x } \right)  }^{ 2 } }{ 2{ \sigma  }_{ x }^{ 2 } }  \right\rfloor  }">  
</p>



Para el caso de x, y para el caso de y la siguiente:



<p align="center">
  <img src="https://render.githubusercontent.com/render/math?math={ f }_{ y }\left( y \right) =\frac { 1 }{ \sqrt { 2\pi { \sigma  }_{ y }^{ 2 } }  } { e }^{ \left\lfloor \frac { -{ \left( y-{ \mu  }_{ y } \right)  }^{ 2 } }{ 2{ \sigma  }_{ y }^{ 2 } }  \right\rfloor  }">  
</p>

Ecuaciones que se introdujeron en el código junto con la herramienta de *curve_fit* y los datos de mu=9.904843810018251 y sigma=3.2994428643069567 para X y mu=15.079460901835715 y sigma=6.026937742803979 para Y obtenidos del mismo.


# Expresión de la función de densidad conjunta que modela los datos.

Al asumir X y Y como dos variables independientes la función de densidad conjunta está dada por la multiplicación de las funciones de densidad marginals de cada una de las variables, por lo que, teniendo en cuenta las ecuaciones mencionadas anteriormente y los valores de sigma y mu para ambas variables, matemáticamente se podría ver en la siguiente ecuación la expresión de la función de densidad conjunta:

<p align="center">
  <img src="https://render.githubusercontent.com/render/math?math={ f }_{ x, y }\left( x, y \right) =\left( \frac { 1 }{ \sqrt { 2\pi { \cdot 3.2994 }^{ 2 } }  } { e }^{ \left\lfloor \frac { -{ \left( x-9.9048 \right)  }^{ 2 } }{ 2\cdot { 3.2994 }^{ 2 } }  \right\rfloor  } \right) \cdot \left( \frac { 1 }{ \sqrt { 2\pi { \cdot 6.0269 }^{ 2 } }  } { e }^{ \left\lfloor \frac { -{ \left( x-15.0796 \right)  }^{ 2 } }{ 2{ \cdot 6.0269 }^{ 2 } }  \right\rfloor  } \right) ">  
</p>


# Valores de correlación, covarianza y coeficiente de correlación (Pearson) para los datos y su significado.

* Correlación


<p align="center">
  <img src="https://render.githubusercontent.com/render/math?math={ R }_{ XY }= 149.54281000000012 ">  
</p>


Es el momento de segundo orden, el cual determina el grado de asociación lineal de dos variables aleatorias. Para determinar la correlación de dos variables es necesario utilizar la siguiente fórmula dado que se asumió independencia estadística entre las variables, lo cual garantiza que no estén correlacionadas:
<p align="center">
  <img src="https://render.githubusercontent.com/render/math?math={ R }_{ XY }=E\left[ X \right] E\left[ Y \right] =9.904843810018251\cdot 15.079460901835715=149.359705 ">  
</p>

Se puede deducir del valor dado previamente de correlación que al ser el mismo que el de la ecuación queda comprobado que no existe la correlación entre ambas variables. Es importante aclarar que si existiese correlación esta no implicaría causalidad, es decir, el comportamiento de una no afecta a la otra.


* Covarianza


<p align="center">
  <img src="https://render.githubusercontent.com/render/math?math={ C }_{ XY }= 0.18310502804041562 ">  
</p>

Para determinar si dos variables son independientes es necesario que el valor de la covarianza sea igual a 0, anteriormente se asumió que ambas variables aleatorias eran independientes, además, en el inciso anterior se obtiente el valor de la correlación y se comprueba de acuerdo a este dado su independencia.

Ahora bien, del valor obtenido para la covarianza se puede observar su cercanía a 0, por lo que,  se puede corroborar, una vez más, la independencia de las variables estudiadas.


* Coeficiente de correlación

<p align="center">
  <img src="https://render.githubusercontent.com/render/math?math=\rho =\frac { { C }_{ XY } }{ { \sigma  }_{ X }{ \sigma  }_{ Y } } =0.009207950005810454">  
</p>

Este momento de segundo orden se encuentra entre los valores de -1 y 1, y corresponde a la medida en que dos variables aleatorias dependen linealmente una de la otra. Su valor, negativo o positivo, determina el valor de la correlación, ya sea positiva o negativa. Si el valor de este momento es cero indica que no existe relación lineal entre las variables aleatorias.

Como se puede observar que el valor obtenido para el coeficiente de correlación es prácticamente 0, por lo que no existe relación lineal entre las mismas.


# Funciones de densidad marginales (2D), la función de densidad conjunta (3D).
A continuación se pueden observar las funciones de densidad marginales de x y y mencionadas en secciones anteriores.
## Funciones marginales:
![](marginalx.png) ![](marginaly.png)

Finalmente, la función de densidad conjunta corresponde a la siguiente.
## Función de densidad conjunta:
![](densidad_conjunta.png)
