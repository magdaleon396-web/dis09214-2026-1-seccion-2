# **Transformaciones y Condicionales**


**ÁNGULOS:**

angleMode();

Por defecto p5.js usa radianes para cambiar a grados:
- angleMode(DEGREES);

Hay que pensarlo con pi:

---

**ROTACIÓN:**
Siemore rota alrededor del punto de origen (0,0)
Se ecomienda usar con translate();
y en algunos casos con rectMode(CENTER);


---


**PUSH**

si yo quiero que un objeto gire para el sentido contrario le pongo un -

```javascript
angleMode(RADIANS);
```

Para usar grados:

```javascript
angleMode(DEGREES);
```

Equivalencias:
- TWO_PI = 360°
- PI = 180°
- HALF_PI = 90°
- QUARTER_PI = 45°

---

## **rotate()**
Sirve para rotar elementos.

```javascript
rotate(20);
```

- Siempre rota desde `(0,0)`.
- Recomendado usar con `translate();`
- A veces junto a `rectMode(CENTER);`

---

## **translate()**
Mueve el punto de origen del canvas.

```javascript
translate(200,200);
```

- Cambia posición del `(0,0)`.

---

## **push() + pop()**
Sistema de memoria temporal para transformaciones y estilos.

```javascript
push();

// cambios

pop();
```

- Guarda estado.
- Restaura estado anterior.

---

## **scale()**
Cambia escala del sistema coordenadas.

```javascript
scale(2,2);
```

- Agranda o reduce elementos.

---

# **Condicionales**

## **Booleanos**
Solo pueden ser:
- true
- false

---

## **if - else if - else**
Estructura condicional.

```javascript
if(condicion){

// código

}
else if(condicion2){

// código

}
else{

// código

}
```

