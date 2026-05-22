## CLASE 6

## **Funciones propias**

## ** GitHub / Markdown**

Para los apuntes de clase en GitHub se usa un archivo .md, porque ese formato acepta texto con Markdown.


Para escribir código dentro del README se puede usar:

javascript
// bloque de código


Y si es una línea corta dentro de una oración, se usa así: código.

También es importante comentar el código con detalle, como si lo fuera a leer alguien que no sabe programar. La idea es que otra persona pueda entender qué hace cada parte y replicarlo.

Nota importante: angleMode(DEGREES) no sirve para “hacer arcos” o “hacer semicírculos”. Solo configura la forma en que p5.js mide los ángulos, en este caso en grados.

---

## **Pensamiento computacional**

Los 4 pilares son:

- Descomposición
- Reconocimiento de patrones
- Abstracción
- Algoritmos

---

## **Descomposición**

“Dividir para conquistar”.

Consiste en separar un problema grande en partes más pequeñas y manejables.

En diseño, por ejemplo, si quiero visualizar la brecha salarial, no hago todo de una vez. Primero puedo pensar el “sueldo A”, después el “sueldo B”, luego la interacción y finalmente el fondo.

En código esto se relaciona con las funciones propias. En vez de tener un `draw()` enorme y desordenado, puedo separar partes:

```javascript
dibujarIconos();
calcularDiferencia();
```

Así el código queda más limpio.

Nota más de cuaderno: si algo se me empieza a hacer gigante en el `draw()`, probablemente conviene separarlo en funciones.

---

## **Reconocimiento de patrones**

“Encontrar similitudes”.

Es mirar qué cosas se repiten o siguen una misma lógica.

En diseño, si tengo que representar 100 personas, no necesito dibujarlas una por una. Puedo notar que todas tienen una forma parecida, por ejemplo un círculo que cambia de posición.

En código esto se relaciona con los bucles for, porque si hay un patrón, el código puede repetirlo por mí.

---

## **Abstracción**

“Lo importante vs. el detalle”.

Es quedarse con lo necesario y sacar lo que no aporta tanto.

En diseño, para representar presión social no hace falta dibujar toda una sociedad. Puede bastar con un círculo que se achica cuando el mouse se acerca.

En código esto se puede trabajar con variables y map(), por ejemplo transformar `mouseX` en un valor de opacidad, tamaño o movimiento.


---

## **Algoritmos**

“La receta paso a paso”.

Es ordenar reglas para que el sistema sepa qué hacer.

En diseño sería algo como: si el usuario hace esto, pasa esto otro.

En código se conecta con diagramas de flujo y condicionales:

```javascript
if(){

}
else{

}
```

---

## **Tipos de interacción**

### **Interacción discreta**
Ocurre cuando pasa un evento específico, como un clic, y el sistema responde con una acción.

Ejemplo:
```javascript
mousePressed();
```

También puede usarse:

```javascript
if(mouseIsPressed){

}
```

Funciona como acción / reacción.

---

### **Interacción continua**
Ocurre cuando el sistema responde todo el tiempo al movimiento o estado del usuario.

Ejemplo:
```javascript
mouseX
mouseY
```

Se puede usar para cambiar tamaño, color o velocidad.

Nota de cuaderno: si algo depende siempre del mouse, es interacción continua. Si pasa solo cuando hago clic, es más discreta.

---

## **Funciones propias**

Las funciones propias sirven para ordenar el código.

Ideas principales:

- Modularidad
- Reusabilidad

La modularidad es separar el código en partes más pequeñas.

La reusabilidad es poder usar una función varias veces sin escribir todo de nuevo.

---

## **Sintaxis función**

```javascript
function NombreDeLaFuncion(){

}
```

Ejemplo:

```javascript
function draw(){
background(147,104,166);
DibujarFiguras();
}

function DibujarFiguras(){
stroke(70,162,247);
strokeWeight(4);
fill(40,199,64);
ellipse(pelota.x,pelota.y,24,24);
}
```

En este caso, draw() llama a la función DibujarFiguras(). Entonces el dibujo queda separado y más ordenado.

 una función es como guardar una mini tarea con nombre. Después solo escribo ese nombre y se ejecuta todo lo que está adentro.

---

## **Parámetros y argumentos**

Aparece como tema de funciones: “function parameters and arguments”.

Sirve para que una función pueda recibir datos y cambiar según lo que le entregue.
no hacer una función rígida, sino una que pueda variar.

---

