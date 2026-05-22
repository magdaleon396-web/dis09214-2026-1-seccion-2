# sesión 07 - 15/05  
**LOOPS : WHILE Y FORD**  


***¿Qué es un Loop?***  
DEF. RAE: (Bucle) Proceso que se repite indefinidamente, serie de instrucciones que se repiten indefinididamente mientras no se cumpla una condición previamente establecida.   
Es una estructura de control que permite ejecutar un bloque de instrucciones de manera repetida o mientras se cumpla una condición especifíca o hasta que se alcance un estado determinado.   

**WHILE:**  
Acción de repetición, no es el movimiento o cambio en si, eso se le agrega  aparte. 
Los bucles son útiles para repetir instrucciones mientras una condición sea verdadera. Son como sentencias if que se repite.   
 
 - while(condición booleana){si es true ejecuta este código en bucle}   

Ejemplo: mientras (x sea menor o igual que el alto de mi lienzo)
{x incrementará 1 cada vez}     

**FOR:   (más fácil, más común de usar)**  
Una forma de repetir un bloque de código cuando se conoce el número
de iteraciones. Los bucles `for` son útiles para repetir instrucciones un
número determinado de veces.
Son una especie de SHORTCUT para hacer loops y siempre tienen 4
elementos:

1. Inicialización de una variable
2. Condición booleana (V-F)
3. Actualización ( Incrementación o decrementación)
4. Lo que queremos que pasé cuando la condición sea TRUE

  - for (inicialización variable; condición booleana; actualización){Lo que queremos que pase cuando la condición sea verdadera}


**NESTED LOOP:**  
Un for dentro de un for.  

- for (inicialización variable; condición booleana; actualización){Lo que queremos que pase cuando la condición sea verdadera
for (inicialización variable; condición booleana; actualización){
}Lo que queremos que pase cuando la condición sea verdadera}

**frameCount:**  
Variable numérica que registra la cantidad de fotogramas dibujadosdesde que comenzó el boceto. El valor de `frameCount` es 0 dentro
de `setup()`. Se incrementa en 1 cada vez que finaliza la ejecución del código en `draw()`.
