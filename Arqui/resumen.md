# Resumen de Arquitectura 2

## Unidad de memoria

 Es un grupo de registros direccionable atravez del bus de direcciones mediante el cual el procesador coloca una direccion para poder acceder a ella 
## Segmentacion de la memoria
Se refiere al manejo de bloques de tamaño variable en memoria virtual y la conversión de estos segmentos a memoria real.  
esta se compone de la siguiente manera:
Segmento:Desplazamiento
Ejemplo A4FB:4872

## Segmentacion de la memoria fisica y sus registros de desplazamiento en 8086

| Registros de segmento   | Registros de proposito general(Offset) |
|-------------------------|:--------------------------------------:|
| Segmento de codigo (CS) |        IP (Instruccion Pointer)        |
| Segmento de data(DS)    |            SI(Source Index)            |
| Segmento de stack(SS)   |              right-aligned             |
| Segmento extra(ES)      | DI(destination Index)                  |

## Caracteristicas del 8086
* Procesador de 16 bits
* Bus de direcciones de 20 bits(puede direccionar 1mb de memoria)
* Bus de datos interno 16 bits
* 89 instrucciones
* no tiene coprocesador

## Direccion Lógica
Esta esta compuesta por un segmento y un desplazamiento

## Division del 8086

Internamente el 8086 y 8086 tienen dos componentes los cuales son:
* Interfaz del Bus (BIU)
* Unidad de ejecucion (EU

## Interfaz del bus (BIU)
Maneja la lectura y escritura desde y hacia la memoria y los puertos 
de entrada y salida


## Unidad de ejecucion (EU)
Procesa las instrucciones del CPU. esta conformada por la mayoria de sus registros generales, los registros indices y apuntadoes, los flags, la alu y la lógica de control que maneja todo el proceso para ejecutar todas las instrucciones.

![Arqui 8086](http://www.eeeguide.com/wp-content/uploads/2018/08/8086-Internal-Architecture.jpg)

## Registros del procesador 
Los registros del procesador, se usan para contener los datos con que se estan trabajando puesto que el acceso a los registros es mas rapido que los accesos a memoria,
Se pueden realizar todos esas operaciones con todos los registros menos los de segmento, el ip y los flags
