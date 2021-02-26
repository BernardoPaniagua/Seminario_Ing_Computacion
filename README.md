# Optimización
> Este documento es una clase en Python que contiene varios métodos para minimizar una función.
## Índice
* [Supuestos](#supuestos)
* [Parámetros](#parámetros)
* [Diagrama general](#diagrama-general)
* [gradiente](#technologies)
* [hessiana](#hessiana)
* [es optimo](#setup)
* [wolfe](#features)
* [aplha](#status)
* [volver_pd](#volver_pd)
* [busqueda_lineal_newton](#busqueda_lineal_newton)
* [BFGS](#BFGS)
* [comparación](#comparación)
* [Ejemplos](#ejemplos)
## Supuestos
* La función es continua.
* La función es dos veces diferenciable en los reales.
* Buscamos el mínimo (local) de la función.
## Parámetros
* function: es la función a optimizar. Puede ser una función def de Python o una "lambda x"; hay ejemplos más adelante.
* max_iters: iteraciones máximas que se van a realizar si no se cumple la tolerancia, si no se indica se utilizarán 300. Generalmente, arriba de 200 iteraciones la precisión no mejora significativamente.
* tol: Es la precisión que se pide a los algortimos para decidir si se llegó a un mínimo.
## Diagrama general
![Example screenshot](./img/diagramaSeminario.PNG)
## gradiente
Calcula el vector de derivadas parciales de la función f en un punto x en específico.
## hessiana
Calcula la matriz de segundas derivadas parciales de f en un punto x en específico.
## es_optimo
Regresa verdadero si se cumple la tolerancia para un punto x, y falso en caso contrario.
## wolfe
Dada una $alpha$, verifica si se cumplen las condiciones de Wolfe para un punto x.
## alpha
Dada x, calcula iterativamente $alpha$ hasta que cumpla las condiciones de Wolfe
## volver_pd
Dada una **matriz** x, verifica si es positiva definida, si lo es regresa x, si no la convierte en positiva definida y regresa la matriz modificada
## busqueda_lineal_newton
Minimiza la función f, partiendo desde el punto inicial x, utilizando el algoritmo de búsqueda lineal de Newton. Sus otros parámetros, modificada y comparación, son booleanos que indican si se quiere usar búsqueda lineal modificada de Newton, y si se quiere hacer comparaciones, respectivamente. Si no se indican se toman como falsos. Regresa el punto óptimo donde se encontró el mínimo de f.
## BFGS
Minimiza la función f, partiendo desde el punto inicial x, utilizando el algoritmo BFGS. El parámetro comparación es un booleano que es verdadero si se quieren hacer comparaciones, y falso en otro caso; si no se indica se toma como falso. Regresa el punto xk donde se encontró el mínimo de f.
## comparacion
Si comparacion es verdadero en alguno de los algoritmos de minimización, se llama a esta función. Realiza la minimización por búsqueda lineal de Newton, así como por su versión modficada, y por BFGS, toma los tiempos de cada uno y los grafica.
## Ejemplos
Abajo de comparacion, está comentado un ejemplo con la función de Rosenbrock, y empieza en (0,0). A continuación se muestra una captura de pantalla de la consola al minimizar esta función con comparaciones.
Después, está implementada una solución a un problema de optimización de cámaras de vigilancia.
![Example screenshot](./img/ss.png)


