# Sub Algoritmos

## Enunciado

**Tema:** Conversor de escalas | **Dificultad:** Examen | **Autor:** Daniel

Se necesita la creación de un algoritmo para convertir de una escala de temperatura a otra. Como de grados Celsius a Fahrenheit y viceversa, de Celsius a Kelvin y viceversa y de Fahrenheit a Kelvin y viceversa, recuerde que para convertir el valor de la temperatura de una escala a otra se emplean las siguientes fórmulas:

| Conversión | Fórmula |
|:---|:---|
| De Celsius a Fahrenheit | $°F = (°C \times 1.8) + 32$ |
| De Fahrenheit a Celsius | $°C = (°F - 32) \div 1.8$ |
| De Celsius a Kelvin | $K = °C + 273.15$ |
| De Kelvin a Celsius | $°C = K - 273.15$ |
| De Fahrenheit a Kelvin | $K = (°F - 32) \div 1.8 + 273.15$ |
| De Kelvin a Fahrenheit | $°F = (K - 273.15) \times 1.8 + 32$ |

Emplear sub-algoritmos para optimizar los procesos de conversión y tener en cuenta que no se conoce la cantidad exacta de veces que se desea convertir de una escala a otra.

## Pseudocódigo

```
Algoritmo Coversor_Temperaturas 
Inicio 
 Var OPC : Entero, Temp : Real, R : Booleano;
 Repetir 
  Menu (OPC);
  Mostrar<< Menu;
  En_Caso ( OPC > 0 )Sea;
     Caso ( OPC = 1 );
    Celsius_Fahrenheit ( Temp );
    Mostrar<< Celsius_Fahrenheit;
   Caso ( OPC = 2 );
    Fahrenheit_Celsius ( Temp );
    Mostrar<< Fahrenheit_Celsius;
   Caso ( OPC = 3 );
    Celsius_Kelvin ( Temp );
    Mostrar<< Celsius_Kelvin;
   Caso ( OPC = 4 );
    Kelvin_Celsius ( Temp );
    Mostrar<< Kelvin_Celsius;
     Caso ( OPC = 5 );
    Fahrenheit_Kelvin ( Temp );
    Mostrar<< Fahrenheit_Kelvin;
     Otro_Caso 
    Kelvin_Fahrenheit ( Temp );
    Mostrar<< Kelvin_Fahrenheit;
  Fin_Caso

  Mostrar<<"Desea realizar otra conversion ?";
  Mostrar<<"1: Si | 0: No";
  Leer>> R;
  Hasta ( R = 0 );
 Fin_Repetir
Fin


Procedimiento Menu ( E/S: OPC : Entero ) ;
 Inicio
  Mostrar<<"*****CONVERTIDOR DE TEMPERATURAS*****";
  Mostrar<<"1. Convertir de Celsius a Fahrenheit";
  Mostrar<<"2. Convertir de Fahrenheit a Celsius";
  Mostrar<<"3. Convertir de Celsius a Kelvin";
  Mostrar<<"4. Convertir de Kelvin a Celsius";
  Mostrar<<"5. Convertir de Fahrenheit a Kelvin";
  Mostrar<<"6. Convertir de Kelvin a Fahrenheit";
  Leer>> OPC;
  
  Mientras ( OPC < 1 Or OPC > 6 ) Hacer;
   Mostrar<<"Opcion invalida, ingrese un valor valido 1-6";
   Leer>> OPC;
  Fin_Mientras
Fin_Procedimiento 

Procedimiento Celsius_Fahrenheit ( E/S: Temp : Real );
Inicio
 Mostrar<<"Ingrese la temperatura en Celsius";
 Leer>> Temp ;
 Temp = ( Temp * 1.8 ) + 32;
 Mostrar<<"La temperatura en Fahrenheit: ", Temp, " (°F)";
 Mostrar<<"*************************************";
Fin_Procedimiento

Procedimiento Fahrenheit_Celsius ( E/S: Temp : Real );
Inicio
 Mostrar<<"Ingrese la temperatura en Fahrenheit";
 Leer>> Temp ;
 Temp = ( Temp - 32 ) / 1.8;
 Mostrar<<"La temperatura en Celsius: ", Temp, " (°C)";
 Mostrar<<"*************************************";
Fin_Procedimiento 

Procedimiento Celsius_Kelvin ( E/S: Temp : Real );
Inicio
 Mostrar<<"Ingrese la temperatura en Celsius";
 Leer>> Temp ;
 Temp = Temp + 373.15;
 Mostrar<<"La temperatura en Kelvin: ", Temp, " (°K)";
 Mostrar<<"*************************************";
Fin_Procedimiento

Procedimiento Kelvin_Celsius ( E/S: Temp : Real );
Inicio
 Mostrar<<"Ingrese la temperatura en Kelvin";
 Leer>> Temp ;
 Temp = Temp - 373.15;
 Mostrar<<"La temperatura en Celsius: ", Temp, " (°C)";
 Mostrar<<"*************************************";
Fin_Procedimiento

Procedimiento Fahrenheit_Kelvin ( E/S: Temp : Real );
Inicio
 Mostrar<<"Ingrese la temperatura en Fahrenheit";
 Leer>> Temp ;
 Temp = [( Temp - 32 ) / 1.8 ] + 273.15;
 Mostrar<<"La temperatura en Kelvin: ", Temp, " (°K)";
 Mostrar<<"*************************************";
Fin_Procedimiento

Procedimiento Kelvin_Fahrenheit ( E/S: Temp : Real );
Inicio
 Mostrar<<"Ingrese la temperatura en Kelvin";
 Leer>> Temp ;
 Temp = [( Temp - 273.15 ) * 1.8 ] + 32;
 Mostrar<<"La temperatura en Fahrenheit: ", Temp, " (°F)";
 Mostrar<<"*************************************";
Fin_Procedimiento
```
