# Sesión 04 - 10/04
### Contenido Movimiento p5
- **Variables**: Constantes y no constantes
- setup es solo una vez, y el draw va cambiando

1. **mousex/ mousey**:
- Variables de sistema numérico que determinan la posición del mouse en las coordenadas X e Y.
- Hace que se mueva la figura con el mouse (mouseX, mouseY);

    * Ejemplo: 
ellipse(mouseX, mouseY, 100,100):  Hace que aparezca un círculo que se mueve con el mouse
ellipse(mouseX, mouseY, mouseX, mouseY): Hace que se agrande o achique según x e y

    * Ejemplo mío: (https://editor.p5js.org/denisse.delgado2/sketches/2XrKuicj1)

    * Ejemplo profe: (https://editor.p5js.org/PoliMujica/sketches/KHG4X-Z6Y)

- Si queremos estela el background tiene que ir arriba si no queremos tiene que ir abajo

2. **Variables integradas del p5**:
 <img width="1109" height="509" alt="2026-04-11 (3)" src="https://github.com/user-attachments/assets/1e094f26-df1a-41aa-b4bc-4499613f909f" />
 <img width="1108" height="574" alt="2026-04-11 (4)" src="https://github.com/user-attachments/assets/6f6852be-1d6e-4b90-819a-29971e80bb0e" />

a. Crea tus propias variables:
- Para declarar una variable podemos usar let para variables dinámicas y const para variables constantes.

<img width="819" height="494" alt="2026-04-11 (5)" src="https://github.com/user-attachments/assets/dc9058ab-8373-46c7-aa9d-ed5a7eb04904" />

b. Declarar variable: let(v. dinámicas): antes se usaba var y const(v. constantes)
   
c. Inicializa tu variable:
   
d. Usa tu variable: 

  * Ejemplo mío: (https://editor.p5js.org/denisse.delgado2/sketches/Fa9LOLvKu)

  * La variable puede tener el nombre que quieran pero la primera palabra va en minúscula y después la otra palabra lleva la primera letra en mayúscula

4. **Javascript objects**: Variables agrupadas
- Es la forma de agrupar muchas variables dentro de una variable. Es una estructura de datos que te permite agrupar valores relacionados bajo un mismo nombre. En lugar de tener muchas variables sueltas, los objetos funcionan como un "contenedor" que organiza la información mediante pares de clave y valor.

- Luego se accede a la información mediante notación de punto.

    *Ejemplo: (https://editor.p5js.org/PoliMujica/sketches/cuJXAPjTm)

    * Después se pone . x (le dices que vaya a esa variable)

    * En lugar de tener muchas variables sueltas, los objetos funcionan como un "contenedor" que organiza la información mediante pares de clave y valor.

<img width="575" height="423" alt="2026-04-11 (6)" src="https://github.com/user-attachments/assets/d36673df-5cb0-4b9d-8dcd-87ec7c0abf54" />

5. **Random()fuction**:
- Devolver numero aleatorio dentro de un rango
- Su trabajo es devolver un número aleatorio dentro de un rango que tú definas.
- Hay 3 tipos:
    * random(): Si no pones nada, devuelve un número decimal entre 0 y 1
    * random(máximo): Devuelve un número decimal entre 0 y el máximo que elijas.
    * random(mínimo, máximo): Devuelve un número decimal entre esos dos valores.

    * Ejemplo mío random b: https://editor.p5js.org/denisse.delgado2/sketches/X7F5EgvgM

    * Ejemplo random c: (https://editor.p5js.org/PoliMujica/sketches/t7x5F6rUt)
   
    * Ejemplo mío random c: (https://editor.p5js.org/denisse.delgado2/sketches/inls94gAi)

    * Ejemplo mio círculo parpadeante: (https://editor.p5js.org/denisse.delgado2/sketches/rK2k1Nqq1)

- Página de tips: (https://kellylougheed.medium.com/rainbow-paintbrush-in-p5-js-e452d5540b25)
- frameRate(12) en el setup hace que vaya más lento, por segundo

5. **Width y height**: (Ancho y alto) Integradas, corresponden a los valores definidos en el createCanvas.

6. **windowWidth, windowHeight**: Permite ajustar el tamaño del lienzo al tamaño de la ventana del navegador, se pone en el setup
- Se pone random(width) y asi solo es random dentro del lienzo

7. **map()fuction**: Convierte el valor de un rango a otro(mapear)
    * Sintaxis: map(valor, min_original, max_original, min_nuevo, max_nuevo)
      *valor: La variable que quieres "mapear" (por ejemplo, mouseX).
      *min_original y max_original: El rango en el que se encuentra ese valor actualmente
      *min_nuevo y max_nuevo: El rango al que lo quieres transformar.

    * Ejemplo mío: https://editor.p5js.org/denisse.delgado2/sketches/nwfzQ3vpi

