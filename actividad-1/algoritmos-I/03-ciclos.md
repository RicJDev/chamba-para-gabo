# Ciclos Repetitivos

## Enunciado

**Tema:** Juego de Feria | **Dificultad:** Introducción | **Autor:** Joan

Desarrollar un Algoritmo que permita llevar el control de un juego de feria, donde se utilizarán los 3 ciclos repetitivos para:

1. Repetir el sistema las veces que sea necesaria (Repetir)
2. Determinar cuando el jugador gana (Mientras)
3. Después que haya jugado, según la cantidad de veces que jugó, que se muestre por pantalla la cantidad de dinero que va debiendo (Para).

Cada jugada cuesta 10$ y solo se puede jugar hasta en 10 oportunidades. Realizar los cálculos pertinentes y usar contadores.

## Pseudocódigo

```
Algoritmo Juego_Feria
Inicio
    Var Cont = 0, Dinero: Entero, Diana = 0, R: Booleano;
    Repetir
        Mostrar<<"(preparando el sistema para un nuevo jugador)";
        Cont = 0;
        Diana = 0;
        Mostrar<<"¡PRUEBA TU SUERTE, Y ATINALE A LA DIANA!";
        Mientras (Diana = 0 or Cont = 10) Hacer;
            Cont = Cont + 1;
            Mostrar<<"(¿el jugador le dio a la diana? 1: Si, 0: No)";
            Leer >> Diana;
        Fin_Mientras
        Si (Cont = 10) Entonces;
            Mostrar<<"¡ERES MUY MALO!";
        Sino
            Mostrar<<"¡ERES MUY BUENO!";
        Fin_Si
        Mostrar<<"A CONTINUACIÓN EL DINERO A DEBER: (*redoble de tambores*)"
        Para (I=0 hasta I=Cont) Hacer;
            Dinero = Dinero + 10;
            Mostrar<<Dinero, "$";
        Fin_Para
        Mostrar<<"¡A PAGAR!";
        Mostrar<<"(¿jugará otra persona? 1:Si, 0: No)";
        Leer>>R;
    Hasta (R = 0);
Fin
```
