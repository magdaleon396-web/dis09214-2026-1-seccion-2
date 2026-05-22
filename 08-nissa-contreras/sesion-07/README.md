# sesión 07 - 15/05
---
# Loops: While & For

**Bucle**  
Definición de la rae:
1. Rizo de cabello en forma de helicoidal
**2. Objeto cuya forma recuerda la del bucle**
3. Proceso que se repite indefinidamente
4. Informática. Serie de instrucciones que se repiten indefinidamente mientras no se cumpla una condición previamente establecida.

## LOOP  
Es una estructura de control que permite ejecutar un bloque de instrucciones de madera repetida mientras se cumpla una condición específica o hasta que se alcance un estado determinado.  

### While
Los bucles while son útiles para repetir instrucciones mientras una condición sea verdadera. Son como sentencias if que se repite.  
While (condición booleana){  
si es true ejecuta este códigoen BUCLE}

Ejemplo:  
Mientras (x sea menor o igual que el alto de mi lienzo) {  
x incrementará 1 cada vez}

While(x <= height) {  
x=x+1 }

Ejemplo en p5.js

```  
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(250, 205, 226);

  let y = 0;

  while (y <= 400) {
    stroke(139, 127, 233);
    strokeWeight(5);
    line(0, y, 400, y);
    y = y + 25;
  }

  let x = 0;

  while (x <= 400) {
    stroke(233, 127, 168);
    strokeWeight(5);
    line(x, 0, x, 400);
    x = x + 25;
  }
}
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(250, 205, 226);

  let y = 0;

  while (y <= 400) {
    stroke(139, 127, 233);
    strokeWeight(5);
    line(0, y, 400, y);
    y = y + 25;
  }

  let x = 0;

  while (x <= 400) {
    stroke(233, 127, 168);
    strokeWeight(5);
    line(x, 0, x, 400);
    x = x + 25;
  }
```
---

## for  
4 elementos  

Una forma de repetir un bloque de código cuando se conoce el número de iteraciones. Los bucles `for` son útiles para repetir instrucciones un número determinado de veces.  
Son una especie de SHORTCUT para hacer loops y siempre tienen 4 elementos:

1. Inicialización de una variable  
2. Condición booleana (V-F)  
3. Actualización ( Incrementación o decrementación)  
4. Lo que queremos que pasé cuando la condición sea TRUE

Ejemplo:  
for (inicialización variable; condición booleana; actualización){  
Lo que queremos que pase cuando la condición sea verdadera  
}

for (let x=0; x <= width; x=x+1){  
ellipse (x, 200, random(300))  
}

Ejemplo en p5.js  

```  
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(250, 205, 226);

  /*
  let x=0;

  while(x < width){ 
    fill(233,127,168);
    ellipse(x,200,50);
    x=x+30;
  }
  */

  for (let x = 0; x < width; x = x + 30) {
    fill(random(233), 127, 168);
    ellipse(x, 200, (random(100));
  }
}
```
---
## Desafío de la clase

```
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(250, 205, 226);

  for (let x = 0; x < width; x = x + 30) {
    fill(random(233), 127, 168);
    ellipse(x, 200, random(100));
  }
  
  for (let y = 0; y < height; y = y + 30) {
    fill(random(201), 38, 115);
    ellipse(200, y, random(100));
  }
}
```

---
## NESTED LOOPS  
Un loop dentro de otro loop  
For dentro de otro for  

for (inicialización variable; condición booleana; actualización){  
Lo que queremos que pase cuando la condición sea verdadera

for (inicialización variable; condición booleana; actualización){  
}  
Lo que queremos que pase cuando la condición sea verdadera  
}

Ejemplo:  
```
for (let x=0 ; x <= width; x=x+25) {

for (let y=0 ; y <= height; y=y+25) {
fill (0, 0, 255);
ellipse (x , y, 15);
}
}
```
---

## frameCount

Variable numérica que registra la cantidad de fotogramas dibujados desde que comenzó el boceto. El valor de `frameCount` es 0 dentro de `setup()`. Se incrementa en 1 cada vez que finaliza la ejecución del código en `draw()`.

