# sesión 10 - 05/06   

**ESTADOS Y CÁMARA WEB**   

PASO 1: Crear y definir variable estados.    
1. al principio de tu co´digo (fuera de las funciones)
PASO 2: Configurar el lienzo
2. Creamos el lienzo de fondo donde va a ocurrir toda la magia.
PASO 3: Crear la estructura del estado (function draw)
3. Aquí usamos un switch Dependiendo del valor de la variable estado, el programa dibujará una cosa u otra.
PASO 4: Programar visualmente cada estado (funciones propias)
PASO 5: La lógica del cambio y el reinicio
5. Para pasar de un estado a otro y lograr que vuelva al comienzo, usamos la función mousePressed() Cada vez
que hagas un clic, la variable aumentará. Si llega a 3 (después del estado 2), volverá a 0.


**1. INTERACCIÓN CON EL TECLADO:**
1.1. Por barra espaciadora o Enter:   
1.2. Por teclas específicas (ej.
Números): Puedes hacer que la
tecla 1 te lleve al inicio, la 2 a la
experiencia y la 3 al final.   

**2. BOTONES REALES EN LA PANTALLA**   
2. En lugar de hacer clic en
cualquier parte de la pantalla,
puedes crear un botón real de
HTML usando la librería de p5.js.
Esto es mucho más profesional   
para menús.   

**3. ZONAS DE CLIC:**   
3. Si no quieres usar botones de
HTML y prefieres dibujar tus
propios botones con rect(),
puedes evaluar si el mouse
estaba dentro de esa caja al
hacer clic.   

**4. INTERACCIONES AUTOMÁTICAS:**   
4. Por Tiempo (Temporizador): Ideal para una
pantalla de introducción (Splash Screen) que
dura 3 segundos y pasa sola al menú.   


**INTERACCION CON EL MUNDO FÍSICO**:   
(cámara web)   
createCapture(VIDEO);
1. Crear la variable para la captura, declarar una
variable global que guardará el flujo de video de
tu cámara web.   
2. Inicializar la cámara en el function setup()
utilizamos el comando especial
createCapture(VIDEO) esto le pedirá permiso
al navegador para encender la cámara del
computador. También definimos tamaño con
captura.size(x,y); y es muy importante
agregar captura.hide(); para que esconda el
video que HTML pone abajo por default.   
3. Dibujar la cámara en el function draw()
usamos la función image(). p5.js toma cada cuadro
(frame) de la cámara y lo dibuja en el lienzo en
tiempo real.
