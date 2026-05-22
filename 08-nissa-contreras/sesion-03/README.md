# sesión 03 - 27/03

# Algoritmo 

**Diagrama de flujo**  
* Representación gráfica de un algoritmo o de los pasos de un proceso. En programación, se utiliza como una herramienta de planificación para visualizar lalógica de un programa antes de escribir una sola línea de código.  
* Se usan componentes estandar (Simbología).

___

## Lenguajes de programación

* ¿Cuantos lenguajes de programacion existen?  
Existen entre 700 y 900 lenguajes de programación que se utilizan actualmente en la industria.  

___

## Libreria de Javascript

* p5.js no es un lenguaje nuevo, sino una biblioteca de javascript.

___

## Setup () {

* Setup se ejecuta una sola vez al principio (para crear el lienzo).  
* Su proposito es configurar el entorno inicial.  
* Defines el tamaño del lienzo, cargas imagenes o sonidos, y estableces configuraciones que no cambiarán.

___

## createCanvas  

* Sintaxis: createCanvas ([width], [height], [render], [canvas]);
* Nos sirve para crear el lienzo (canvas) y determinar su tamaño en pixeles, solo se pone una vez y siempre dentro del setup();

___

## Background  

* Sintaxis background(v1, v2, v3, [a]);  
* Ejemplo background(250, 150, 228,150);
* Nos sirve para designar el color del lienzo. Se puede poner en el setup(); o en el draw(), pero tienes resultados diferentes.

___

## strokeWeight();

Establece el tamaño del borde de las figuras o el ancho de la linea o punto. Siempre se pone arriba de Stroke();

## noStroke();

Se usa para que mi figura no tenga borde.


## Stroke ();  

Establece el color que se utiliza para dibujar puntos, lineas y contornos de figuras. Se pone arriba de la linea de código de la figura.


## strokeCap();

Define la forma de la linea o borde de las figuras.  
Las constantes son: ROUND, SQUARE, PROJECT  
Por defecto siempre es ROUND

---

## fill();

Establece el COLOR de relleno para las figuras. Se pone arriba de la figura que quiero colorear.

---

## arc();

Nos sirve para hacer arcos o medio círculo. X e y son las coordenadas del centro del círculo que contiene este arco, w y h son la anchura y alto del círculo que contiene este arco, star y stop, es donde comienza y termina el ángulo de este arco.  
Se debe activar el modo ángulos en el SETUP(); para que sea más fácil : angleMode(DEGREES);

---

## Desafío de la clase

```
function setup() {
  createCanvas(500, 500); //crea un lienzo de 500 x 500 píxeles
  angleMode(DEGREES); //activa el modo ángulo para los arcos
}

function draw() {
  background(176, 54, 30); //le asigna el color rojo al fondo del lienzo en valores RGB

  strokeWeight(40); //asigna el tamaño del borde a 40 px
  stroke(255, 255, 255); //le asigna el color blanco al borde de la figura en valores RGB
  fill(0, 0, 0); // asigna el color de relleno negro de la figura en valores RGB
  strokeCap(SQUARE); //dale forma recta al borde de mi figura
  arc(250, 250, 200, 200, 90, 270); //dibuja un arco en la coordenada x,y y determina sus medidas

  strokeWeight(40); //asigna el tamaño del borde a 40 px
  stroke(50, 70, 140); //le asigna el color azul al borde de la figura en valores RGB
  fill(230, 210, 117); //asigna el color de relleno amarillo de la figura en valores RGB
  strokeCap(SQUARE); //dale forma recta al borde de mi figura
  arc(250, 250, 200, 200, 270, 90); //dibuja un arco en la cordenada x,y y determina sus medidas

  noStroke(); //elimina el borde de mi figura
  fill(212, 88, 72); //asigna el color de relleno rojo de la figura en valores RGB
  arc(250, 250, 80, 80, 270, 90); //dibuja un arco en la coordenada x,y y determina sus medidas

  fill(176, 54, 30); //asigna el color de relleno rojo de la figura en valores RGB
  triangle(250, 245, 245, 255, 250, 255); //dibuja un triángulo en la coordenada x,y y determina sus medidas

  fill(0, 0, 0); //asigna el color de relleno negro de la figura en valores RGB
  triangle(250, 245, 250, 255, 255, 255); //dibuja un triángulo en la coordenada x,y y determina sus medidas
}
```
![Desafío](https://github.com/user-attachments/assets/90beeb2f-d302-4f1e-aedf-fede446b571a) 
