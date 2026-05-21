# Sesión 05 - 17/04
## TRANSFORMACIONES & CONDICIONALES (If - else)

- El p5 mide los ángulos en radianes
- Con el agle mood(degree) se trabaja en grados

<img width="1027" height="590" alt="2026-05-21" src="https://github.com/user-attachments/assets/e6186f5d-8007-41f5-8b0f-b408c68bbd33" />

1) **Ángulos** → angleMode() 
    * Se mueve como las agujas del reloj
    * Grados→ En el setup se pone angleMode(DEGREES)

<img width="453" height="377" alt="2026-05-21 (1)" src="https://github.com/user-attachments/assets/4ff92660-bf01-4ba1-bf0c-d4bc930f3a3b" />

2) **Rotación** → rotate(valor radianes o grados)
- Siempre rota desde el punto de origen 0,0
- Usar el translate antes que el rotate
- rectMode(CENTER): Hace que todo esté al centro

Ej profe: (https://editor.p5js.org/PoliMujica/sketches/XFVDpysTg)

3) **Trasladar**→ translate(x,y);
- Sirve para trasladar el PUNTO DE ORIGEN (0,0) a otra coordenada de mi canvas.

Ej profe: (https://editor.p5js.org/PoliMujica/sketches/ddsUf63Oy)

4) **Push y pop** → Guardar y restaurar, sistema de memoria temporal, lo que pase dentro no afecta lo demás
- push() pop()
- Hay una lista de cosas que se quedan adentro al usar el menos gira hacia el otro lado

Ej profe: (https://editor.p5js.org/PoliMujica/sketches/XmQz1O5p9)

5) **Escala** → scale(x,y)
- Hace zoom

Ej profe: (https://editor.p5js.org/PoliMujica/sketches/Rxcg579Jx)

—

### CONDICIONALES
- Expresión booleana: Enunciado que puede ser verdadero o falso
    * Ejemplo: Si algún estudiante apaga por completo las luces de la sala, la profesora debe bailar.

#### OPERADORES
-  Para construir este tipo de expresiones se utilizan 3 tipos de operadores:
operadores:  3 tipos
1.  Operandos(o valores) Son los datos básicos que se evalúan. Pueden ser:
• Variables: (como x, y o mouseX, mouseY, etc).
• Constantes o Literales: Valores fijos como 5, "Hola" o los mismos valores booleanos True y False.

2. De comparación: Contrastar dos valores
• == (Igual a)
• != (Diferente de)
• > o < (Mayor o menor que)
• >= o <= (Mayor o igual / Menor o igual)

<img width="1358" height="718" alt="2026-05-21 (2)" src="https://github.com/user-attachments/assets/5db9d244-6eeb-4356-87b8-9a3e1b709a50" />

Ejemplos:
   * menor que < y mayor que > : Al comparar números, el operador devuelve un booleano basado en la comparación matemática.
     
   * Al comparar cadenas de texto, el operador compara carácter por carácter basándose en su orden alfabético.
     
   * menor o igual que: <= y mayor o igual que: >=  : Similar a < y >, pero también devuelve true cuando ambos valores son iguales.
  
   * Lo mismo se aplica a las cadenas de texto, comparando siempre su orden alfabético.
   
   * Igual == y No igual != : El operador igual == devuelve true cuando los operandos son iguales y false cuando no lo son, mientras que el no igual != devuelve true cuando los operandos no son iguales y false cuando son iguales.

<img width="732" height="622" alt="2026-05-21 (3)" src="https://github.com/user-attachments/assets/0d4d76c8-190a-47ce-b291-53ef037aa6f3" />

3. Lógicos: Combinar dos expresiones
• AND (&&): Es verdadero solo si ambas partes son verdaderas.
• OR (||): Es verdadero si al menos una de las partes es verdadera.
• NOT (!): Invierte el valor (si era verdadero, pasa a ser falso).

Ejemplos:
AND && : El operador AND devuelve true solo si los dos operandos son true; de lo contrario, devuelve false. Por ejemplo:

OR || : A diferencia de AND, OR devuelve true cuando al menos uno de los operandos es igual a true.

NOT ! : El operador NOT devuelve el opuesto del valor booleano actual.

<img width="1179" height="591" alt="2026-05-21 (5)" src="https://github.com/user-attachments/assets/724b3d3b-9d55-420b-908e-1565aca47742" />

SENTENCIA CONDICIONAL(IF- ELSE IF - ELSE)
- IF : Evalúa una condición; si es verdadera, ejecuta el código.
ej: Si algún estudiante apaga por completo las luces de la sala, la profesora debe bailar.
    * La sentencia if puede complementarse con la sentencia else if, que añade
condiciones de prueba complementarias a la original, y con la sentencia else, que implica todos los casos que no cumplen con la condición original. (Nota: puedes añadir tantas sentencias else if como desees).

- ELSE IF : Permite evaluar múltiples condiciones en secuencia si la anterior fue falsa.
    * Si no pasa nada haz esta otra cosa

- ELSE: Ejecuta código alternativo si la condición if es falsa.
    * {ejecuta este código si ambas condiciones son falsas}

Ej: Si algún estudiante apaga por completo las luces de la sala, la profesora debe bailar.
Si no se cumple lo anterior SI la ayudante se levanta de su silla, la profesora debe cantar.
Y SI NO SE CUMPLEN NINGUNA DE LAS ANTERIORES, los estudiantes guardan silencio.

Ejemplo square profe: (https://editor.p5js.org/PoliMujica/sketches/ZxBqL-b9-)
Ejemplo carita feliz: (https://editor.p5js.org/PoliMujica/sketches/ZxBqL-b9-)

- Está mouse is pressed vs mousepressed

- Encargo 4 (https://editor.p5js.org/denisse.delgado2/sketches/5aRY-Q9a7)

