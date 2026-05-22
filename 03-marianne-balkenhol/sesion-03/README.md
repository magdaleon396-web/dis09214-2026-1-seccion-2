# **P5.js**

## **Pensamiento computacional**
- Algoritmo = pasos ordenados para resolver un problema.
- Características: precisión, orden, finitud y definición.
- Input = entrada.
- Proceso = transformación.
- Output = resultado.

La idea del algoritmo es que si sigo los mismos pasos debería llegar siempre al mismo resultado. Es como una receta, pero aplicada a lógica.

---

## **Diagramas de flujo**
Representación visual de procesos usando simbología estándar para planificar lógica antes de programar.

Sirven mucho para ordenar ideas antes de escribir código. A veces entender el flujo visualmente es más fácil que leer código directamente.

---

## **Lenguajes**
- Python
- JavaScript
- C++
- Java
- Swift
- Kotlin

Cada lenguaje tiene enfoques distintos. Algunos se usan más para visuales, otros para apps, páginas web o sistemas más complejos.

---

## **p5.js**
Biblioteca de JavaScript enfocada en dibujo, animación y visuales.

```javascript
function setup(){

}

function draw(){

}
```

- setup() → configuración inicial.
- draw( → loop infinito, movimiento e interacción.

setup() ocurre solo una vez, mientras que draw() se repite constantemente. Ahí es donde normalmente pasa el movimiento.

---

## **Canvas + fondo**
```javascript
createCanvas(500,500);

background(255);
background(255,0,0);
background(0,0,255,50);
```

- Canvas = lienzo.
- Background = color fondo.
- RGB + Alpha.
- En setup() queda fijo.
- En draw() se reinicia constantemente.

Si el background() está en draw(), el dibujo se limpia frame por frame. Si no, empiezan a quedar rastros y “memoria” del movimiento.

---

## **Color**
```javascript
colorMode(RGB);
colorMode(HSB);
colorMode(HSL);
```

- RGB = Red, Green, Blue.

RGB funciona más pensando en mezcla de luces, mientras HSB y HSL son más cómodos para controlar tonos y saturación de forma visual.

---

## **Sistema coordenadas**
- (0,0) arriba izquierda.
- X horizontal.
- Y vertical.

A diferencia del plano cartesiano normal, acá el eje Y crece hacia abajo. Eso al principio igual confunde un poco.

---

## **Figuras**
```javascript
point();
line();
rect();
ellipse();
circle();
square();
triangle();
quad();
arc();
```


```javascript
angleMode(DEGREES);
```

Ángulos:
- 0° = derecha.
- 90° = abajo.
- 180° = izquierda.
- 270° = arriba.

Importante: angleMode(DEGREES) no crea arcos, solo cambia la forma en que se miden los ángulos.

---

## **Bordes + relleno**
```javascript
stroke();
strokeWeight();
strokeCap();
fill();
noStroke();
```

- `stroke()` → color borde.
- `strokeWeight()` → grosor.
- `strokeCap()` → forma línea.
- `fill()` → relleno.
- `noStroke()` → sin borde.

Tipos:
- ROUND
- SQUARE
- PROJECT

strokeWeight() cambia muchísimo cómo se siente visualmente una figura. Aunque sea la misma forma, un borde grueso o fino cambia caleta el resultado.
