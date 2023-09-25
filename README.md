# Python-Ejercicios-MCI
Aplicaciones de la derivada y la integral 

## CODIGO DEL GRADIENTE (Diferenciación_Númerica.py)
El código que se muestra a continuación es el que se utilizó en el programa 1. El código sirve para calcular el gradiente de presión de una cama fluidizada para ello es necesario tener sus medidas de presión. En la tabla 1 se muestran dichas medidas.

TABLA I. medidas de presión de una cama fluidizada.
Posición z (m)	0	0.5	1	1.5	2.0
Presión P (kPa)	1.82	1.48	1.19	0.61	0.15

Gracias al programa 1, se podrán estimar los valores del gradiente de presión dp/dz en sus diferentes posiciones.
El código se desarrolló usando el lenguaje de programación Python utilizando el IDE Jupyter NoteBook. En primera instancia es necesario agregar algunos paquetes para que el código se compile correctamente, para trazar graficas es necesario agregar “matplotlib.pyplot”, al manipular muchos datos de lógica matemática, también es necesario agregar el paquete “numpy”, el cual permite realizar cálculos lógicos y matemáticos mediante matrices.
Para desarrollar el código es necesario entender el tema de diferenciación numérica, y dar un breve repaso de la serie de Taylor, el teorema del valor medio, diferencias hacia adelante, hacia atrás, centradas y de segundo orden. Para obtener más información consulte el capítulo 6 Diferenciación numérica de [2].
La función principal está definida por “def difer(x,y,tipo=0,orden=1)”. A través de esta función se puede seleccionar el tipo de diferenciación que se desea aplicar. En este caso en la variable “tipo” al seleccionar “-1” se le solicita al programa que realice una diferenciación hacia atrás. Cuando se selecciona “0” se está solicitando una diferenciación centrada y al ingresar el valor “1” el programa aplicará una diferenciación hacia adelante. 
En la variable “orden” se tiene la posibilidad de seleccionar una derivada de primer orden utilizando el valor “1”, y utilizando el valor “2” el programa ejecutará una derivada de segundo orden. 
Mediante la codificación de las fórmulas de diferenciación y de la serie de Taylor es como el código logrará ejecutar todas las operaciones solicitadas. Por último se le solicita al programa que grafique los resultados obtenidos mediante la instrucción “fig = plt.figure()”, y para mostrar la gráfica en pantalla se utiliza la instrucción “plt.show()”.

## CODIGO CONTROLADOR PID (ApliMat_PID.py)
El código mostrado en el programa 2, sirve para graficar el comportamiento de un controlador PID mediante el lenguaje de programación Python utilizando el IDE Jupyter NoteBook. En primera instancia es necesario agregar algunos paquetes para que el código se compile correctamente, para trazar graficas es necesario agregar “matplotlib.pyplot”, para resolver integrales es necesario incluir “scipy.integrate”, al manipular muchos datos de lógica matemática, también es necesario agregar el paquete “numpy”, el cual permite realizar cálculos lógicos y matemáticos mediante matrices. 
El código se desarrolla a partir de la fórmula 27, mostrada en la sección II.2, obteniendo su función de transferencia en la fórmula 29. A partir de estas dos ecuaciones se plantea el código del programa 2.
Es necesario escribir la fórmula 27 de forma que el lenguaje de programación reconozca cada dato que se desea ingresar, por ello a lo largo del programa se hace uso de variables que toman el valor de cada dato necesario para dar solución a la fórmula. 
 Al avanzar en la escritura del código se puede observar que se trata de un controlador PID que se utiliza para calentar continuamente la corriente de líquido que fluye a través de un tanque. En este caso el controlador PID se utiliza para obtener la temperatura configurada en dicho tanque. 
Una vez que se han definido cada una de las variables necesarias para obtener un resultado numérico del funcionamiento del controlador PID, solo faltará representar este resultado de forma gráfica.
Para graficar los resultados obtenidos basta con utilizar plt.xlabel('Time'), de esta forma el eje X tomará los valores del tiempo que el controlador PID vaya generando. En el caso del eje Y se utiliza plt.ylabel('Temperature'), para graficar los valores de temperatura que el controlador PID genere. Cuando los datos que se desean graficar han sido ordenados, se le indica al programa que grafique la solución obtenida a partir de la fórmula 27, para esto se utiliza plt.plot(tspan,sol), en la línea de código anterior se encuentra contenida la solución o el comportamiento del controlador PID, en formato de vector. En donde “tspan” especifica el intervalo de tiempo durante el que actúa el controlador PID, indicando el tiempo inicial y final de un vector de dos números. 

##
El programa 3 muestra el código para resolver integrales dobles y graficar el resultado que se obtiene. (Integral_Doble.py)

En el código se agregan algunos paquetes para que se compile correctamente. Para trazar graficas es necesario agregar “matplotlib.pyplot”, al manipular muchos datos de lógica matemática, también es necesario agregar el paquete “numpy”, el cual permite realizar cálculos lógicos y matemáticos mediante matrices. Con el paquete “from scipy.integrate import dblquad”, el código tendrá la capacidad de resolver integrales dobles.
En este caso se necesita graficar el resultado obtenido en 3D, para ello se utiliza la instrucción “ax = fig.add_subplot(1, 2, 2, projection='3d')”, mediante esta instrucción se definen las medidas que tendrá el eje Y,X,Z.  
