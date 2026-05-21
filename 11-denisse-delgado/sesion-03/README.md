# Sesión 03 - 27/03
#  P5.JS

- Algoritmo: Secuencia de instrucciones finitas, específicas, ordenadas, definidas y sin ambigüedad

- Preparación de sandwich: 

→ Input(entrada): Información o ingredientes y utensilios para empezar

→ Algoritmo: Pasos lógicos que transforman esa entrada(Instrucción)

→ Output: Sandwich terminado, resultado o la solución al problema

- Diagrama de flujo: Representación gráfica del algoritmo o de los pasos, se usa simbología
<img width="544" height="742" alt="4" src="https://github.com/user-attachments/assets/144d0ce6-8c91-4ba0-8c78-579e072e5647" />

→  Simbología:

<img width="866" height="385" alt="1" src="https://github.com/user-attachments/assets/f4c25626-35cd-46c8-ad4a-5f2b1529a8b1" />

- Lenguaje de programación:
<img width="390" height="242" alt="2" src="https://github.com/user-attachments/assets/351f3dd5-f9fd-43b3-afdc-40ed8bec5a21" />

→ Los más conocidos son javascript, python, etc.

→ En p5 se usa una simplificación de javascript

---

## P5 ##
- Referencia: Diccionario

- Para empezar a programar usar el botón de Start coding

- Función setup: Una sola vez al principio, el tamaño del lienzo, sonido, etc. configuraciones que no van a ir cambiando

- createCanvas: Cambia el tamaño del lienzo(ancho, largo)

→ ancho, largo, renderer(p2d o 3d, si esta en 2d no se usa), canvas(parámetro oculto)

- Función draw: Las repite una y otra vez(60 veces por segundo), crea movimiento

→ 220 es un gris

- Background: Colores

→ Escala de grises 220, 0 es negro y 255 es blanco

→ rgb 3 números (255, 0, 0) (rojo, verde, azul) 

→ Nombre de colores: (‘blue’) siempre entre comillas

→ Transparencia: 4 números (0, 0, 255) rgb y el cuarto

- RGB:

→ Negro(0, 0, 0)

→ Blanco(255, 255, 255)

→ rojo(255, 0, 0), verde(0, 255, 0), azul(0, 0, 255)

- Se puede cambair el modo de color en el setup: colorMode(HSB)
- Para desactivar una linea de codigo se pone: //
- Comentar el código: Se pone en español al lado con // antes
- Cada línea de código tenemos que comentarla y nos puede pedir que cambiemos el color en una solemne
- Dibujar en p5: y,x

→ y(vertical) x(horizontal

→0,0 está en la esquina superior derecha

- **Figuras geométricas**: 

→ point: crea un punto (300, 300) son las coordenadas

→ stroke: color del punto(el borde)

→ strokeweight: tamaño del borde(30)

→ line: se define dónde empieza y dónde termina(x1,y1,x2,y2)

→ rect: se define dónde empieza y dónde termina(x1,y1,x2,y2)

*Tiene un borde y fondo(strokeweight es el tamaño del borde)
*fill: fondo de la figura

→ ellipse: ahora la x e y son el centro del círculo(x1,y1,x2,y2) x1 y y1 son las coordenadas y x2 y2 es el tamaño

→ circle: 3 coordenadas: xy y el diámetro

*Para quitar borde es: noStroke()

→ square(x, y, lado)

→ triangle: cada punta tiene una xy(x1,y1,x2,y2,x3,y3)

→ quad: (x1,y1,x2,y2,x3,y3,x4,y4)

→ arc: se pone en el setup: angleMode(DEGREES)

*primero es el centro, esquina derecha, como las agujas del reloj

*(x1,y1,x2,y2,x3,y3) x1 y1 es el centro del circulo, x2y2 son los lados, x3y3 es el angulo

<img width="333" height="227" alt="3" src="https://github.com/user-attachments/assets/6cded2ba-6043-4a2b-a1d3-909c19268f25" />


→ strokeCap(SQUARE): linea cuadrada

→ strokeCap(ROUND): linea cuadrada

→ Guardar: file + save

* Para ordenar el codigo: edit + tindy code
* Para Guardar o copiar link: file + share + edition
