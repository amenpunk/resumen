# Resumen de Arquitectura 2

## Unidad de memoria

 Es un grupo de registros direccionable atravez del bus de direcciones mediante el cual el procesador coloca una direccion para poder acceder a ella 
## Segmentacion de la memoria
Se refiere al manejo de bloques de tamaño variable en memoria virtual y la conversión de estos segmentos a memoria real.  
esta se compone de la siguiente manera:
Segmento:Desplazamiento
Ejemplo A4FB:4872

## Buses en la arquitectura de Von Neuman
Tanto la memoria de datos, como la memoria de programa se encuentran en el mismo lugar en von Neuman y son afectadas por los
tres buses (datos,control,direcciones) el de controes el que le ayuda ala unidad de control a condinar en que momento se habilitan que
puertos y el bus de direcciones que devuelve las direcciones de la memoria ubicandolas pero es le bus de datos el que lee el dato

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
de entrada y salida, Proporciona un bus de datos bidireccional completo de 16 bits y un bus de direcciones de 20 bits.

## Funciones de la unidad de interfaz de bus:
1.  Envía la dirección de la memoria o E / S. 
2.  Obtiene instrucciones de la memoria. 
3.  Lee datos del puerto / memoria. 
4.  Escribe datos en el puerto / memoria. 
5.  Es compatible con la cola de instrucciones. 
6.  Proporciona la instalación de reubicación de direcciones.

Continue reading at http://www.eeeguide.com/8086-internal-architecture/



## Unidad de ejecucion (EU)
Procesa las instrucciones del CPU. esta conformada por la mayoria de sus registros generales, los registros indices y apuntadoes, los flags, la alu y la lógica de control que maneja todo el proceso para ejecutar todas las instrucciones.

![Arqui 8086](http://www.eeeguide.com/wp-content/uploads/2018/08/8086-Internal-Architecture.jpg)

## Registros del procesador 
Los registros del procesador, se usan para contener los datos con que se estan trabajando puesto que el acceso a los registros es mas rapido que los accesos a memoria,
Se pueden realizar todos esas operaciones con todos los registros menos los de segmento, el ip y los flags



