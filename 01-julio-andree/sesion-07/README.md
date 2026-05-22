# sesión 07 - 15/04
## Loops While & Loops  
Bucle: serie de instrucciones que se repiten de manera indefinida.  
Loop: Estructura de control que perimite ejecutar un bloque de instrucciones de manera repetitida, mientras se cumpla una condición específica.  
### While  
son utiles para repetir instrucciones mientras una condicion sea verdadera.  
While(condición booleana){ejecuta este codigo si es true};  
Ej.  ```While(x sea menor o igual que el alto de mi lienzo){x incrementará en 1 cada vez};  
(definir x antes del While)```  
### For  
Forma de repetir un bloque de código  
For(inicialización variable; condición booleana; actualización){lo que queremos que pase cuando la condición sea verdadera};  
Ej. ```For (let x=0; x<= width, x=x+1){ellipse (x,200,random(300))}```  
{}: todo lo que esté en las llaves es lo que se va a repetir.  
### Nested Loop  
Un for dentro de otro for. Nos sirve para rellenar toda la pantalla sin necesidad de hacer mas líneas de codigo por separado.  
For (Inicialización variable; condición boolena; actualización){  
lo que queremos que pase cuando la condición sea verdadera  
For (Inicialización variable; condición boolena, actualización){  
lo que queremos que pase cuando la condición sea verdadera  
}      
Ej. ```for (let x = 0; x <= width; x = x + 25) {  
for (let y = 0; y <= width; y = y + 25) {  
    fill(233, 127, 168);  
    ellipse(x, y, 50);  
    }  
}```  
Se ejecuta primero el segundo loop hasta que se cumpla la condición, luego hace el primer loop nuevamente.  
### FrameCount  
Variable númerica que cuenta la cantidad de fps desde que comenzó el boceto.  

