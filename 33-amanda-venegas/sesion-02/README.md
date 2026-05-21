# sesión 03 - 27/03

# Pensamiento-computacional

### CRONOGRAMA DE CURSO PENSAMIENTO COMPUTACIONAL 

En el curso PENSAMIENTO COMPUTACIONAL nos introduciremos en el uso del razonamiento lógico,
estructurado y creativo propio de la computación como herramienta para analizar y crear sistemas, flujos y comportamientos.
Comprender la lógica más que la sintaxis 

#### Unidad 1 -> introducción a la computación para el diseño 

Breve historia de la computación.
- Herramientas de documentación técnica: Introducción a Github y markdown.
- Relación entre dibujo y programación.
- Variables y condicionales.
- Organizar el código mediante funciones.

#### Unidad 2 -> Estructuras lógicas y comportamiento

- Bucles y repeticiones.
- Eventos y callbacks.
- Objetos y arreglos.
- Sensores y periféricos: mouse, teclado, webcam, otros.

#### Unidad 3 -> Proyecto computacional básico

- Introducción a interfaces simples y
prototipado en pantalla.
- Aplicación de los contenidos en un sistema funcional.
- Evaluación de la experiencia, lógica y
expresión del sistema.

## Evaluaciones 

Solemne 1   50%
Solemne 2   50% 

TOTAL 70% presentación examen ->  Examen 30% 

---
---
# 🌸 Clase 20/03 parte 1 - Historia breve de la computación 🌸
 

### **Primera fase abstracción**

- Máquina diferencial
Charles Babbage diseñó esta máquina en 1822 para automatizar el cálculo y la tabulación de funciones polinómicas. Estas son expresiones algebraicas formadas por la suma o resta de términos donde una variable x está elevada a potencias no negativas. Se trataba de un dispositivo mecánico de gran escala basado en engranajes; un acercamiento a la automatización de acciones rutinarias que antes realizaban las personas. Babbage nunca pudo construirla, pero años después, el Museo de Ciencias de Londres construyó en 1991 la Difference Engine No. 2 siguiendo los planos originales, y su diseño resultó ser totalmente correcto.

- Máquina Analítica

Diseñada por Charles Babbage entre 1834 y 1837, fue concebida para realizar cualquier tipo de cálculo establecido. Se considera la primera máquina de cálculo completamente automática (podía realizar operaciones más allá de la suma). Babbage dividió esta máquina en dos partes que conceptualmente se mantienen en la actualidad:
  
**El molino:** ->  **La CPU o Procesador**, donde se procesan los datos. 
El almacen -> **La memoria** donde se guardan los datos. 
Las targetas perforadas -> **El Software**  

### Ada lovelace 

Considerada una de las primeras programadoras de la historia y esta le abrió los ojos a Baddage sobre como construir la Máquina (analitica), ella al visitar el **Telar de jacquard** se inspiró para ayudar en el diseño del sistema
Además, fue la primera en crear un algoritmo para ser implementado a al máquina, este sirvia para calcular **Números de Bernoulli**, esto se considera **el primero programa de computación**

## Telar de jacquard (1801) 

Es el primer sistema de almacenamiento de información binaria (0 y 1, o sí o no).
El telar usaba un sistema de tarjetas perforadas para lograr diseños o dibujos complejos, si había agujero, la varilla pasaba (podemos entenderlo como 1 o "encendido") y, si no había agujero, la varilla chocaba contra la tarjeta y quedaba abajo (podemos entenderlo como 0 o "apagado").

-El telar de Jacquard introdujo tres conceptos fundamentales de la computación moderna:

1. La separación entre **Hardware*** y **Software** donde Hardware era la maquina fisica y Software serian las tarjetas perforadas, antes se tenia que reconstruir la máquina para cambiar la tarea, mientras con este sistema solo cambias de programa.
   
2. El sistema binario : Creó un sistema de lógica binaria.
 
3. El pixel y la imagen rasterizada: El tejido podemos entenderlo como una forma primigenia de la imagen de Mapa de bits. 

## La Máquina De Turing

Originalmente fue definida por el matemático inglés **Alan Turing** como una «máquina automática» en 1936. No es una máquina física, es un experimento mental (una máquina teórica). Turing imaginó una cinta infinita, un cabezal que lee/escribe símbolos, y un conjunto de reglas (estados).

> Define la Computabilidad Universal: Turing demostró que una máquina simple, con las instrucciones correctas, puede simular a cualquier otra máquina.

--- 

# Despertar visual 

- Artistas y algoritmos
Los intentos de mezclar el arte con la computación empezaron aproximadamente en 1960 

#### Artistas pioneros

EEUU

- Vera Molnár
- Manfred Mohr
- Georg Nees
- Frieder Nake
- Lillian Schwartz
  
Europa

- Hiroshi Kawano
  
- Computer Technique Group  Japón; y Waldemar Cordeiro, son pioneros 

# Etapa 3 Democratizacion del creative coding 

El Software libre nace formalmente en 1983, cuando Richard Stallman anunció el inicio del Proyecto GNU.

Su objetivo era crear un sistema operativo libre. En 1985 se publica el Manifiesto GNU y se funda la Free Software Foundation (FSF). 

Buscan garantizar 4 libertades esenciales:

 1. Libertad 0 (Uso): La libertad de ejecutar el programa como se desee, con
cualquier propósito.
 2. Libertad 1 (Estudio): La libertad de estudiar cómo funciona el programa y
cambiarlo para que haga lo que el usuario quiera. El acceso al código
fuente es una condición necesaria.
 3. Libertad 2 (Distribución): La libertad de redistribuir copias para ayudar a
otros.
4. Libertad 3 (Mejora): La libertad de mejorar el programa y hacer públicas
las mejoras, para que toda la comunidad se beneficie. El acceso al código
fuente es necesario.

Principios fundamentales adicionales de la FSF:

1. Libertad, no precio: El software libre es una cuestión de libertad
de los usuarios de computadores, no de precio.

2. Copyleft: Se promueve la distribución bajo términos de copyleft,
que garantizan que el software y sus versiones modificadas sigan
siendo libres.

3. Lucha contra restricciones: Campañas activas contra patentes
de software, Gestión Digital de Restricciones (DRM) y otras
amenazas a la libertad de los usuarios.

4. Desarrollo del proyecto GNU: Fomento del desarrollo de un
sistema operativo completamente libre.

---

Hay diferencia entre open source y Software Libre

#### Open sourse 
"Colaboración". El código abierto permite que más ojos revisen errores y mejoren el producto.

#### Software Libre
"Libertad" El usuario debe tener el control de su informática.


---
---

# 🌸 Clase 20/03 parte 2 - Markdown 🌸

- GitHub es una plataforma basada en la nube donde puedes almacenar, compartir y trabajar junto con otros usuarios para escribir código

Titulos

# Titulo Grande h1
## Subtitulo h2
### Pequeño
###### Mas pequeño  h6

---
## Tipos de texto

**Negrita**

*Cursiva*

~~Tachado~~

---
## Listas 

Con puntitos

- Agua
- Pan
- Harina
   * azucar
   * canela

Numeradas 

  1. Primero
  2. Segundo
  3. Tercero
     1. Firts

---
## Linea separadora 

---

## Links 

[google](https://www.google.com/?hl=es)

## Imagenes

![gatos](link de la imagen)

## Bloques 

> habia una vez ........
> 
>> pero paso......

## Emojis

:rocket -> no me funciono pero tmb se puede pegar directamente 

---
---
