# Resumen BDD2

## Principio de OLAP (ON LINE ANALYTIC PROCESSING)

Es un principio que responde a la necesidad de mejorar los tiempos de 
respuestas en las bases de datos.
entre las ventajas encontramos que analiza la relaciones entre distintos tipos de datos
y lleva un historial de ellos:

## Que es OLAP

procesamiento analitico en linea, su objetivo es 
agilizar la consulta de grandes cantidades de datos
Para ello utiliza estructuras de datos 
diversas, normalmente multidimensionales (o Cubos OLAP)


## MOLAP

esta base de datos tiene dos niveles y su motor es una base 
de datos multidimiensional y un motor analitico* su estructura optimizada para maximizar las consultas.
y es apropiado para cubos de rapida respuesta

## ROLAP

esta base da datos tiene 3 nivele y funcional por medio de un datawarehouse
cabe mencionar que este sistema es relaciona
* es la mas lenta de todas
* su uso mas frecuente es cuando contamos con grandes conjutos de datos
que no son frecuentemente buscados.

## HOLAP

es un hibrido entre ROLAP Y MOLAP 


## MOLAP

este tambien es relacional, maneja volumenes mas grandes de 

## Que es bussinss Inteligence.

es la habildad de transformar los datos en informacion y 
la informacion en conocimiento

## Que es OLTP
Procesamiento de Transacciones En Línea 
es utilizado en las bases de datos relacionales pero es lento
en consultas multitabla

## DATA MART

es un subconjunto de datos en toda la empresa qu ees de valor para un grupo especifico de 
usuarios. Por ejemplo el data mart de marketing.

El abordaje mas popular para el diseño de datawahrehouse es del modelo multidimensional
Este modelo puede existir en forma de esquema de estrella, esquema de copo de nieve, constelacion de echos.

## que son las bases de datos multidimensionales

Las bases de datos multidimensionales (BDMB) son un tipo de base de
datos optimizada para Data Warehouse que se utilizan principalmente 
para crear aplicaciones OLAP, una tecnología asociada al acceso y análisis de datos en línea.

DBMS esta optimizado para OLTP Y OLAP esta optimizado para data waarehouse

## ETL 

es una herramienta de extraccion y transforamacion de l ainromafion para luego
ser cargada en un data warehouse

## De que fomras peude existir un data warehouse

* Esquema de estrella.
* Esquema de copo de nieve.
* Constelaciond e hechos.

## Que tipo de operaciones se pueden realizar con DataWarehouse?

* Roll up: permite escalar la jerarquia o reducir dimensiones generalizados
* Drill down: permite ir desde un alto nivel de resume a nu nuvel de datos mas detallado.
* Slice : permite hacer un corte o proyeccicon
* Dice: permite seleccionar
* Pivot permite girar el cubo

## cuales son los metodos de accesos a las BDMD
* Arboles b,Tabalas de hash

## Que es un DDS
Es un Servicio de Distribución de Datos para sistemas en tiempo real es un estandar
para  es la especificación de la logica de intercambio de informacion entre aplicaciones.

## Que es un DSS

Es un sistema de soporte para la de descisiones, es una heramienta de bussines intelligence 
enfoada al analis de los datos de la organizacion.
entre sus caracteristicas podemos encontrar:

* informes dinamicos
* no requiere conocimientos previos
* no requiere conocimientos tecnicos
* rapidez en tiempo de respuesta

## Que tipos de DSS podemos encontra

* Sistemas de informacion gerencial
* sistema de informacion ejecutiva
* sistemas expertos basados en inteligencia artifical
* sistemas de apoyo a la deciones de grupo

## Cuale es el finde la optimizacion de consultas

disminuir su tiempo de ejecucion modificando su diseño

## Cuales son las reglas de optimizacion algebraicas de de consultas
* conmutatividad /Asociatividad
* bajar la selecciones(Reduce el numero de tuplas)
* bajar las proyecciones(reduce el tamaño=
* eliminar subconsultas de las condiciones
