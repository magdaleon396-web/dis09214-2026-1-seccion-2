# sesión 05 - 10/04
# Transformaciones y condicionales  

## Ángulos  
angleMode();
Por defecto p5.js ocupa radianes para medir los ángulos.  
Para cambiar a grados se usa esto en el function SETUP: angleMode(DEGREES).  

## Rotación  
rotate();  
Para rotar elementos alrededor del punto de origen (0,0).  
Sintaxis: rotate(valor en radianes o en grados);  
Se recomienda usar con translate();  

## Trasladar  
translate();  
Se traslada el punto de origen (0,0) a otra coordenada del canvas.  
Sintaxis: translate(x,y);  

## Guardar y restaurar  
push();    pop();  
trabajan juntas como un sistema de memoria temoral para el estilo y las transformaciones del lienzo.  

## Escala
scale();  
Ajusta la escala del sistema de coordenadas actual por el factor especificado.  
Sintaxis: scale(x,y);  

## Condicionales  

### Expresión booleana  
Cualquier enunciado, dato o instrucción que, al ser evaluado, solo puede arrojar uno o dos valores posibles: verdadero o falso.  
### Sentencia Condicional  
***If - else if - else***: **If** (condición) {ejecuta este código si es true}. **else if** (condición 2) {ejecuta este código si es true}. **else** {ejecuta ese código si ambas condiciones son falsas}.

