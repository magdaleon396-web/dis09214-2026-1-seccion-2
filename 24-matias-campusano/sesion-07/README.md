# sesión 07 - 15/05  

## Loops while & for  

*proceso que se repite indefinidamente  
*Informatica. Serie de instrucciones que se repiten indefinidamente mientras no se cumpla una condición previamente establecida.  

**Loop**  
Es una estructura de control que permite ejecutar un bloque de instrucciones de manera repetida mientras se cumpla una condición específica o hasta que se alcance un estado determinado.

### While (condición booleana){ejecuta este código si es true}

Ejemplo:  
Minetras(x sea menor o igual que el alto de mi lienzo){x incrementará 1 cada vez}  
While(x<=height){x=x+1}  

### For  
Una forma de repetir un bloque de código cuando se conoce el número de iteraciones. Los bucles "for" son útiles para repetir instrucciones 

**For**(inicialización varialbe;condición booleana;actualización){lo que queremos que pase cuando la condición sea verdadera}  
    For(let x=0; x<=width; x=x+1){ellipse(x,200,random(300))}

### FOR dentro de otro FOR  o NESTED LOOPS

for(inicio variable;condición booleana;actualización){lo que queremos que pase cuando la condición booleana
}

### frameCount  
Variable numérica que registra la cantidad de fotogramas dibujados desde que comenzó el boceto. El valor de 'frameCount' es 0 dentro de setup()'. Se incrementa en 1 cada vez que finaliza la ejecución del código en 'draw()'.

Ejemplos en p5: https://editor.p5js.org/campossantom/sketches/w3yvHUH_C
