# sesión 06 - 14/04  
# 4 Pilares  

## 1. Descomposición  
__"Dividir para conquistar"__  
Consiste en tomar un problema grande y complejo y romperlo en partes más pequeñas y manejables.  

*  __En diseño:__ Si quieres visualizar la "Brecha Salarial", no programas todo de una vez. Primero diseñas cómo se ve el "Sueldo A", luego el "Sueldo B", luego la "Interacción" y finalmente el "Fondo".
*  __En el código:__ Se traduce en el uso de Funciones Propias. En lugar de un draw() gigante, tienes una función dibujarIconos() y otra calcularDiferencia(), etc.

## 2. Reconocimiento de patrones  
__"Encontrar similitudes"__  
Es observar tendencias o regularidades dentro de un problema. Si algo se repite o sigue una lógica constante, podemos automatizarlo.  

*  __En diseño:__ Notas que para representar a 100 personas, no necesitas dibujar 100 veces. Notas que todas son un círculo con una posición x distinta.
*  __En el código:__ Se traduce en el uso de Bucles (for). Si hay un patrón, el código lo repite por ti con solo tres líneas.

## 3. Abstracción   
__"Lo importante vs. el detalle"__  
Es filtrar la información innecesaria y quedarse solo con las características que definen el problema. Es crear una representación simbólica de la realidad.  

*  __En diseño:__ Para representar la "presión social" no necesitas dibujar a toda la sociedad; quizás un círculo que se achica cuando el mouse se acerca es suficiente.
*  __En el código:__ Se traduce en el uso de Variables y la función map(). Una posición de mouse (mouseX) se "abstrae" para convertirse en un valor de opacidad o miedo.

## 4. Algoritmos  
__"La receta paso a paso"__  
Es el diseño de una serie de reglas ordenadas para resolver el problema. Es el "plan de acción" que debe seguir el sistema.  

*  __En diseño:__ Es el flujo de la experiencia. "Si el usuario hace esto, pasa aquello; si no, pasa esto otro”.
*  __En el código:__ Se traduce en el Diagrama de Flujo y en las Condicionales (if/else). Es el mapa lógico que conecta todas las partes anteriores.

## Tipos de interacción  
1. Interaccion discreta (eventos):
Es cuando ocurre un evento específico (clic) y el sistema responde con una acción única (aparecen círculos). Es un interruptor de "encendido/apagado" o "acción/reacción".
 *  __En el código:__ Se suele usar dentro de la función mousePressed() o con un if(mouseIsPressed).

2. Interacción continua (input de datos):
Es cuando el sistema reacciona constantemente al movimiento o estado del usuario, sin necesidad de hacer algo específico (clic).
*  __En el código:__ Usar mouseX o mouseY directamente para afectar el tamaño, color o velocidad de algo.





