# Resumen BDD2

## Principio de OLAP (ON LINE ANALYTIC PROCESSING)

Es un principio que responde a la necesidad de mejorar los tiempos de 
respuestas en las bases de datos.
entre las ventajas encontramos que analiza la relaciones entre distintos tipos de datos
y lleva un historial de ellos:

## Que es OLAP

Procesamiento analitico en linea, su objetivo es 
agilizar la consulta de grandes cantidades de datos
Para ello utiliza estructuras de datos 
diversas, normalmente multidimensionales (o Cubos OLAP)


## MOLAP

Esta base de datos tiene dos niveles y su motor es una base 
de datos multidimiensional y un motor analitico su estructura optimizada para maximizar las consultas.
y es apropiado para cubos de rapida respuesta

## ROLAP

Esta base da datos tiene 3 niveles y funciona por medio de un datawarehouse
cabe mencionar que este sistema es relacional
* Es la mas lenta de todas
* Su uso mas frecuente es cuando contamos con grandes conjutos de datos
que no son frecuentemente buscados.

## HOLAP

Es un hibrido entre ROLAP Y MOLAP 


## MOLAP

Requiere un preprocesamiento y almacenamiento de la información contenida en el cubo OLAP

## Que es Bussinss Inteligence.

es la habildad de transformar los datos en informacion y 
la informacion en conocimiento

## Que es OLTP
Procesamiento de transacciones en línea 
es utilizado en las bases de datos relacionales pero es lento
en consultas multitabla

## DATA MART

Es un subconjunto de datos de toda la empresa que es de valor para un grupo especifico de 
usuarios. Por ejemplo el data mart de marketing.

El abordaje mas popular para el diseño de datawahrehouse es del modelo multidimensional
Este modelo puede existir en forma de esquema de estrella, esquema de copo de nieve, constelacion de echos.

## Que son las bases de datos multidimensionales

Las bases de datos multidimensionales (BDMB) son un tipo de base de
datos optimizada para Data Warehouse que se utilizan principalmente 
para crear aplicaciones OLAP, una tecnología asociada al acceso y análisis de datos en línea.

DBMS esta optimizado para OLTP Y OLAP esta optimizado para data waarehouse

## ETL 

Es una herramienta de extraccion y transforamacion de la informacion para luego
ser cargada en un data warehouse

## De que formas puede existir un data warehouse

* Esquema de estrella.
* Esquema de copo de nieve.
* Constelacion de hechos.

## Que tipo de operaciones se pueden realizar con DataWarehouse?

* Roll up: permite escalar la jerarquia o reducir dimensiones generalizados
* Drill down: permite ir desde un alto nivel de resume a un nivel de datos mas detallado.
* Slice : permite hacer un corte o proyeccicon
* Dice: permite seleccionar
* Pivot permite girar el cubo

## cuales son los metodos de accesos a las BDMD
* Arboles b,Tabalas de hash

## Que es un DDS
Es un Servicio de Distribución de Datos para sistemas en tiempo real, Es un estandar
para  es la especificación de la logica de intercambio de informacion entre aplicaciones.

## Que es un DSS

Es un sistema de soporte para la de descisiones, es una heramienta de bussines intelligence 
enfoada al analis de los datos de la organizacion.
entre sus caracteristicas podemos encontrar:

* Informes dinamicos
* No requiere conocimientos previos
* No requiere conocimientos tecnicos
* Rapidez en tiempo de respuesta

## Que tipos de DSS podemos encontra

* Sistemas de informacion gerencial
* Sistema de informacion ejecutiva
* Sistemas expertos basados en inteligencia artifical
* Sistemas de apoyo a la deciones de grupo

## Cual es el finde de la optimizacion de consultas

Disminuir su tiempo de ejecucion modificando su diseño

## Cuales son las reglas de optimizacion algebraicas de de consultas
* Conmutatividad /Asociatividad
* Bajar la selecciones(Reduce el numero de tuplas)
* Bajar las proyecciones(reduce el tamaño)
* Eliminar subconsultas de las condiciones

## Cuales son las causas principales de una respuesta pobre?

* 60% programacion
* 20% diseño
* 17.5 Base de datos
* 2.5 Sistema*

## Como calcular el coste de una consulta

El optimizador se base en las estadisticas almacenadas en el catalogo de oracle,
atravez de instrucciones

``` sql

ANALYZE [TABLE,INDEX][COMPUTE,ESTIMATE] STATISTICS;

```

## Normas básicas de optimizacion 

* Las condiciones; tanto de filtro como de join deben ir en el orden que esta definido el indice.
* Al crear restricciones de tipo PRIMARY KEY o unice se crea automaticamente un idnice sobre esa columna
* Para chequeos, es siempre mejor crear restricciones (Constraints) que (triggers)
* se deben optimizar dos tipos de instrucciones: las que consumen mucho timpo de ejeuccion o se ejeutan muchas veces
* generar un plan para todas las consultas de la aplicacion.
* si una palicacion que era rapida se vuelve lenta hay que analizar los factores que pudieron cambiar 
* utiliza siempre las mismas consultas ya que se ahorrara tiempo de parsing.
* las consultas mas usadas deben volverse procedimientos almacenados
* los filtros de las consultas deben ser lo mas especificos posible
* no se deben lanzar consultas de forma repetida o en forma de ciclo
* evitar condiciones IN en " SELECT ", sustituyendolas por joins
* No meter un select dentro de un IN
* Cuando se hace una consulta multitabla el orde en que se pone el from infule el plan de ejecucion
* Si en la cláusula where se utiliza campos indexados como argumentos de funciones, el indice quedara desactivado.
* Evitar las funciones de conversion de tipo de datos 
* una condicion negada con "NOT" desactiva los indices
* una consulta que utiliza la cláusula dinsctin debe ser ordenada
* Desactivar los indicies si se va realizar una operacion masiva de borrado, insercion o actualizacion.


## 15 Consejos para optimizar Consultas SQL

* Se debe tener cuidado con la creacion de indices ya que estos pueden optimizar o empeorar la DB
* La manera en que usamos los simbolos operacionales afeca la consulta
* Hacer buen uso del comodin "%"  en un "LIKE"
* Utilizar "EXISTS" en vez de "COUNT"
* Es mejor utilzar "palabra%" que un string del tipo "Substr(columnda,1,1)"
* Algunas bases de datos buscan mejor si hay columnas unicas y indexadas 
* Usar las funciones "MAX Y MIN" preferiblemente en conlumnas indexadas"
* Se deben utilizar los tipos de datos mas eficientes "pequeños" que sean posibles
* la columna que se utiliza para un indexado debe ser la mas corta posible.
* No es necesario indexar una cadena cuando en su lugar se pueden indexar un prefijo o sufijo
* Tratar de que la consulta retorne el menor numero de registros posibles
* En bases de datos como MYSQL o Oracle es recomendable utilizar los valores por defecto
* Nunca utilizar un subquery en un IN
* Utilizar "UNION" en vez de "OR"
 
## Que tipos de enfoques tiene el control de acceso a BD
* Control de acceso discrecional
* Control de acceso obligatorio 

## Que es el control de acceso Discrecional

Garantiza privilegios a usuarios, incluyendo la capacidad para acceder archivos de datos especificos para operar de una manera determinada

## Que es el control obligatorio
Clasifica usuarios y datos en multiples niveles de seguridad

## Que tipos de clases de seguridad existen
* Top Secret (TS)
* Secret (S)
* Confidential (C)
* Unclassified (U)

## Que son los estandares ISO/IEC, 27001, SOX, Cobit, Itil
Son estandares para la seguridad y clasificacion de los datos

## Que tipos de autenticacion existen en oracle
* Mediante Password
* Externa
* Global

## Cuales son las sentencias SQL para dar privilegios?
* Grant (otorga privilegios)
* Revoke (quita privilegios)

``` sql
GRANT SELECT ON tabla_alumnos TO byron
REVOKE ALL ON tabla_usuarios FROM byron

```
## Que son las 12 reglas de cod
Son un conjunto de reglas para determinar si un SGBD es relacional

1.  Informacion: 
* Todos los datos deben estar almacenados en tablas.
2.  Acceso garantizado: 
* Cualquier dato es accesible sabiendo el nombre de su fila y el nombre de su columna o atributo
3.  Tratamiento sistematico de los valores nulos: 
* El SGDB debe soportar valores nulos.
4.  Catálogo en línea relacional: 
* Se debe poder obtener el diccionario de datos y consultarlo con las mismas instruccioens SELECT
5.  Sublenguaje de datos completo: 
* No puede haber funciones fuera de un mismo lenguaje.
6.  Vistas actualizadas: 
* las vistas deben mostrar la infomacion actualizada.
7.  Inserciones,modificaciones y eliminaciones de alto nivel: 
* Esto implica que el lenguaje de manipulacion de datos trabaje con un conjunto de filas a la vez.
8.  Independencia Física: 
* El acceso a los elementos logicos de la DB no deben cambiar porque la DB fisica cambie.
9.  Independencia Lógica: 
* Si cambia el nombre de la tabla o la columna que modificamos esto no debe afectar el esquema externo.
10. Independencia de integridad: 
* Las reglas de integridad deben ser gestionadas y almacenadas por el SGBD.
11. Independencia de distribucion: 
* El esquema logico debe ser el mismo independientemente de si la DB es distribuida o no.
12. No subversión: 
* La DB no debe permitir que exista un lenguaje que permita saltarse las reglas anteriores.

## Que son las bases de datos distribuidas.
Este se compone por un conjunto de sitios conectados entre sí mediante algun tipo de red de comunicacion en el cual cada sitio es un un sistema de DB en si mismo y los sitios trabajan como  si todos los datos estuvieran almacenados en el sitio propio del usuario.

## Que es la fragmentacion de BD
Es la descomposicion o particion de una tabla en pedazos llamados fragmentos y esta se puede dar de dos formas:
* Fragmentacion Horizontal(Selecciona registros completos de una relacion).
* Fragmentacion Vertical(Selecciona columnas completas de una relacion).

## Transacciones distribuidas
Es aquella que involucra algún proces en distintos sitios de la red, existe un agente raiz que inicia toda la transaccion y este sitio raiz es llamado sitio de origin de la transaccion y este es el encargado de asegurar BEGIN-TRANSACTION, COMMIT O ROLLBACK de toda la transaccion distriubida

## Commit de 2 fases

Es un protocolo de las bases de datos distribuidas en el que un sitio o agente llamado cordinador es el responsable de tomar la decision de hacer un commit o un rollback global y cada participante es responsable de grabar a sus bitacoras y bases de datos globales 

## Cuales son las fases del commit
* La primera fase tiene como objetivo lograr una desicion común
* La segunda fase es llevar a cabo esta decision.
