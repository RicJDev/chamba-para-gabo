# Estructuras Condicionales

## Enunciado

**Tema:** Convertir | **Dificultad:** Examen | **Autor:** Joan

Desarrollar un Algoritmo que le permita al usuario saber cuánto equivalen exactamente diferentes representaciones del tiempo, teniendo en cuenta que: 

- 1 año = 365 días.
- 1 día = 24 horas.
- 1 hora = 3600 segundos.

El usuario podrá elegir qué formato elegir y deberá mostrar por pantalla todas las conversiones (Segundos, Horas, Días, Años). Realizar los Cálculos pertinentes.

## Pseudocódigo

```
Algoritmo Convertir
Inicio
    Var opc: entero, x, segundos, horas, dias, year: real, opcion: cadena;
    Mostrar<<"Bienvenido, a continuación escoja su opción, y se mostrará por pantalla todo convertido";
    Mostrar<<"1. Segundos";
    Mostrar<<"2. Horas";
    Mostrar<<"3. Dias";
    Mostrar<<"4. Años";
    Leer>>opc; 
    Si (opc < 1 or opc > 4) Entonces;
        Mostrar<<"Opción inválida, escoja nuevamente";
        Mostrar<<"1. Segundos";
        Mostrar<<"2. Horas";
        Mostrar<<"3. Dias";
        Mostrar<<"4. Años";
        Leer>>opc; 
    Fin_si
    En Caso (opc > 0) Sea;
        Caso (opc = 1):
            Mostrar<<"Ingrese la cantidad de Segundos que desea convertir a Horas, Días, y Años:";
            Leer>>x;
            segundos = x;
            horas = x / 3600;
            dias = x / (3600 * 24) ;
            year = x / (3600 * 24 * 365);
            opcion = "Segundos";
        Caso (opc = 2):
            Mostrar<<"Ingrese la cantidad de Horas que desea convertir a Segundos, Dias, y Años:";
            Leer>>x;
            segundos = x * 3600;
            horas = x;
            dias = x / 24;
            year = x / (24 * 365);
            opcion = "Horas";
        Caso (opc = 3):
            Mostrar<<"Ingrese la cantidad de Días que desea convertir a Segundos, Horas, y Años:";
            Leer>>x;
            segundos = x * (3600 * 24);
            horas = x * 24;
            dias = x;
            year = x / 365;
            opcion = "Dias";
        Otro Caso:
            Mostrar<<"Ingrese la cantidad de Años que desea convertir a Segundos, Horas, y Días:";
            Leer>>x;
            segundos = x * (3600 * 365 * 24 );
            horas = x * (365 * 24);
            dias = x * 365;
            year = x ;
            opcion = "Años";
    Fin_caso
    Mostrar<<"Tus resultado de: ", opcion, ", fue exitosa, las conversiones son las siguientes:";
    Mostrar<<"Segundos: ", segundos;
    Mostrar<<"Horas: ", horas;
    Mostrar<<"Dias: ", dias;
    Mostrar<<"Años: ", year; // Nota: en el original dice "years", pero la variable es "year"
Fin
```
