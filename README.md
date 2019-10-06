# Proyecto statistical learning2

## Env
Todos los problemas se trabajaron con pytorch como herramienta y en el ambiente proporcionado por google collab (bastante frustrante) 

## Metodología
* En cada problema se inicio con una hipotesis acerca de la variable a predice, clases a clasificar o salida deseada a obtener. 
* Se inicio con exploración y manipulación de data, para encontrar correlaciones y tendencias.
* Se inicio el entranmiento con hyperparametros por defeccto para ver como funcionaba y luego modificarlos de acuerdo a su comportamiento.
* Se realizaron pruebas exhaustivas modificando parametros, preparando data, buscando diferentes approachs para lograr mejores convergencias.

## Problema 1

El dataset era un archivo con 998000 registros de sesiones de medición de motores electricos. El objetivo general o lo deseado era lograr encontrar un modelo que permitiera predicir la temperatura del pm (Permanent Magnet) ya que es muy costoso medirlo con instrumentos propios.

El modelo fue entrenado, se probo varios opciones. El primero con stocastic gradient descent, luego con algun optimizador mas moderno como adam.

Los mejores resultados fueron con adam, sin embargo no se logro entontrar un modelo lo suficiente bueno.

Al final se logro interpretar que el modelo funciona mejor por sesiones. Se logro asi un modelo con un R^2 del 70%. Esto da un indicio que por ahi puede ser la ruta a la solución. Por motivos de tiempos y recursos de computo no se hizo la prueba, pero se podrian entrenar mas modelos con diferentes sesiones y luego comparar resultados, ya sea por una media aritmetica o usando el modelo que se adapta mas general a las demas seciones.

https://github.com/kenny08gt/proyecto_statistical_learning2/blob/master/ProyectoSL2_P1.ipynb

## Problema 2

Se utilizo un dataset de cifar10, que trae 60000 imagenes con 10 clases. El objetivo es lograr clasificar correctamente las imagenes dentro de las clases existentes, a traves de una red convolucional.

Se logro entrenar hasta tener un 70% de precisión.

https://github.com/kenny08gt/proyecto_statistical_learning2/blob/master/proyectoSl2_P2.ipynb

## Problema 3

Se utilizo un dataset que contiene mas de 550000 letras de canciones. A travez de una red convolucional con LSTM.
El objetivo fue entrenar la red con canciones escritas por metallica para poder generar nuevas letras. Sin embargo el numero de canciones escritas por metallica en el dataset parecia ser muy pequeno, entonces si intento usar dos artistas como metallica y megadeth, que tienen una historia parecida y son contemporaneos. Se logro entrenar y la red, sin embargo, pareciera que la perdida en promedio sigue siendo demasiada alto.

Se logro generar salidas, pero sigue pareciendo que le falta entrenamiento. Me quedo con la duda sin con mas recursos computacionales es podria haber generado algo mejor.

https://github.com/kenny08gt/proyecto_statistical_learning2/blob/master/ProyectoSL2_P3.ipynb

## Conclusiones
* Cada problema presento sus retos diferentes, sin embargo algo comun fue que los datasets no estaban preparados, o si servirian para el objetivo de cada uno, sin saber si iban a converger. 
* El poder de computo es un gran handicap. Google collab ofrece gpu pero con memoria limitada, por itempo limitado y a veces deja de responder.
* El futuro de estas herramientas es maravilloso y no me queda mas que emoción para esperarlo.
