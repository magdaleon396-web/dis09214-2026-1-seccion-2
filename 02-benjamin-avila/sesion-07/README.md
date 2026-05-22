# sesión 07 - 15/05
-----
**LOOPS WHILE & FOR**
*¿Qué es un loop?*
(Bucle), son infinitos

Definición de bucle:

-Informatica. Serie de instrucciones que se repiten indefinidamente mientras no se cumpla una condicion previamente establecida

   ***LOOP*** :
Es una estructuea de control que permite ejecutar un bloque de instrucciones de manera repetida mientras se cumpa una condicion especifica o hasta que de alcance un estado determinado.

***While*** :
3 elemento

Los bucles while som utiles para repetir instrucciones mientras una condicion sea verdadera. Son como sentencias if que se repite
//while(condicion boleana){si es true ejecuta este codigo en BUCLE}

*EJEMPLO:* //mientras (x sea menor o igual que el alto de mi lienzo){x incrementará 1 cada vez mas}

//while(x<=height) {x = x + 1}

***For:***
4 elementos

Una forma de repetir un bloque de código cuando se conoce el número de iteraciones. Los bucles `for` son útiles para repetir instrucciones un número determinado de veces. Son una especie de SHORTCUT para hacer loops y siempre tienen 4 elementos:

1. Inicialización de una variable
2. Condición booleana (V-F)
3. Actualización ( Incrementación o decrementación)
4. Lo que queremos que pasé cuando la condición sea TRUE

//for (inicialización variable; condición booleana; actualización){Lo que queremos que pase cuando la condición sea verdadera}

*EJEMPLO:* //for (inicialización variable; condición booleana; actualización){Lo que queremos que pase cuando la condición sea verdadera}

//for (let x=0 ; x <= width; x=x+1) {ellipse (x , 200, random(300))}

*QUEDARNOS SIEMPRE CON EL FOR MAS QUE CON EL WHILE*

****NESTED LOOPS****

Un loop dentro de otro loop

*Un for dentro de otro for*

****frameCount****

Variable numérica que registra la cantidad de fotogramas dibujados desde que comenzó el boceto. El valor de `frameCount` es 0 dentro de `setup()`. Se incrementa en 1 cada vez que finaliza la ejecución del código en `draw()`.




