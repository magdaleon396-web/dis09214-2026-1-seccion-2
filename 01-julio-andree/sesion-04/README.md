# sesión 04 - 10/04
## Variables: datos que van cambiando  
Mouse X = Determina posición del mouse  
mouse Y = Determina posición del mouse  
Ej. mouseX, mouseY  
Ej. Ellipse (mouseX, mouseY ,ancho de ellipse,alto de ellipse);  
Background en Setup para pintar.  
Background en Draw para seguir el cursor.  
### Crear tus propias variables  
para declarar una variable podemos usar **let** para varias dinámicas y **const** para variables constantes.  
Declarar una variable consta de tres partes:  
* Declarizar tu variable
* Inicializa tu variable
* Usa tu variable
### Javascriptobject  
Nos sirve para agrupar varias variables dentro de una sola variable.  
Es una estructura de datos que te permite agrupar valores bajo un mismo nombre. En lugar de tener muchas variables sueltas, los objetos funcionan como un "contenedor" que organiza la información.  
Luego accedes a esta información mediante puntos ".".  
### Random (); fuction  
Devuelve un valor aleatorio dentro de un rango que tú definas.  
* **random():** si no pones nada te da un valor decimal entre 0 y 1.  
Ej: random() da 0.4571.  
* **random(máximo):** te da un valor decimal entre 0 y el número máximo que tu elijas.  
Ej: random(100) da 67.  
* **random(minimo, maximo):** te da un número decimal entre esos dos valores.  
random(20,50) da un número entre 20 y 50.  
### (width , height);  
variables que corresponden al ancho y el alto del lienzo definidos por el createCanvas. 
### (windowWidth, windowHeight);  
variable que perimite ajustar el tamaño del lienzo al tamaño de la ventana del navegador. Se usan en el crateCanvas.  
### map(); fuction  
función que nos permite pasar de un valor de un rango a otro. Toma un valor que esta a una escala y lo convierte a otra escala de manera proporcional.  
Sintaxis: map(valor, min_original, max_original, min_nuevo, max_nuevo)
* valor: La variable que quieres "mapear" (por ejemplo, mouseX).
* min_original y max_original: El rango en el que se encuentra ese valor actualmente
* min_nuevo y max_nuevo: El rango al que lo quieres transformar.
