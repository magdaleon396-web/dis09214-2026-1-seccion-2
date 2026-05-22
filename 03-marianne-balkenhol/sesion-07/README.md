# CLASE 7



15/5/2026


# Loops, while y for

---

# ¿Qué es un bucle?

## Definición según la RAE

1. Rizo de cabello en forma helicoidal.  
2. Objeto cuya forma recuerda la del bucle.  
3. Proceso que se repite indefinidamente.  
4. En informática: serie de instrucciones que se repiten indefinidamente mientras no se cumpla una condición previamente establecida.

---

# LOOP

Un loop es una estructura de control que permite ejecutar un bloque de instrucciones de manera repetida mientras se cumpla una condición específica o hasta llegar a un estado determinado.

Los loops permiten automatizar procesos repetitivos dentro de un programa.

---

# WHILE

El loop while es útil para repetir instrucciones mientras una condición sea verdadera.

## Estructura

While (condición booleana) {

ejecuta este código si es true

}

---

## Funcionamiento

- Primero se evalúa la condición.
- Si la condición es ***true***, el código se ejecuta.
- Luego vuelve a comprobar la condición.
- El proceso continúa en bucle hasta que la condición sea ***false***.

---

# FOR

El loop for sirve para repetir instrucciones una cantidad determinada de veces.

Es una especie de shortcut para crear loops y siempre tiene 4 elementos principales:

1. Inicialización de una variable.  
2. Condición booleana (verdadero o falso).  
3. Actualización de la variable (incremento o decremento).  
4. Acción que se ejecutará mientras la condición sea verdadera.

---

## Estructura

for (inicialización variable; condición booleana; actualización){

Lo que queremos que pase cuando la condición sea verdadera

}

---

# NESTED LOOPS

Los nested loops son loops dentro de otros loops.

Por ejemplo: un for dentro de otro for.

Esto permite generar repeticiones más complejas, como patrones, cuadrículas o múltiples combinaciones de elementos.

---

## Estructura

for (inicialización variable; condición booleana; actualización){

Lo que queremos que pase cuando la condición sea verdadera

for (inicialización variable; condición booleana; actualización){

Lo que queremos que pase cuando la condición sea verdadera

}

}

---

# frameCount

frameCount es una variable numérica que registra la cantidad de fotogramas dibujados desde que comenzó el boceto.

## Funcionamiento

- Dentro de setup(), el valor inicial de frameCount es 0.
- El valor aumenta en 1 cada vez que termina la ejecución del código dentro de draw().

frameCount sirve para:

- Crear animaciones.
- Generar movimiento.
- Controlar tiempos.
- Hacer cambios automáticos dentro del sketch


















