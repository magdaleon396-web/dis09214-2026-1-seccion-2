# sesión 04 - 23/03

# Clase Datos Dinámicos Variables  

## Posición del mouse  
Variable del sistema numérico que determina la posición del mouse en coordenadas x,y.  
Sintaxis: (MouseX, mouseY);  
Ejemplo: ellipse(mouseX, mouseY, 100, 100);  

## Crear variables propias  
Para crear una variable se puede usar:  
***let*** para variables dinámicas.  
***const*** para variables constantes.  
La variable se declara arriba de todo (antes que la función setup).  

## Javascript Objects  
Para organizar nuesstro codigo de una manera adecuada y ordenada.  
Forma de agrupar **muchas variables** dentro de **una variable**.  

## Función random();  
Devuelve un número aleatorio dentro de un rango que tú definas.  
***random()***: Si no se pone nada, devuelve un número decimal entre **0 y 1**.  
***random(máximo)***: Devuelve un número decimal entre el **0 y el máximo que elijas**.  
***random(mínimo, máximo)***: Devuelve un número decimal entre el **valor mínimo y el valor máximo que elijas**.  

## (width, height);  
Variables integradas en p5, que corresponden a los valores definidos en el createCanvas.  

## (windowWidth, windowHeight);  
Variables integradas en p5, que permiten ajustar el tamaño del lienzo al tamaño de la ventana del navegador, se usa en el createCanvas.  

## Función map();  
Permite convertir un valor de un rango a otro (toma un número que está en una escala y lo traduce proporcionalmente a una escala nueva).  
Sintaxis: map(valor, mínimo original, máximo original, mínimo nuevo, máximo nuevo).

