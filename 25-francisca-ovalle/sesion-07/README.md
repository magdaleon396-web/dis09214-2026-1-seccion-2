# sesión 07 - 15/05 Apuntes  
---  
# LOOPS WHILE & FOR:  
## ¿Qué es un loop? (bucle)  
Los loops son repeticiones infinitas.  
***Definición de blucle:***   
1. Rizo de cabello en forma helicoidal
2. Porceso que se repite indefinidamente
3. Informatica: Serie de instruccciones que se repiten indefinidamente mientras no se cumpla una condición previamente establecida.

***LOOP:*** Estructura de control que permite ejecutar un bloque de instrucciones de manera repetida mientra se cumpla una condición específica o hasta que se alcance un estado determinado.    

***WHILE:*** Los bucles while son útiles para repetir isntrucciones mientras una condición sea verdadera. Son como sentencia **if** que se repite.  
While(condición booleana){si es true se ejecuta el código en BUCLE}  

*Ejemplo:   While(x <= height){x=x+1}*   

*Ejemplo: Mientras ( x sea menor o igual que el alto de mi lienzo){ x se incrementará 1 cada vez}*  

***FOR***: Una forma de repetir un bloque de código cuando se conoce el número de iteraciones. Los bucles *`for`* son útiles para repetir instrucciones un
número determinado de veces. Son una especie de *SHORTCUT* para hacer loops y siempre tienen 4 elementos:  
1. Inicialización de una variable
2. Condición booleana: V-F
3. Actualización: Incrementación o decrementación
4. Lo que queremos que pasé cuando la condición sea TRUE

*Ejemplo:* *for (inicialización variable; condición booleana; actualización){Lo que queremos que pase cuando la condición sea verdadera}*  

*Ejemplo: for (let x=0 ; x <= width; x=x+1) {ellipse (x , 200, random(300))}*  
### NESTED LOOPS:
Un loop dentro de otro loop  
***Un for dentro de otro for***   

*Ejemplo: for (inicialización variable; condición booleana; actualización){
**Lo que queremos que pase cuando la condición sea verdadera**
for (inicialización variable; condición booleana; actualización){
}
**Lo que queremos que pase cuando la condición sea verdadera**
}*  

*Ejemplo: for (let x=0 ; x <= width; x=x+25) {
for (let y=0 ; y <= height; y=y+25) {
fill (0, 0, 255);  
ellipse (x , y, 15);
}
}*  
***frameCount:*** Variable numérica que registra la cantidad de fotogramas dibujados desde que comenzó el boceto. El valor de *`frameCount`* es 0 dentro de *`setup()`*. Se incrementa en 1
cada vez que finaliza la ejecución delcódigo en *`draw()`*.
