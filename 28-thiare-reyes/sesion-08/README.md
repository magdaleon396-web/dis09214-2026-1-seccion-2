# Solemne 2
## Basta a la violencia de género
Thiare Reyes

Este proyecto es un llamado a **frenar** o **parar** la violencia de género, en el se puede observar una imagen de una mujer asustada por un brazo con el puño cerrado, haciendo alución que es victima de violencia, acompañado de elementos visuales como este patron de lineas verticales que hacen referencia a una reja como si no tubiera salida, tambien se encuentra un rectángulo y circulo el cual van en esa posicion para llamar la atención del usuario y desvien la mirada al puño.
Luego que el usuario interactua, este escenario cambia abruptamente, ahora hay una imagen de una mujer con el brazo extendido hacia adelante, hcaciendo una señal de alto con la mano, sobre esa imagen hay un texto que dice **BASTA** y si el usuario sigue interacuando, moviendo el mouse a la derecha esta palabra se va haciedo cada vez más grande hasta llegar al final del lienzso, esto haciendo referencia que las mujeres tenemo que gritar para que nos escuchen y en la parte atras de la imagen se ve un triangulo rojo que parpadea, representando una alerta. Con este proyecto busco reflejar a de todas la mujeres que pudieron salir de esa brutal situación y tranmitir este potente mensaje.

<img width="619" height="736" alt="Captura de pantalla 2026-05-22 050053" src="https://github.com/user-attachments/assets/51db5f54-ed34-4d34-96dc-a9601a68768f" />

<img width="617" height="737" alt="Captura de pantalla 2026-05-22 050201" src="https://github.com/user-attachments/assets/0cefc901-4c1e-4e05-8192-9efa4c74388c" />

* Inspiración o referencia
  * Si bien no tengo una referencia concreta, recorde y me inspiré en los comerciales o propaganda del gobierno de *no más a la violencia* en la que salía una escena de una mujer siendo violentada y la secuencia del video salia ella con muchas mujeres llamando a frenar y denunciar estos hechos. 

<img width="1408" height="632" alt="Diagrama de flujo" src="https://github.com/user-attachments/assets/4304db17-26fe-40c3-8394-ba479a7971e7" />

* Código P5.js
```let escena = 1; // Variable que controla que imagen se muestra
let rotacionFondo = 0; // Variable para crear un bucle y la rotación del fondo
let tamanoTexto = 32; // Variable para animar el texto con map()
let colorAlerta; // Variable para guardar un color aleatorio
let mujerAmenazada; // Variable de imagen mujer con un puño
let mujerBasta;  // Variable de imagen mujer extendiendo el brazo y mostrando la palma de la mano
let i =0;

function preload(){ // Sirve para cargar imagenes antes de empezar el programa
   mujerAmenazada= loadImage('mujeramenazada.png'); // imagen escena 1
   mujerBasta = loadImage('mujerbasta.png'); // imagen escena 2
}

function setup() { // Configura el entorno inicial
  createCanvas(500, 600); // Lienzo de 500 x 600
  colorAlerta = color(200, 0, 0);
}

function draw() { // Permite crear movimiento y interacción en tiepmo real
  background(0); // Color del lienzo (negro)

  // Sentencias condicionales (if, else if, else)
  if (escena === 1) {
    dibujarEscenaUno(); // si el valor de escena es igual a 1, da como resultado dibujarEscenaUno, el cual es el fondo de lineas
  } else if (escena === 2) {
    dibujarEscenaDos(); // si el valor no es 1, y es 2 este ejecuta dibujarEscenaDos, donde sale la palabra basta
  } else {
    // Escena por defecto o de seguridad
    background(125, 27, 27);
  }
  
function dibujarEscenaUno() { // Fondo dinámico usando un Bucle FOR

  stroke(200);
  for (let i = 0; i < width; i += 30) {
    line(i, 0, i, height); // Patron de lineas verticales fijas a lo largo del de todo el ancho del lienzo 
  }
  
  image(mujerAmenazada, 50, 100, 400, 400);  // Aquí se muestra la primera imagen
  
  
  fill(180); // relleno del rectángulo
  rect(50, 20, 100, 150); // rectángulo en la posición (50, 20, 100, 150)
  
  noStroke(); // sin borde
  fill(46, 22, 161); // color de relleno del elipse
  ellipse(width / 4, height / 4, 120, 120); // posición del elipse
}

function dibujarEscenaDos() { 
 
  if (frameCount % 10 === 0) { 
    colorAlerta = color(random(200, 255), random(0, 50), random(0, 50));
  }
  
  push();
  translate(width / 2, height / 2);
  rotate(rotacionFondo);
  scale(1.2);
  
  // Triángulo de advertencia en el fondo
  fill(colorAlerta); // relleno de color usando la variable colorAlerta
  triangle(0, -250, -250, 120, 150, 120); // posición del triángulo
  pop();
  
  // Incrementa la rotación para el fondo de la escena 2
  rotacionFondo += 0.01;
  
  
  image(mujerBasta,50, 150, 400, 400); // Aquí se muestra la segunda imagen
  
  
  tamanoTexto = map(mouseX, 0, width, 40, 70); // El tamaño del texto cambiara suavemente según la posición X del mouse
  
  //Texto "BASTA"
  fill(255); // color de la letra (blanco)
  textAlign(CENTER, CENTER); // alinear el texto en el centro del lienzo
  textSize(tamanoTexto); // tamaño de la letra, usando la variable tamanoTexto
  textStyle(BOLD); // estilo de la letra, en este caso es bold
  text("BASTA", width / 2, height / 2 + 50); // palabra o frase elegida y su posición
 }
}
//Interacción con el usuario
function mousePressed() { // Al hacer click, si está en la escena 1 pasa a la 2, y viceversa
  if (escena === 1) {
    escena = 2;
  } else {
    escena = 1;
  }
}
```

* Link Sketch P5.js
[P5.js](https://editor.p5js.org/ThiareReyes/sketches/-gpL8WYoS)
