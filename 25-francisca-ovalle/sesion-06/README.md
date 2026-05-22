# Sesión 06 - 24/04 Apuntes  
---  
## 4 PILARES:  
### 1. Descomposición: "Dividir para conquistar" 
Consiste en tomar un problema grande y complejo y romperlo en partes más pequeñas y
ma  
- ***En diseño***: Si quieres visualizar la *"Brecha Salarial"*, no programas todo de una vez.
Primero diseñas cómo se ve el *"Sueldo A"*, luego el *"Sueldo B"*, luego la *"Interacción"* y
finalmente los *"Fondos manejables"*.  
- ***En el código***: Se traduce en el uso de funciones propias. En lugar de un *draw() gigante*,
tienes una función *dibujarIconos()* y otra *calcularDiferencia()*, etc.  

### 2. Reconocimiento de patrones: "Encontrar similitudes"  
Es observar tendencias o regularidades dentro de un problema. Si algo se repite podemos automatizarlo.  
- ***En diseño***: Notas que para representar a 100 personas, no necesitas dibujar 100 veces.
- ***En el código***: Se traduce en el uso de Bucles (for). Si hay un patrón, el código lo repite por
ti con solo tres líneas.
### 3. Abstracción: "Lo importante vs. el detalle"  
Es filtrar la información innecesaria y quedarse solo con las características que definen el
problema. Es crear una representación simbólica de la realidad.  
- ***En diseño***: Para representar la *"presión social"* no necesitas dibujar a toda la sociedad;
quizás un círculo que se achica cuando el mouse se acerca es suficiente.
- ***En el código***: Se traduce en el uso de variables y la función map(). Una posición de
mouse (mouseX) se *"abstrae"* para convertirse en un valor de opacidad o miedo.
### 4. Algoritmos: "La receta paso a paso”  
Es el diseño de una serie de reglas ordenadas para resolver el problema.  
- ***En diseño***: Es el flujo de la experiencia. *"Si el usuario hace esto, pasa aquello; si no,
pasa esto otro”*.
- ***En el código***: Se traduce en el Diagrama de Flujo y en las Condicionales (if/else).
---
## Tipos de interacción:  
### 1. Interacción Discreta (Eventos):  
Es cuando curre un evento específico (clic) y el sistema responde con una acción única (aparecen
círculos). Es un interruptor de *"encendido/apagado"* o *"acción/reacción"*.  
- ***En el código***: Se suele usar dentro de la función *mousePressed()* o con un *if(mouseIsPressed)*.
### 2. Interacción Continua (Input de Datos):  
Es cuando el sistema reacciona constantemente al movimiento o estado del usuario, sin necesidad
de hacer algo especifico (clic).  
- ***En el código***: Usar mouseX o mouseY directamente para afectar el tamaño, color o velocidad
de algo.
---
