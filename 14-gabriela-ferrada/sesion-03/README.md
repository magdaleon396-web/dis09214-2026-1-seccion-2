# sesión 03 - 27/03

# CLASE P5.JS

#### Algoritmo

- Es una secuencia de instrucciones paso a paso, LÓGICAS, DEFINIDAS, FINITAS Y ORDENADAS, que permiten solucionar un problema o realizar una tarea específica, tiene 4 características fundamentales:

1) **Precisión:** Cada paso debe estar detallado Y CLARÍSIMO (sin tantas vueltas y ambigüedades)
2) **Orden:** Los pasos llevan una secuencia lógica
3) **Finitud:** Tiene que terminar en algún momento; no puede ser infinitouuuu
4) **Definición:** Si sigues el mismo algoritmo 2 veces con los MISMOS DATOS, ¡deberías obtener el mismo resultado!

- ¡LA MINÚSCULA Y LA mayúscula son súper importantes!
- Con el comando + + : se agranda la interfaz
- SI queremos MOVIMIENTO lo tenemos que colocar en function draw, si NO queremos MOVIMIENTO, o sea que quede con estela, lo colocamos en setup
- No es necesario repetir los códigos en una misma figura, si cambiamos AHÍ SÍ, los escribimos de nuevo
- **comando + shift** te ORDENA el CÓDIGO AUTOMÁTICAMENTE
- SIEMPRE colocar al final del código **;**

### ESTRUCTURA
* Input (Entrada): La info o los ingredientes que necesitas para empezar
  * Proceso: Los pasos lógicos que transforman esa entrada **ALGORITMO**
    * Output (Salida): El resultado FINAL O LA SOLUCIÓN AL PROBLEMA

------------------------------------------------------------
### Diagrama de flujo

-----> Representación gráfica de un algoritmo o de los pasos de un proceso. En programación, se utiliza como herramienta de planificación para visualizar la lógica de un programa antes de escribir una sola línea de código.

----> Se usan componentes ESTÁNDAR **(simbología)**, para que cualquier programador pueda entenderlo
![imagen SIMBOLOGIA diagrama flujo](https://images.ctfassets.net/w6r2i5d8q73s/2n2DPUtFMSCmiP5s5Jdzii/ca83a6fa0cddeed0b4b10784058f627c/simbolos_diagrama_flujo.jpg) 

-------------------------------------------------------

### LENGUAJES DE PROGRAMACIÓN

- Existen entre 700 y 900 lenguajes de programación que se utilizan actualmente en la industria, la academia y el desarrollo de software profesional
- Si incluimos lenguajes antiguos (en desuso tamb), lenguajes creados para la invest, dialectos específicos, etc..., supera los 9.000 según repositorios como (Online Historical Encyclopaedia of Programming Languages)
  
- **Propósito general:** Python, Java, C++, C#
- **Desarrollo web:** JavaScript, TypeScript, PHP, Ruby
- **Sistema de bajo nivel:** C, Rust, Go
- **Análisis de datos:** R, Python, Julia
- **Móvil:** Swift (iOS), Kotlin (Android)

--------------------------------------------------------
**P5.JS (Utiliza principalmente JavaScript)**

- **OJO** ¡¡¡SIEMPREEE SE TERMINA COLOCANDO UN ; para cerrar el código, si no puede tener problemas!!!!!
- **OJO PIOJO** SIEMPRE TIENE QUE ESTAR UNA LLAVE que se llama function draw ----> } , AL FINAL , SI NO LOS CÓDIGOS SALEN CON ERROR

- Librería de JavaScript ----> P5.JS no es un lenguaje nuevo desde cero, sino una library de JavaScript. ¿Qué significa esto? : Que usa toda la potencia y la sintaxis de JavaScript PEROOO te REGALA un "vocabulario" especializado para dibujar, animar y crear cosas visuales de forma mucho más sencilla.

##### FUNCIONES MAESTRAS

1) function setup() { : Se utiliza para crear el lienzo, Se ejecuta una vez al principio
* Su propósito: Configurar el entorno inicial
* ¿Qué pasa aquí? : Defines el tamaño del lienzo (createCanvas), cargas imágenes o sonidos y estableces configuraciones QUE NO CAMBIARÁN (como el color del fondo inicial)

2) function draw() { : Se ejecuta en un bucle infinito (normalmente 60 veces x segundo / lo que permite crear animaciones OMGG)
* Su propósito: Crear movimiento y responder a la interacción en tiempo real
* ¿Qué pasa aquí? : Dibujas formas que cambian de posición, detectas dónde está el ratón o cambias colores gradualmente)

----------------------------------------------------------

**{CREATE CANVAS}** (siempre va dentro del setup)

Sintaxis ----> createCanvas([width], [height], [renderer], [canvas]);
EJEMPLO ----> createCanvas(100, 100);

- createCanvas(width, height); ----> Sirve para crear el lienzo del canvas y determinar su tamaño en píxeles, solo se pone una vez y SIEMPRE dentro del setup();
- [Renderer] ----> Define el motor del renderizado (es para crear cosas 3D)
  * **P2D (default):** Es el modo 2D, Es el que usas por defecto si no escribes nada. Está optimizado para formas básicas, texto e imágenes planas.
    * **WEBGL:** Activa el modo 3D, Utiliza la tarjeta gráfica **(GPU)** de tu computadora. Es **indispensable** si quieres usar funciones como **box(), sphere(), luces o texturas complejas**.
      * **[Canvas]:** Este es el parámetro "oculto" y menos utilizado, pero súper útil si eres desarrollador web. Por defecto, p5.js crea un elemento nuevo y lo pone en tu HTML.

------------------------------------------------------
**{BACKGROUND}**

Sintaxis ----> background(v1, v2, v3, [a]);

EJEMPLO ----> background(250, 150, 228, 150);

- background(v1, v2, v3, [a]); -----> Nos sirve para designar **EL COLOR** de nuestro lienzo canvas / Se puede poner en el setup(); o en el draw(), pero TIENES RESULTADOS DIFERENTES
- [v1, v2, v3] ----> Son los valores de **R, G, B**. La profe nos dejó páginas para buscar colores por su código
  * [Htmlcolorcodes](https://htmlcolorcodes.com/)
  * [Colorspickers](https://colorspicker.net/es/#google_vignette)
- [a] ----> Es el parámetro para el canal alpha, nos sirve para darle **semitransparencia** al color del fondo (0-255) / DONDE **1** es MUY transparente y **255** MUY poco transparente (se puede usar sin este parámetro igual).

##### BACKGROUND ESCALAS

- Escala de grises (1 n°): background(220); (donde 0 es negro y 255 blanco)
- Color RGB (3 n°): background(255, 0, 0); (Rojo, Verde, Azul)
- Nombres de los colores: background('blue'); (siempre entre comillas)
- Transparencia (4 n°): background(0, 0, 255, 50); (R, G, B y el cuarto número es el canal **"Alpha"**) o sea colocamos un número en el cuarto.

##### ESPACIO DE COLOR RGB

- R: Red [0 - 255]
- G: Green [0 - 255]
- B: Blue [0 - 255]
- WHITE: (255, 255, 255)
- BLACK: (0, 0, 0)
- colorMode(RGB); ese es el código

##### ESPACIO DE COLOR HSV / HSB

- H: Hue [0 - 360°]
- S: Saturation [0 - 100%]
- B: Brightness [0 - 100%]
- colorMode(HSB); ese es el código (¡SE coloca en el SETUP!), Ejemplo: Si le quiero bajar el brillo a un morado y que esté en lila, simplemente pongo colormode y lo bajo.

##### ESPACIO DE COLOR HSL

- H: Hue [0 - 360°]
- S: Saturation [0 - 100%]
- L: Lightness [0 - 100%]
- colorMode(HSL); ese es el código

----------------------------------------
¿Pongo el background en setup(); o en el draw();? -------> La posición del background() determina si tu dibujo tiene "memoria" o si se "limpia" constantemente (igual yo lo coloco en el setup() abajo).

--------------------------------------------
## {DIBUJAR EN EL P5.JS}

- Para dibujar ahí, tenemos que entender que el Canvas FUNCIONA CON UN SISTEMA DE COORDENADAS (x, y) como un plano cartesiano, pero hay que tener en cuenta que el punto (0, 0) NO está en el CENTRO, sino en la esquina superior izquierda.
- X es horizontal e Y es en vertical
Ejemplos: el punto de la esquina derecha sería 400x400 (porque eso mide el canvas 400x400), el de la izq al final sería (0, 400), el de la dere (400, 0) y el punto medio sería 200x200

![plano cartesiano](https://p5js.org/_astro/coordinates.DW7JVAkD_Z13e1Vf.png) 

-----------------------------------------------
## FIGURAS GEOMÉTRICAS

- point(x, y); ----> Dibujamos un solo píxel en las coordenadas dadas.
- line(x1, y1, x2, y2); ----> Dibujo una línea desde un punto inicial hasta un punto final
- rect(x, y, ancho, alto); ----> Dibujo un rectángulo, por defecto, x e y definen la esquina superior izquierda
- ellipse(x, y, ancho, alto); ----> Dibujo un óvalo o círculo, a diferencia del rectángulo, x e y definen el centro de la figura
- circle(x, y, diámetro); ---> Es una versión simplificada de la elipse cuando quieres un círculo perfecto
- square(x, y, lado); ----> Es un rectángulo donde todos los lados son iguales
- triangle(x1, y1, x2, y2, x3, y3); ----> Necesitamos sí o sí darle las coordenadas de sus tres esquinas
- quad(x1, y1, x2, y2, x3, y3, x4, y4); ----> Un cuadrilátero, sirve para hacer formas irregulares de cuatro lados

------------------------------------------------

## {TAMAÑO DEL BORDE}

- strokeWeight(); ----> Establece el tamaño del borde de las figuras o el ancho de la línea o punto / SIEMPRE SE PONE ARRIBA DE stroke();
  * Sintaxis: strokeWeight(weight);
    * Ejemplo: strokeWeight(25);
      
- noStroke(); ----> Se usa para que la figura esté sin borde

-----------------------------------------------
## {COLOR DEL BORDE}

- stroke(); ----> Establece el color que se utiliza para dibujar puntos, líneas y contornos de figuras. Se pone SIEMPREEE arriba de la línea de código de la figura
  * Sintaxis: stroke(v1, v2, v3, [alpha]);
   * Ejemplo: stroke(245, 0, 0);

---------------------------------------------

## {FORMA DEL BORDE/LÍNEA}

- strokeCap(); ----> Define la forma del borde de las líneas o el borde de las figuras (por defecto siempre es ROUND, pero está tamb SQUARE Y PROJECT)
  * Sintaxis: strokeCap(cap);
    * Ejemplo: strokeCap(SQUARE);
   
---------------------------------------------
## {RELLENO DE COLOR}

- fill(); ----> Establece el COLOR DE RELLENO DE LA FIGURA, se pone ARRIBA SIEMPRE de la figura que quiero pintar
  * Sintaxis: fill(v1, v2, v3, [alpha]);
    * Ejemplo: fill(252, 159, 216); (aquí se colocan los números del color RGB)

--------------------------------------------
## {FIGURAS GEOMÉTRICAS 2D AVANZADAS}

- arc(); ---> Nos sirve para hacer arcos o medios círculos. X e Y SON LAS COORDENADAS del centro del círculo que contiene este arco, W y H SON LA ANCHURA Y EL ALTO del círculo que contiene este arco, START y STOP es DÓNDE COMIENZA y TERMINA el ángulo de este arco.
  * Sintaxis: arc(x, y, w, h, start, stop)
    * Ejemplo: arc(250, 250, 100, 100, 270, 90)
      
- **angleMode(DEGREES):** La profe dijo que lo activáramos en el **function setup()** PORQUE es más fácil controlar los ángulos con este código
* En p5.js (y en la mayoría de los lenguajes de programación), el grado 0 NO está arriba, sino a la derecha (en el eje X positivo) , **Y se mueve en el sentido del reloj**

- **0° / 0 rad:** A las 3 en punto (derecha)
- **90° / HALF_PI:** A las 6 en punto (abajo)
- **180° / PI:** A las 9 en punto (izquierda)
- **270° / (PI + HALF_PI):** A las 12 en punto (arriba)

![reloj angulos](https://s3.eu-central-1.amazonaws.com/studysmarter-mediafiles/media/1865576/summary_images/SexaCircunferencia.svg?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIA4OLDUDE42UZHAIET%2F20260329%2Feu-central-1%2Fs3%2Faws4_request&X-Amz-Date=20260329T231817Z&X-Amz-Expires=604800&X-Amz-SignedHeaders=host&X-Amz-Signature=dad677852c0af742a1c7079a843809ac60d2d802edbefe2ac796842ea94a5d1d) 

-------------------------------------------

## SOLEMNE 1

- Debemos hacer un dibujo en un papel milimetrado, inspirándonos en un artista que haga obras geométricas o abstractas, puede ser de 25x25 o 50x50 (mejor estaaaa / para que calce mejor en el canvas de p5.js)
- La entrega debe tener formato de bitácora (GitHub), en donde debemos presentar nuestro proyecto, comentar sobre el proceso de réplica que hicimos (¿de quién nos inspiramos?, ¿por qué?, etc...), las dificultades encontradas y sus soluciones, el resultado, el código (comentado SÚPER IMPORTANTE COMENTAR AL LADO SIEMPRE) y el link a su proyecto en el editor de p5.js. Además, incluir fotos de su dibujo y W.I.P.
- SE **entrega** con **link directo GITHUB** y la bitácora de GitHub de las clases anteriores que tenemos anotada SERÁ EVALUADA TAMBIEN 

- **SE ENTREGA ANTES DEL 10 DE ABRIL, OBVIOO ANTES DE LA CLASE!!!**
- Los desafíos tienen que estar públicos, ¡¡¡YA ENTREGUÉ!!!
