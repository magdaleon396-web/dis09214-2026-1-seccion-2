# **Datos Dinámicos y Variables**


## **Movimiento**
Introducción a variables y datos dinámicos para generar interacción y movimiento en p5.js.

Las variables hacen que el sketch deje de ser algo estático. En vez de tener figuras siempre iguales, ahora pueden reaccionar, moverse o cambiar según lo que haga el usuario.

---

## **Mouse**
```javascript
mouseX;
mouseY;
```

Variables integradas que detectan posición del mouse en eje X e Y.

```javascript
ellipse(mouseX, mouseY, 100,100);
```

El círculo sigue al mouse porque mouseX y mouseY están cambiando constantemente. Todo el rato guardan la posición actual del cursor.

---

## **Variables integradas p5**

### Canvas
```javascript
width;
height;
```

- Tamaño definido en createCanvas().

Sirven para no tener que escribir manualmente medidas todo el tiempo.

---

### Mouse
```javascript
mouseX;
mouseY;
pmouseX;
mouseIsPressed;
mouseButton;
```

- Posición actual.
- Posición anterior.
- Detectar click.
- Botón presionado.

pmouseX guarda la posición anterior del mouse, entonces sirve harto para detectar velocidad o dirección de movimiento.

---

### Teclado
```javascript
key;
keyCode;
keyIsPressed;
```

Sirven para detectar teclas y generar interacción con teclado.

---

### Tiempo
```javascript
frameCount;
deltaTime;
```

frameCount nunca deja de subir mientras el sketch corre, entonces puede servir como una especie de contador interno.

---

### Ventana
```javascript
windowWidth;
windowHeight;
focused;
```

Permiten adaptar el sketch al tamaño real de la ventana del navegador.

---

## **Crear variables**
```javascript
let circulo = 0;
const tamaño = 50;
```

- let = variables dinámicas.
- const = variables constantes.
- Antes se usaba var.

**pasos:**
1. Declarar.
2. Inicializar.
3. Usar.


Acá el círculo se mueve porque el valor cambia frame por frame. Si la variable no cambiara, el círculo quedaría quieto.

También se puede pensar como una memoria pequeña que guarda datos mientras el programa funciona.

---

## **Javascript Objects**
Sirven para agrupar variables dentro de una sola estructura.

```javascript
let circulo = {

x:0,
y:200,
diameter:50

};
```

Acceso usando notación punto:

```javascript
circulo.x
circulo.y
```

Es más cómodo tener toda la información junta en vez de muchas variables separadas. Sobre todo cuando empiezan a aparecer varios objetos distintos.

---

## **random()**
Genera números aleatorios.

```javascript
random();
random(100);
random(20,50);
```

Sirve mucho para darle sensación más viva o menos rígida al sketch, porque los valores nunca salen exactamente iguales.

---

## **Width + Height**
```javascript
width;
height;
windowWidth;
windowHeight;
```


Así el canvas se adapta automáticamente al navegador y no queda fijo en un solo tamaño.

---

## **map()**
Transforma un rango de valores en otro.

```javascript
map(valor, minOriginal, maxOriginal, minNuevo, maxNuevo);
```


- Usado para color, tamaño, movimiento e interacción.

Es como traducir un valor a otro lenguaje. Por ejemplo convertir la posición del mouse en color, opacidad o velocidad.

Muy útil cuando quiero que algo responda de manera proporcional y no tan brusca.
