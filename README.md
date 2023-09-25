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
