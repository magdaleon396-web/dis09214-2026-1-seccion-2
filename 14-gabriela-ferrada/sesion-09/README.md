# sesión 09 - 29/05

**EXAMEN**
- Ocupar n° proporcionales en el height y el width, para que no se pierda la compocisión del diseño que hagamos (ej: witdh/2 height/2)
- Tener OJO con los diagramas de flujo, se utiliza como una herramienta de planificación para visualizar la lógica de un programa antes de escribir una sola línea de código. No es como un mapa mental.

EJ: 

<img width="971" height="552" alt="Captura de pantalla 2026-06-06 125922" src="https://github.com/user-attachments/assets/da915022-4945-4578-ad8b-df311c8e86f3" />

-----------------------------------------
# Arrays (listas)
----> Es un contenedor que agrupa elementos , en un orden especifico. O sea es un contenedor con compartimentos numerados donde puedes guardar múltiples datos bajo un mismo nombre. Es una lista que mantiene varios datos ordenados. Los arrays son útiles para almacenar datos relacionados y pueden contener datos de cualquier tipo.

- Es como un tren (Que seria el array) con vagones y cada vagon es un elemento donde cada elemento puede tener lo que tu quieras, como: Variables, otros arrays, etc...
<img width="461" height="207" alt="Captura de pantalla 2026-06-06 131441" src="https://github.com/user-attachments/assets/f4eec82e-3fe6-4f43-8e0f-c0e2b11e02d4" />



⭐ En programacion se empieza a contar desde el cero!

SINTAXIS: let nombreArray =[e0 , e1 , e2 , e3 , e4 , e5] ; ----> Contamos SIEMPRE desde el cero.

EJEMPLO: let Colores = [ “red”, “orange”, “yellow”, “green”, “blue”] ;

## ¿Pero como ocupo estos elementos del array?
- Para llamar a alguno de los valores de mi array usamos: nombreArray [ no elemento ]
EJ: background ( Colores[1] ); ---> Esto pintará el fondo de mi lienzo de color anaranjado.

[EJ profe](https://editor.p5js.org/PoliMujica/sketches/6S1tglHiR)

- No se deben declrarar todo arriba, OJO, puedes declarar el array arriba, pero algunas veces tienes que declarar abajo.
- El index : Es para almacenar el valor que esta en el momento, (Se coloca arriba) como let.
- index = 0 , se resetea y se vuelve a empezar a repetir.
- **cons:** se usa para variables que no mutan y son iguales, se coloca al inicio del todo, es parecido al let, pero es una variable constante.

----------------------------------------------
# CLASS (molde)
-----> Define la estructura, datos y comportamientos que tendra un tipo de objeto en especifico.
* Es como un molde de galletita , no es el objeto real en sí , sino las instrucciones empaquetadas para fabricar **infinitas copias independientes** basadas en ese mismo modelo. Se utiliza la palabra clave **new**

LA SINTAXIS BÁSICA: Se estructura SIEMPRE en 3 partes dentro de un bloque de llaves:
1) La palabra clave **class + nombre que le queramos dar**
2) El método constructor (donde se definen las propiedades del objeto usando .this)
3) Las **funciones personalizadas** que definen lo que hace el objeto.

<img width="697" height="306" alt="Captura de pantalla 2026-06-06 140533" src="https://github.com/user-attachments/assets/e01d8285-0f3a-40f4-81d2-f1ef5cb3f21c" />

- Primero se escribe afuera y abajo del function draw(); y despues se CREA en el setup();
<img width="340" height="157" alt="Captura de pantalla 2026-06-06 141114" src="https://github.com/user-attachments/assets/c67cacae-8caa-4dbc-b477-c8da2256da4d" />

- Luego llamamos a sus métodos en el draw();
<img width="325" height="292" alt="Captura de pantalla 2026-06-06 141131" src="https://github.com/user-attachments/assets/a9410e88-fc28-4230-9f00-fe43e391c695" />
  
- Y por ULTIMO abajo del function draw el **class**
<img width="407" height="412" alt="Captura de pantalla 2026-06-06 141146" src="https://github.com/user-attachments/assets/f0e2b268-eeb5-42c4-934f-221eed1f85d5" />

-----------------------------------------------
# Class + Array
-----> Sirve para crear, mover y controlar muchos objetos a la vez (como lluvia, estrellas o burbujas) sin tener que escribir código para cada uno por separado.
* Ej: El **class** es el diseño que dice cómo deben ser todas las galletas x ejemplo (forma, color, tamaño). Cada galleta puede tener tener un sabor o chispitas distintas, pero todas son del mismo molde (class). Y el **array** es como la bandeja en donde se guardan todas esa galletas que se van horneando para poder manejarlas juntas.

1) Creamos el array, se declara una variable al principio de todo, para guardar los objetos.
2) Creamos el class, se definen las variables y las funciones que tendrá cada objeto
3) Llenamos el array en el setup(); , Usamos un for para crear muchas instancias usando la palabra clave **new** y las metemos al array con .push().
4) Animamos en el draw, Usamos otro for para recorrer la bandeja de arriba a abajo y le pedimos a cada objeto que ejecute sus funciones en cada fotograma.

- El [] almacena todos los objetos juntos.

[Ejemplo profe](https://editor.p5js.org/PoliMujica/sketches/8gsrkntPw) 

---------------------------------------------------
- Encargo 05 : Crear nuestro propio sistema de particulas, con 5 imagenes minimo en png.
- [Encargo 05 LOML by gabyferradaexe](https://editor.p5js.org/gabyferradaexe/sketches/U4-rakksS) 

