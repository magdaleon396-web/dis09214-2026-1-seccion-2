# CLASE 9
## viernes 5 de junio
**Estados y Camara Web**

# Estados
Los estados permiten tener distintas pantallas o momentos dentro de un mismo proyecto.

Ejemplo:
- estado 0 = inicio
- estado 1 = experiencia
- estado 2 = final

Cada estado muestra cosas diferentes segun el valor de una variable.

---

# Como funcionan

## Paso 1

Crear una variable para guardar el estado actual.

La variable indica en que pantalla estamos.

## Paso 2

Configurar el lienzo en setup().

Es el espacio donde ocurrira toda la experiencia.

## Paso 3

Crear la estructura de estados en draw().

Dependiendo del valor de la variable se muestra una pantalla diferente.

## Paso 4

Programar visualmente cada estado.

Cada estado puede tener:
- colores distintos
- formas distintas
- interacciones distintas
- informacion distinta

## Paso 5

Crear la logica del cambio.

Al cambiar el valor de la variable cambia la pantalla.

Si llega al ultimo estado puede volver al inicio.

---

# Formas de cambiar de estado

## Teclado

Se puede cambiar usando:
- barra espaciadora
- enter
- numeros
- teclas especificas

Ejemplo:

1 = inicio

2 = experiencia

3 = final

---

# Botones HTML

Se pueden crear botones reales en pantalla.

Son utiles para menus y navegacion.

---

# Zonas de clic

En vez de usar botones HTML se pueden dibujar figuras y detectar si el mouse hizo clic dentro de ellas.


---

# Cambio automatico

El estado cambia sin que el usuario haga nada.

Puede ocurrir por:

- tiempo
- puntaje
- eventos del sistema

Ejemplo:

pantalla inicio = 3 segundos

pantalla menu = aparece automaticamente

---

# Interaccion con el mundo fisico

El computador puede recibir informacion desde dispositivos externos.

Ejemplo:
- camara web
- microfono

---

# Camara Web

Permite capturar video en tiempo real desde la camara del computador.

El navegador debe pedir permiso para acceder a ella.

---

# Funcionamiento

## 1. Crear variable

Se crea una variable para guardar la captura de video.

## 2. Inicializar camara

La camara se activa en setup().

Tambien se puede definir:
- ancho
- alto

## 3. Mostrar video

La imagen de la camara se dibuja en el lienzo en tiempo real.

Cada frame se actualiza constantemente.




