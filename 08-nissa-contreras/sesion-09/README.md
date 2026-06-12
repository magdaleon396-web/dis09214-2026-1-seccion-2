# sesión 09 - 29/05

# Examén 

1. Perfeccionar la entrega de la solemne 2, o hacer una nueva, que representaba una problematica de genero.  
2. Debe tener 3 estados (PANTALLAS) : INICIO - INSTRUCCIONES - INTERACCIÓN.  
3. Debe tener un RESET o forma de volver a comenzar. (Sin tener que apretar play en la interfaz de p5.js)
4. Hacer un diagrama de flujo de su ALGORITMO - CÓDIGO. (Diseño de sistema)
5. Adaptar su sketch en p5.js para que sea windowResized. canvas (windowWidth, windowHeight)

## El sketch debe incluir como mínimo lo siguiente:

1. 4 variables creadas por ustedes.  
2. 2 variables Integradas en p5.js (ej: width, height, mouseX).  
3. 2 imágenes.  
4. Texto.  
5. 1 función random() y 1 función map().  
6. 3 Sentencias condicionales (if, else if, else)  
7. 1 bucle for (ideal para patrones o repetición de elementos).  
8. 2 funciones propias definidas fuera de draw().  
9. 1 interacciones con el usuario (ej: mouseIsPressed, keyPressed, etc).  
10. 1 Array + 1 Class  
11. Incluir Periféricos: WEB CAM o SONIDOS o TECLADO  
12.Debe tener 3 estados y un RESET.  

## Carpeta de entrega

* En la carpeta de entrega deben dejar 3 links:  
1. Link a un repositorio en Github que presente el Examen de forma
detallada y en lenguaje formal. (REPO EXAMEN)

2. Link al Sketch en p5.js (con permiso de edición)

3. Link al repositorio de la bitácora de clases: (Deben estar todas las
clases desde Historia de la Computación en adelante)

* Dejar el documento con los link en la carpeta de entrega EXAMEN en nuestro Google Drive del curso antes de la clase del viernes 26 de JUNIO.

## Pauta de evaluación
![Pauta de evaluación](https://github.com/user-attachments/assets/08300fa1-c377-4a50-b9e9-46b8ff491a29) 

---

## ¿Qué es un diagrama de flujo? 

**Algoritmo:** Es una secuencia de instrucciones paso a paso, lógicas, definidas, ordenadas y finitas que permiten solucionar un problema o realizar una tarea específica.  

El diagrma de flujo es una representación gráfica de un algoritmo o de los pasos de un proceso. En programación, se utiliza como una herramienta de planificación para visualizar la lógica de un programa antes de escribir una sola línea de código.

**Input (Entrada):**  
La información o los ingredientes que necesitas para empezar.

**Proceso:** Los pasos lógicos que transforman esa entrada.

**Output (Salida):** El resultado final o la solución al problema.

---

## Array (listas) 

* Es como un contenedor con  compartimientos numerados donde puedes guardar múltiples datos bajo un mismo nombre. Es una lista que mantiene varios datos ordenados. Los arreglos (Arrays) son muy útiles para almacenar datos relacionados y pueden contener datos de cualquier tipo.

**Ejemplo**
* Imagina un tren con vagones (un tren de programación, por así decirlo): el tren en sí es el array, pero cada vagón es un elemento, y cada elemento puede contener lo que quieras: números enteros, variables, ¡incluso otros arrays!

**SINTAXIS**
let nombreArray =[e0, e1, e2, e3, e4, e5];  
let Colores = ["red", "orange", "yellow", "green", "blue"];

¿Cómo uso los elementos de este Array?  
* Para llamar a alguno de los valores de mi array vamos a usar: nombreArray [n° elemento]

* Ejemplo:
background (Colores[1]);
* Esto pintara el fondo de mi lienzo de color anaranjado.

* Ejemplo en p5
```
let Colores = ["red", "orange", "yellow", "green", "blue", "purple"];
let index = 0

function setup() {
  createCanvas(400, 400);
  frameRate(1);
}

function draw() {
  //background(Colores[2]);
  
  background(Colores[index]); 
  index = index + 1;
  print(index);
  
  if (index >= Colores.length) {
  index = 0;
 }
}
```

Elementos en p5:  
index: Recorre la lista que esta contenida en el Array de forma seguida, en la velocidad que uno le asigne.  
print: Imprime en la consola los datos que queremos visualizar.
length: Sirve para recetear los elementos del Array, para que funcione como bucle y estos se vayan repitiendo. Equivale al numero total de elementos que tiene mi Array.

---

## Class (molde)

* Una clase (class) es un molde o plantilla abstracta que define la estructura, los datos (propiedades) y los comportamientos (métodos) que tendrá un tipo de objeto específico.

**Ejemplo**  
* Imagínala como el plano de diseño de una casa o un molde para hacer galletas: no es el objeto real en sí, sino las instrucciones empaquetadas para fabricar infinitas copias independientes basadas en ese mismo modelo utilizando la palabra clave new

**SINTAXIS**
*  La sintaxis básica de una clase en JavaScript se estructura siempre en tres partes dentro de un bloque de llaves:  
1. La palabra clave class + nombre que le quiera dar.  
2. El método constructor (donde se definen las propiedades del objeto usando .this)  
3. Las funciones personalizadas que definen lo que hace el objeto.

Se escribe afuera y abajo del función draw(); :  
```
class cuadrado {
  constructor() {
    this.x = 150;
    this.y = 150;
  }

  move() {
    this.x = this.x + random(-5, 5);
    this.y = this.y + random(-5, 5);
  }
  show() {
    stroke(179, 255, 127);
    strokeWeight(4);
    noFill();
    rect(this.x, this.y, 200, 200);
  }
}
```

Y luego se crea en el setup(); :   
```
function setup() {
  createCanvas(500, 500);
  cuadrado1 = new cuadrado();
  cuadrado2 = new cuadrado();
  cuadrado3 = new cuadrado();
```

Y se llama a sus métodos en el draw();    
```
function draw() {
  background(129, 167, 242);

  cuadrado1.move();
  cuadrado1.show();
  cuadrado2.move();
  cuadrado2.show();
  cuadrado3.move();
  cuadrado3.show();
}
```
---

## Ejemlo de sistema de partículas en p5.js

```
let gotas = []; // creo  Array vacío para guardar las partículas

function setup() {
  createCanvas(500, 500);

  // Creamos 200 gotas iniciales al arrancar
  for (let i = 0; i < 200; i++) {
    gotas[i] = new Gota();
  }
}

function draw() {
  background(20, 24, 35); // Fondo nocturno oscuro

  // Recorremos el array para actualizar y mostrar cada gota
  for (let i = 0; i < gotas.length; i++) {
    gotas[i].caer();
    gotas[i].mostrar();
  }
}

// El molde de nuestra partícula de nuestra gota
class Gota {
  constructor() {
    this.x = random(width); // Nace en un punto horizontal al azar
    this.y = random(-500, 0); // Nace arriba, fuera de la pantalla, para un efecto escalonado
    this.velocidad = random(4, 9); // Cada gota tiene una velocidad diferente
    this.largo = random(10, 25); // El tamaño de la línea de la gota
  }

  caer() {
    this.y = this.y + this.velocidad; // Mueve la gota hacia abajo

    // RECOLECTOR/RECICLAJE: Si la gota pasa el fondo de la pantalla...
    if (this.y > height) {
      this.y = random(-50, 0); // Resetea su posición arriba del todo
      this.x = random(width); // Le da una nueva posición horizontal
      this.velocidad = random(4, 9); // Cambia su velocidad para mantener el ritmo azaroso
    }
  }

  mostrar() {
    stroke(138, 180, 248, 150); // Color azul translúcido (el cuarto número es la opacidad)
    strokeWeight(2); // Grosor de la línea

    // Dibuja la gota como una línea vertical corta en movimiento
    line(this.x, this.y, this.x, this.y + this.largo);
  }
}
```
---

## Encargo para el viernes 5 de junio

* Crear un sistema de partículas, con 5 imágenes (mínimo) en .PNG
* Se puede crear diseños o usar fotos recortadas.
* Tema libre.

___ 

# Encargo realizado:

```
let fondo; // Imagen de fondo
let Fotos = []; // Aray que almacenará todas las imágenes disponibles
let FotosParticulas = []; // Array que almacenará las imágenes pequeñas
let foto0, foto1, foto2, foto3, foto4, foto5; // Lista de fotos a utilizar

// Control de escenas
let escena = 0; // 0 = imágenes, 1 = lluvia
let index = 0; // Guarda la imagen del Array que se esta mostrando

function preload() {
  // Se ejecuta antes que setup y carga las imágenes que se van a utilizar

  fondo = loadImage("FONDO.png"); // Fondo del lienzo

  foto0 = loadImage("nissa1.png"); // Imagen cargada
  foto1 = loadImage("nissa2.png"); // Imagen cargada
  foto2 = loadImage("nissa3.png"); // Imagen cargada
  foto3 = loadImage("nissa4.png"); // Imagen cargada
  foto4 = loadImage("nissa5.png"); // Imagen cargada
  foto5 = loadImage("nissa6.png"); // Imagen cargada
}

function setup() {
  // Se ejecuta una sola vez al iniciar

  createCanvas(500, 500); // Crea un lienzo de 500x500 píxeles

  Fotos = [ 
    foto0,
    foto1,
    foto2,
    foto3,
    foto4,
    foto5,
  ]; // Guarda todas las imágenes en un único Array

  crearParticulas(); // Crea las imágenes cuadradas pequeñas
}

function draw() {
  // Se ejecuta constantemente, 60 veces por segundo aprox

  // ESCENA 1: SEIS IMÁGENES
  if (escena == 0) { // Si se presenta la primera escena, se cumple lo siguente

    imageMode(CORNER); // En la primera escena las imágenes se dibujan desde la esquina superior izquierda
    image(Fotos[index], 0, 0, width, height); // Recorre la lista de imágenes que se encuentran en el Array. Dibuja la imagen actual que esta contenida en el index ocupando todo el tamaño del lienzo
  }

  // ESCENA 2: LLUVIA DE IMÁGENES
  else if (escena == 1) { // Si se presenta la segunda escena, se cumple lo siguente

    imageMode(CORNER); // La imagen del fondo se dibuja desde la esquina superior izquierda
    image(fondo, 0, 0, width, height); // Dibuja el fondo rosado

    imageMode(CENTER); // Dibuja las imágenes desde su centro 
    for (let i = 0; i < FotosParticulas.length; i++) { // Recorre todas las imágenes del Array
      FotosParticulas[i].caer(); // Actualiza su posición
      FotosParticulas[i].mostrar(); // Dibuja la imagen
    } 

    // Texto
    fill(255); // Asigna el color blanco al texto
    stroke(245, 181, 201); // Asigna el color rosado al borde del texto
    strokeWeight (8); // Asigna el tamaño del borde en 7 píxeles
    textAlign(CENTER); // Asigna que el texto este alineado
    textSize(15); // Asigna el tamaño de 14 píxeles al texto
    text("Haz clic para reiniciar", width / 2, height - 25); // Escribe la frase "Haz clic para reiniciar" en el centro horizontal del lienzo y a 25 píxeles del borde inferior
  }
}

// CLIC
function mousePressed() { 
  // Galería
  if (escena == 0) { // Si se presenta la primera escena, se cumple lo siguente 
    index++; // Se avanza a la siguente imagen

    if (index >= Fotos.length) { // Si ya se visualizaron todas las imágenes, se cumple lo siguente
      escena = 1; // Cambia a la segunda escena
    }
  }

  // LLUVIA DE IMÁGENES
  else if (escena == 1) { // Si se presenta la segunda escena, se cumple lo siguente
    reiniciar(); // Al hacer clic en la segunda escena, se reinicia el sketch
  }
}

function reiniciar() { // Devuelve todo al estado inicial
  escena = 0; // Vuelve a las seis imágenes principales
  index = 0; // Muestra nuevamente la primera imagen

  crearParticulas(); // Genera pequeñas imágenes nuevamente 
}

function crearParticulas() { // Crea una función llamada crearParticulas
  FotosParticulas = []; // Elimina las anteriores imágenes pequeñas que estaban guardadas

  for (let i = 0; i < 50; i++) { // Crea 50 imágenes pequeñas nuevas
    FotosParticulas.push(new ParticulaImagen()); // Las guarda dentro del Array "FotosPasticulas"
  }
}


// CLASS IMÁGENES PEQUEÑAS
class ParticulaImagen { // Define el comportamiento de cada imagen flotante
  
  constructor() {
    this.x = random(width);
    this.y = random(-height, 0);

    this.velocidad = random(0.3, 1); // Avanzará entre 0.3 y 1 píxel cada vez que se ejecute el draw
    this.tamano = random(40, 80); // Asigna un tamaño aleatorio de cada imagen pequeña de entre 40 y 80 píxeles
    this.offset = random(1000); // Dale un valor aleatorio para el movimiento lateral
    this.miFoto = random(Fotos); // Escoge una imagen aleatoria
  }

  caer() {
    this.y += this.velocidad; // Movimiento hacia abajo

    this.x += sin(frameCount * 0.02 + this.offset) * 0.4; // Movimiento suabe hacia los lados

    if (this.y > height + 100) { // Si la imagen sale por debajo del lienzo, ocurre lo siguente
      this.y = random(-300, -50); // Vuele a aparecer arriba
      this.x = random(width); // Genera una nueva posición en x
      this.velocidad = random(0.3, 1); // Genera una nueva velocidad
      this.tamano = random(40, 80); // Genera un nuevo tamaño aleatorio
      this.miFoto = random(Fotos); // Escoge una nueva imagen aleatoria
    }
  }

  mostrar() {
    image(this.miFoto, this.x, this.y, this.tamano, this.tamano); // Dibuja la imagen de esa partícula en su posiciónal actual (x,y) y con su tamaño actual
  }
}
```
