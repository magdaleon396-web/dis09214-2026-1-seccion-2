# sesión 07 - 15/05

LOOPS, WHILE & FOR 
--
LOOP:
--
Es una estructura de control que permite ejecutar
un bloque de instrucciones de manera repetida
mientras se cumpla una condición específica o
hasta que se alcance un estado determinado.

WHILE (3 elementos)
--
Los bucles while son útiles para repetir
instrucciones mientras una condición sea
verdadera. Son como sentencias if que se repite.

while (condición booleana) {
si es true ejecuta este código en BUCLE}

```
//Ejemplo:
While (x <= height) {
x=x+1 }
```

Ejemplo:
Mientras (x sea menor o igual
que el alto de mi lienzo) {
x incrementará 1 cada vez }

como agregar codidos(agregar 3 comilla que vas hacia el otro lado) al inicio y final del codigo que voy a copiar)
--

```
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);

  let x=0;

  while(x < width){ //while significa mientras. mientras X sea menor que el width de el canvas 
    fill(233,127,168); // relleno del circulo 
    ellipse(x,200,50);  // se crea un circulo en en x, 200 de tamaño 50
    x=x+30; // pero luego el valor de X amuneta a en 30 cada vez que el loop se repita.
    tecnicamente el loop de while termina cuando x sea igual o mayor que width 
  }

}
``` 

```
function setup() {
  createCanvas(400, 400);
  noFill();
  strokeWeight(2);
}

function draw() {
  // fondo negro
  background(0); 
  
  // creo variable diametro y le asigno un valor de 400
  let diametro = 400; 

  //loop Mientras el valor de mi varibale diametro sea mayor que 0

    
  while (diametro > 0) {
  // asigna un color al borde alterado por mi varbiale diametro
    stroke(diametro, 100, 255 - diametro / 2);
    
  // crea un circulo en cordenada x, cordenada y, diametro  
    circle(width / 2, height / 2, diametro);
    
  //creamos la variable opArt que será un map de mouseX
    let opArt = map(mouseX, 0, width, 5, 50); 
    diametro = diametro - opArt; 
  }
}
```

for (4 elementos)
--
for (inicialización variable; condición booleana; actualización){
Lo que queremos que pase cuando la condición sea verdadera
}

```
for (let x=0 ; x <= width; x=x+1) {
ellipse (x , 200, random(300))
}
```

Una forma de repetir un bloque de código cuando se conoce el número
de iteraciones. Los bucles `for` son útiles para repetir instrucciones un
número determinado de veces.
Son una especie de SHORTCUT para hacer loops y siempre tienen 4
elementos:

1. Inicialización de una variable
2. Condición booleana (V-F)
3. Actualización ( Incrementación o decrementación)
4. Lo que queremos que pasé cuando la condición sea TRUE

```
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(127, 221, 233);

  /*
  let x=0;
  
  while(x < width){ 
    fill(233,127,168);
    ellipse(x,200,50);
    x=x+30;
  }
  */

//declaro condición 
  for (let x = 0; x < width; x = x + 30) {
    fill(233, 127, 168);
    ellipse(x, 200, 50);
  // for: cuando x sea igual a 0; x sea menor que width; x sea igual a x más 30. se rellenan circulos en x, 200, 50
  }
}
```

   ejercicio mini en clase
   -- 
   hacer los circulos horizontlates en vertical 
   <img width="552" height="546" alt="image" src="https://github.com/user-attachments/assets/da4a6f12-32de-416e-8ee7-8675e01d22c3" />

 ```
   function setup() {
  createCanvas(400, 400);
  frameRate(10)
}

function draw() {
  background(220);

for (let y = 0; y < width; y = y + 30) {
    fill(random(255), random(255), random(255));
    ellipse(200, y, random(100));
  }

}
```


NESTED LOOPS
--
Un loop dentro de otro loop (tecnicamente un for dentro de un for) utilizado para crear dos condiciones for en un solo loops simultaneamente 

for (inicialización variable; condición booleana; actualización){
Lo que queremos que pase cuando la condición sea verdadera
for (inicialización variable; condición booleana; actualización){
}
Lo que queremos que pase cuando la condición sea verdadera
}

```
for (let x=0 ; x <= width; x=x+25) {

for (let y=0 ; y <= height; y=y+25) {
fill (0, 0, 255);
ellipse (x , y, 15);
}
}
```

Ejemplo de Nested Loop:
--
<img width="522" height="522" alt="image" src="https://github.com/user-attachments/assets/7273f5fb-7f41-4df3-9e86-6841d6a6d13f" />

```
function setup() {
  createCanvas(400, 400);
  frameRate(24);
}

function draw() {
  background(0);

  for (let x = 0; x < width; x = x + 25) {
    for (let y = 0; y < height; y = y + 25) {
      fill(0, 0, 255);
      ellipse(x, y, 15);
    }
  }
}

// Agregar valores Random en color y ellipse para movimiento 
// Agregar mouseX y mouseY
```
Segundo ejemplo:
```
function setup() {
  createCanvas(400, 400);
  frameRate(24);
  colorMode(HSB); // Hue - Saturación - Brillo (mas facil de trabajar)
  frameRate(9);
}

function draw() {
  background(0);

  let cambioHue = map(mouseX, 0, 400, 0, 360);
  let cambioSat = map(mouseY, 0, 400, 0, 360);

  background(cambioHue, cambioSat, 100);

  if (mouseIsPressed) {
    background(0, 0, 100);
  }

  for (let x = 0; x < width; x = x + 25) {
    for (let y = 0; y < height; y = y + 25) {
      fill(random(360), 80, 100);
      ellipse(x, y, random(20));
    }
  }
}

function mouseReleased() {
  fill(255, 0, 0);
  ellipse(mouseX, mouseY, random(400));
}

// Agregar mouseX y mouseY
```

frameCount
--
Variable numérica que registra la
cantidad de fotogramas dibujados
desde que comenzó el boceto. El
valor de `frameCount` es 0 dentro
de `setup()`. Se incrementa en 1
cada vez que finaliza la ejecución del
código en `draw()`.

Ejemplo:

<img width="536" height="533" alt="image" src="https://github.com/user-attachments/assets/465277f7-feed-477c-89c1-6acfe1f74eef" />
<img width="541" height="545" alt="image" src="https://github.com/user-attachments/assets/16d86e13-77ba-4416-b3d4-bc6086e7c33f" />

``` 
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(0);

  print(frameCount);
  
  if ((frameCount <= 180)) {
    background(130, 237, 75);
    textSize(50);
    textAlign(CENTER, CENTER);
    text("HOLA"+"\n ¿Cómo estay?", 200, 200);
  }
  else {
    background(237,75,211); 
    textSize(100);
    textAlign(CENTER, CENTER);
    text("CHAO", 200, 200);
  }
  
  if(mouseIsPressed){
    frameCount = 0;
  }
}
```


