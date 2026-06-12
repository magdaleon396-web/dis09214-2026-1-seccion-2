# sesión 10 - 05/06

# Estados y camara web
* Para crear un sketch con estados diferentes hay que seguir los siguentes pasos:

**Paso 1: CREAR Y DEFINIR VARIABLE ESTADOS**  
Al principio de tu código (fuera de las funciones), debes crear una variable que guarde en qué pantalla nos encontramos. Empezará en 0.  
* Ejemplo: let estado = 0; // 0 = Inicio, 1 = Experiencia, 2 = Final

**Paso 2: CONFIGURAR EL LIENZO (function setup)**  
Creamos el lienzo de fondo donde va a ocurrir toda la magia.  
* Ejemplo:
```
function setup() {
  createCanvas(400, 400);
  textAlign(CENTER, CENTER);
}
```

**Paso 3: CREAR LA ESTRUCTURA DEL ESTADO (function draw)**  
Aquí usamos un switch dependiendo del valor de la variable estado, el programa dibujará una cosa u otra.  
* Ejemplo:
```
function draw() {
  background(220);

  switch (estado) {
    case 0:
      pantallaInicio();
      break;
    case 1:
      pantallaExperiencia();
      break;
    case 2:
      pantallaFinal();
      break;
  }
}
```

**Paso 4: PROGRAMAR VISUALMENTE CADA ESTADO (funciones propias)**  
Ahora creamos las funciones que inventamos en el paso anterior. Cada una tendrá un diseño y un color diferente para que se note el cambio.  

**Paso 5: PROGRAMAR VISUALMENTE CADA ESTADO (funciones propias)**

```
function pantallaInicio() {
  background(135, 206, 250);
  fill(0);
  textSize(24);
  text("ESTADO 0: INICIO", width / 2, height / 2 - 20);
  textSize(16);
  text("Haz clic para continuar", width / 2, height / 2 + 20);
}

function pantallaExperiencia() {
  background(144, 238, 144);
  fill(0);
  textSize(20);
  text("ESTADO 1: EXPERIENCIA", width / 2, height / 2 - 20);
  
  // Interactividad extra en este estado
  fill(255, 100, 100);
  ellipse(mouseX, mouseY, 30, 30);
  
  fill(0);
  textSize(14);
  text("Mueve el mouse. Haz clic para avanzar.", width / 2, height / 2 + 40);
}

function pantallaFinal() {
  background(255, 182, 193);
  fill(0);
  textSize(24);
  text("ESTADO 2: FINAL", width / 2, height / 2 - 20);
  textSize(16);
  text("Haz clic para volver al inicio 🔄", width / 2, height / 2 + 20);
}
```

**Paso 5: LA LÓGICA DEL CAMBIO Y EL REINICIO**  
Para pasar de un estado a otro y lograr que vuelva al comienzo, usamos la función mousePressed() Cada vez que hagas un clic, la variable aumentará. Si llega a 3 (después del estado 2), volverá a 0.  
* Ejemplo:
```
function mousePressed() {
  estado = estado + 1;
  
  if (estado > 2) {
    estado = 0;
  }
}
```
---

## Importante

Hay muchas formas diferentes de cambiar de un estado a otro.

**1. Interacción con el Teclado** 

* Por barra espaciadora o Enter  
* Por teclas específicas (ej. Números): Puedes hacer que la tecla 1 te lleve al inicio, la 2 a la experiencia y la 3 al final.  

**2. Botones Reales en la Pantalla**

* En lugar de hacer clic en cualquier parte de la pantalla, puedes crear un botón real de HTML usando la librería de p5.js. Esto es mucho más profesional para menús.

**3. Zonas de Clic (Botones dibujados con rect o ellipse)**

* Si no quieres usar botones de HTML y prefieres dibujar tus propios botones con rect(), puedes evaluar si el mouse estaba dentro de esa caja al hacer clic.

**4. Interacciones Automáticas (Por Tiempo)**

* Por Tiempo (Temporizador): Ideal para una pantalla de introducción (Splash Screen) que dura 3 segundos y pasa sola al menú.

---

## Cámara Web

**createCapture(VIDEO);**  

1. Crear la variable para la captura, declarar una variable global que guardará el flujo de video de tu cámara web.

2. Inicializar la cámara en el function setup() utilizamos el comando especial createCapture(VIDEO) esto le pedirá permiso al navegador para encender la cámara del computador. También definimos tamaño con captura.size(x,y); y es muy importante agregar captura.hide(); para que esconda el video que HTML pone abajo por default.

3. Dibujar la cámara en el function draw() usamos la función image(). p5.js toma cada cuadro (frame) de la cámara y lo dibuja en el lienzo en tiempo real.

```
let captura;

function setup() {
  createCanvas(640, 480);
  
  // Capturamos la cámara del computador
  captura = createCapture(VIDEO); 
  captura.size(500, 480); //define tamaño de la captura de video
  captura.hide(); // Esconde el duplicado de HTML
  textAlign(CENTER);
}

function draw() {
  background(0);
  
  // Dibujamos la captura en la posición (0,0)
  image(captura, 0, 0, width, height);
}
```
---

## EJEMPLOS CÁMARA INTERACTIVA

Cámara web que reacciona al micrófono
* [P5.js](https://editor.p5js.org/Nissacontreras/sketches/MBRcU-3oN)


Cámara web con puntos
* [P5.js](https://editor.p5js.org/Nissacontreras/sketches/jKHMJdh6I)


Cámara web con filto
* [P5.js](https://editor.p5js.org/Nissacontreras/bocetos/OxS-WRfOb)


Encender y apagar camara web
* [P5.js](https://editor.p5js.org/Nissacontreras/sketches/C0lKCI365)
