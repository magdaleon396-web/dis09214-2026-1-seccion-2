# sesión 07 - 15/05

# ***LOOPS WHILE & FOR*** 

- **Bucle**: Rizo de cabello, proceso que se repite indefinidamente
  * Informatica: Serie de instrucciones que se repiten indefinidamente mientras no se cumpla una condición previamente establecida

- **Loop**: Estructura de control que permite ejecutar un bloque de instrucciones de manera repetida mientras se cumpla una condición específica o hasta que se alcance un estado determinado.

------------------------------------

# WHILE (3 elementos)

- Los blucles while son útiles para repetir instrucciones mientras una condición sea verdadera. Son como sentencias if que se repite. Antes del while va el let x=0

**Sintaxis** ----> while (condición booleana){si es true ejecuta este co´digo en BUCLE}

#### EJEMPLO:  Mientras (x es menor o igual que el alto de mi lienzo){x incrementára 1 cada vez}

- ¨¨javascript¨¨----> eso es para que el codigo este ordenado 

-------------------------------

# FOR (4 elementos) 

- Es una forma de repetir un bloque de código cuando se conoce el numero de iteraciones. Los bucles ´for´ son utiles para repetir instrucciones un número determinado de veces. Son una especie de SHORTCUT para hacer loops y **SIEMPRE** tienen 4 elementos.
- Mejor que nos quede en la cabeza EL FOR que el while!

  1) Inicialización de un variable
  2) Condición booleana (V-F)
  3) Actualización (incrementación - decrementación)
  4) Lo que queremos que pasé cuando la condición sea TRUE
 
  **Sintaxis** ----> for(inicialización variable; condición booleana; actualización){Lo que queremos que pase cuando la condición sea verdadera}

  #### EJEMPLO:
                 for (let x=0 ; x <= width; x=x+1) {
                 ellipse (x , 200, random(300))
                 }

---------------------------

# NESTED LOOP (loop dentro de otro loop) ( for dentro de otro for )

- Primero empieza el loop hijo y despues el loop MADRE
- Podemos rellenar todo el programa

**Sintaxis** ---> 
for (inicialización variable; condición booleana; actualización){
Lo que queremos que pase cuando la condición sea verdadera
for (inicialización variable; condición booleana; actualización){
}
Lo que queremos que pase cuando la condición sea verdadera
}

---------------------------------
# FRAME COUNT ( viene integrada en p5js)

- Variable numérica que registra la cantidad de fotogramas dibujados desde que comenzó el boceto. El
valor de **frameCount** es 0 dentro de **setup()**. Se **incrementa** en 1 cada vez que finaliza la ejecución del código en **draw()**.
- Para la solemne 2 , esta permitido ocupar IA, Si ocupamos algo nuevo gracias a la IA , hay que explicar coomo funciona y como lo ocupabamos,TENEMOS QUE PRESENTAR
- Primero hacer EL DIAGRAMA DE FLUJO para visualizar nuestra idea, pensar en la problemática primero.
- Ojo con las fíguras y elementos, algo que visualmente se vea bien , podemos ocupar diseños que tengamos en ilustrator o photoshop  pegarlo como PNG.
