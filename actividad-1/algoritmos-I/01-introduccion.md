# Introducción a los algoritmos

## Enunciado

**Tema:** Fórmulas físicas | **Dificultad:** Introducción | **Autor:** Ricardo

Se necesita un algoritmo que, utilizando la siguiente fórmula física de caída libre:

$$t = \sqrt{\frac{2h}{g}}$$

calcule el tiempo que tarda un objeto en caer desde una altura \( h \) (en metros), considerando la aceleración de la gravedad \( g = 9.8 \, \text{m/s}^2 \). El algoritmo debe solicitar al usuario la altura \( h \) y mostrar por pantalla el tiempo calculado.

## Pseudocódigo

```
Algoritmo caida_libre
Inicio
  var t, h, g: Real;
  
  g = 9.8;
  
  Mostrar << "Ingrese la altura a la que se encuentra el objeto en metros. ";
  Leer >> h;
  
  t = [(2 * h) / g] ^ (1/2);
  
  Mostrar << "Su objeto tardará unos ", t, " segundos en caer.";
Fin
```
