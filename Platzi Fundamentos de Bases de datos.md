## 1. Introducción al Curso de Bases de Datos

* Relacional
* No Relacional

Bases de datos son fundamentales
* Transforman el uso de datos
* Evolucionan en Big Data o Analitica
* Apoyando Procesos de Negocio, Procesos de Innovación, como puedo ser mucho más eficiente a la hora de crear una StartUp, a la hora de crear un sistema de información productivo y críti## co.

Diferentes tipos de tecnologías:

* Bases de datos empresarial
* Open Source
* Datos en la nube

Otros tipos de bases de datos:

* Bases de datos basados en grafos
* Bases de datos basados en cartografía
* Bases de datos basados en geografía

Estas anteriores funcionan bien a la hora de aplicarlas a un eCommerce, se usan al buscar relaciones entre los objetos a vender y las preferencias del usuario, son unas de muchas formas de implementar.

Teoría del diseño y Modelado Relacional, 
* 9 diferente pasos para fundamentar el proceso de creación o diseño de la base de datos, nos ayudará a ahorrar mucho tiempo

Diseño inicial de bases de datos no relacionales

Diferencias entre Datos Relacionales y No Relacionales, al ser que se diseña diferente para una que la otra.

Estándar de programación o lenguaje que utilizan las bases de datos Relacionales, el Estándar SQL, operaciones básicas de modelado de bases de datos y operaciones para obtener resultados.


## 2. Propósito general de las Bases de Datos 

### ¿Qué es una base de datos?

Una base de datos es un conjunto de datos ordenados que están relacionados entre sí y almacenados sistemáticamente para su posterior uso. Las bases de datos permite el almacenamiento de grandes cantidades de datos de forma organizada.

### Historia de las Bases de Datos

1950-1960: Maquinas tabuladoras, tarjetas perforadas y cintas magnéticas.

1960-1979: Modelos jerárquicos, discos duros, modelo de data relacional, transacciones en tiempo real.

Un disco duro tiene información persistente, o sea que perdura en el tiempo.

1970-1980: SQL, Sistemas SQL comerciales, bases de datos paralelas y distribuidas, bases de datos orientadas a objetos.

SQL es un estándar, la mayoría de los comandos básicos, en cualquier tipo de datos que sea SQL deben funcionar (MariaDB, MySQL, etc).

1980-1990: Data mining, data warehouse, e-commerce.

2000-Actualidad: XML, administración automatizada, analytics, big data, No SQL, InMemory, Scale Out, Systems of Engagement.
Historia de las Bases de Datos (va a venir en el examen …creo)

* 1950-1960: Maquinas tabuladoras, tarjetas perforadas y cintas magnéticas.

* 1960-1979: Modelos jerárquicos, discos duros, modelo de data relacional, transacciones en tiempo real.

Un disco duro tiene información persistente, o sea que perdura en el tiempo.

* 1970-1980: SQL, Sistemas SQL comerciales, bases de datos paralelas y distribuidas, bases de datos orientadas a objetos.

* SQL es un estándar, la mayoría de los comandos básicos, en cualquier tipo de datos que sea SQL deben funcionar (MariaDB, MySQL, etc).

* 1980-1990: Data mining, data warehouse, e-commerce.

* 2000-Actualidad: XML, administración automatizada, analytics, big data, No SQL, InMemory, Scale Out, Systems of Engagement.

DBMS: Data Base Management System 
SGDB: Sistemas de Gestion de Bases de Datos

Estrategia y Plataforma tecnologica con ciertas herramientas para persistir la data en el tiempo y sacar informacion de ella

## 3. Tipos de Bases de Datos y sus aplicaciones en la industria

* Bases de datos relacionales: Este tipo de base de datos se diferencia porque trabaja con un conjunto de tablas y se manipula de acuerdo con el modelo de datos relacional.

* Bases de datos no relacionales: En este tipo de base de datos aunque todas se denominan NoSQL, en realidad hay diferentes tipos:

  – Bases de datos “Clave” – “Valor”: Es el modelo de NoSQL más popular y sencilla en cuanto a funcionalidad.

  – Bases de datos “Documentales”: Este tipo es el más versátil ya que guarda información como un documento generalmente de tipo JSON o XML.

  – Bases de datos “En grafo”: La información representada en este tipo de bases de datos se realiza en forma de nodos de un grafo y sus relaciones con las aristas del mismo.

  – Bases de datos “Orientadas a Objetos”: En este tipo de bases de datos la información se representa mediante objetos de igual forma que lo hacen los lenguajes de programación orientados a objetos.

### Tipos de Bases de Datos:

* MariaDB: Es una distribución de base de datos que deriva de Mysql.

* Neo4j: Base de datos basada en nodos (centrada en grafos).

* MongoDB: Base de datos NoSQL. Trabaja en varias instancias (Divide y vencerás).

### Aplicaciones de Bases de Datos:

* Hacer reservaciones, las cuales no redundan (repetir) en data (Aerolineas).
* Tomar desiciones basados en un comportamiento histórico (Escuelas).
* Realizar transacciones internas y externas (Bancos).
* Registros distribuidos, usando bases de datos como fundamento (blockchain).
* Registro de inventarios, compra, venta y relación con sus usuarios y clientes (Tiendas de Retail)
* Inventario y Registro de producción (Manufactura)
* Historial de empleados (Recursos Humanos)

Una base de datos no necesariamente puede ser un sistema unificado, también puede ser un sistema que se encuentre dentro de una sola infraestructura (o arquitectura) con instancias separadas.


## 4. Visión general de los datos

### Que es un Dato? 

Un dato como tal es algo que me permite describir un objeto. un dato es una caracteristica de un objeto. color, altura, etc…
y la informacion es como mostramos los datos .

### Niveles de Abstraccion

* Conceptual: Definimos los conceptos de que vamos a diseñar/modelar. Iniciamos a usar los objetos de entidades y relaciones.

* Lógico: En el diagrama logico resolveremos dudas de consistencias que pudieron quedar del nivel conceptual.

* Físico: Como lo va a ver la base de datos. Este es el paso previo a pasar el modelo a lenguaje SQL.

Entidad : objeto con caracteristicas

Una entidad es una abstracción del mundo real, por ejemplo una casa y va a tener ventanas, puertas, habitaciones etc, además van a existir otras entidades, por ejemplo en una casa viven personas, éstas serían una segunda entidad.

Relacion: Es la relacion que existe entre las entidades…

## 5. Tipos de Datos

### Tipos de Datos en BD: 
 
 * caracter, 
 * numerico, 
 * varchar (caractares mas variables), 
 * imagen, 
 * fecha, 
 * moneda, 
 * texto, 
 * bit (1 y 0, verdadero y falso), 
 * decimal (miligramos, unidades flotante)

La mayoría de estos tipos de datos se basan en el stándar SQL92, los cuales son aplicables a todas las bases de datos.

* Esquemas: Estructura logica que va a tener mi base de Datos
* Instancias: Contenido de particulas que tiene mi BD en un instabte de tiempo

* DML es para manipular los datos en las instancias (las operaciones básicas que hacemos en un CRUD) 
* DDL es el código para definir, crear o modificar la estructura o el esquema de la base de datos con sus tablas y campos.

Ambos son tipos de declaraciones de SQL, pero son cuatro en total, además están 

* DCL (Data Control Language) para manejar permisos y control de acceso a los datos por parte de los usuarios 
* TCL (Transaction Control Language) para manejar la integridad de las transacciones.

* Hadoop Distributed File System (HDFS): 

Es un sistema de archivos distribuido, escalable y portátil escrito en Java para el framework Hadoop. El HDFS almacena archivos grandes (el tamaño ideal de archivo es de 64 MB9​), a través de múltiples máquinas. Consigue fiabilidad mediante replicado de datos a través de múltiples hosts, y no requiere almacenamiento RAID en ellos.

* General Parallel File System (GPFS): 

Es un sistema de ficheros distribuido de alto rendimiento desarrollado por IBM. GPFS proporciona un acceso concurrente de alta velocidad a aplicaciones que se encuentran ejecutando en múltiples nodos de un cluster dando una visión de un disco compartido entre todos ellos.

Otros tipos de BD: XML, No SQL, In Memory

#### CHAR

Se utiliza para almacenar el valor de cadena de caracteres de longitud fija.
El número máximo de caracteres que el tipo de datos puede contener es de 255 caracteres.
Es un 50% más rápido que VARCHAR.
Utiliza la asignación de memoria estática.

#### VARCHAR

Se utiliza para almacenar datos alfanuméricos de longitud variable.
El máximo que este tipo de datos puede soportar es hasta 65,535± caracteres compartidos para la fila.
Es más lento que CHAR.
Utiliza la asignación de memoria dinámica.


## 6. Diferentes tipos de Bases de Datos


### Bases de datos SQL

* La indexación funciona como un indice de un libro o de un temario, nos dice donde encontramos un tema y en que pagina.
* La indexación en SQL se hace por medio de una estructura de arbol, esta nos permite hacer busquedas.
* Existe el problema que cuando se buscan tipos de datos que no estan necesariamente estructurados en una estructura de datos se busca desde el primer dato hasta el ultimo.

Ejemplos; PostgreSQL, MariaDB.

### Bases de Datos No SQL

* La indexación funciona con objetos JSON, no necesariamente funciona como un arbol, se pueden hacer indices dividiendo los objetos por sus caracteristica y particularidades.
Ejemplos; MongoDB, Cassandra.

### Bases de datos Analíticas y de Bigdata

* Ejemplos; Hadoop, Hortonworks, Spark

### Bases de datos basadas en aceleración

Son bases de datos muy rápidas que sin embargo no tienen persistencia.

Ejemplos; Redis, neo4j, Kinetica.

### Formas de usos en las bases de datos:

* On premise open source, bases de datos de formato empresarial u opensource instalada en nuestra maquina sin una gran infraestructura.

* Licenciamiento por cores o sockets, se paga dependiendo de ciertas características; como el hardware en el que va a correr.

* Licenciamiento modular, se paga por funcionalidades o modulos para necesidades diferentes.

* Pago por uso a través de SAAS(Software As A Service) o PAAS (Platform As A Service). Es como adquirir una renta y pagar por usar una base de datos.

* Suscripción de nodos de computo, funciona para plataformas como Hadoop el cual no es centralizado y trabaja de forma distribuida, se paga por nodo utilizado.


## 7. Reto ¿Hadoop y Blockchain podrían cambiar una Base de Datos tradicional?
## 8. ¿Qué es una Entidad?

¿Qué es una entidad?

Una entidad es la representación de un objeto o concepto del mundo real. En las bases de datos se emplea un modelo de datos para describir la estructura de la base de datos

Barker = Aquí una entidad se representa como una caja, es una caja que va a tener atributos. Estos atributos van a poder ser obligatorios u opcionales.

## 9. ¿Qué es una Relación?

Para definir una Relación tenemos que tener en cuenta los siguientes puntos:

La obligatoriedad. Ésta se denota con una línea continua.
Opcional. Se representa con una línea punteada.
Datos importantes:

El símbolo con el que representamos la característica “de uno a muchos” es con la llamada pata de gallo, que gráficamente es una línea continua con dos líneas en 45 grados en cada lado.


0 - 1 ----------- (cero a uno: es obligatorio pero solo se puede tener uno)
1 - 1 ___________ (uno a uno: es obligatorio y solo se puede tener uno)
0 - M ----------≡ (cero a muchos: no es obligatorio y se puede tener muchos)
1 - M __________≡ (uno a muchos: es obligatorio y se puede tener muchos)
M - M ≡---------≡ (muchos a muchos: no es obligatorio y se puede tener muchos)


## 10. Características o datos de una Entidad

Los atributos de una entidad son las características que lo identifican o lo definen.


Entidad Fuerte: La constituyen las tablas principales de la BD, que contienen los registros principales del sistema de información y que requieren de entidades o tablasauxiliares para completar su descripción o información.

Entidad Debil: Tablas auxiliares de una tabla principal a la que completan o complementan con la información de sus registros relacionados.

## 11. ¿Ya aparecieron las llaves?

Las llaves nos dan acceso a los datos de una entidad, su notación es
la de numeral #.

Las llaves tienen que ser irrepetibles y obligatorias, por lo tanto el ID puede ser una llave.

Una llave puede ser compuesta, esta se compone de 2 numeros, entre ID y Numero de seguro social. (Como un numero de teléfono móvil).

Las llaves foráneas son llaves que van a estar en nuestra tabla, que no necesariamente son nuestras llaves primarias pero van a permitir acceder a otra tabla donde ahí sean llaves primarias.

Una llave foranea tiene que ser llave primaria de una tabla (entidad).

Las llaves son fundamentales por que son obligatoriamente índices, los cuales permiten encontrar los datos cuando se necesitan de una forma rápida y ordenada.

Tupla/registro/fila: representa un objeto único de datos implícitamente estructurados en una tabla.


## 12. Índices e Indexación

El uso de indices tiene como ventaja:

* Permite ordenar las tablas por varios criterios simultaneamente.
* El coste de insercion y eliminacion es menor.
* Con los registros ordenados se utilizaran algoritmos muchos mas eficientes.

RowID

Representa una dirección de la base de datos, ocupada por una única fila. 
El ROWID de una fila es un identificador único para una fila dentro de una base de datos. No hay dos filas con el mismo ROWID. 

Este tipo de dato sirve para guardar punteros a filas concretas. El ROWID se compone de:

-Número de datafile donde se almacena la fila
-Dirección del bloque donde está la fila
-Posición dentro del bloque

Siempre que queramos obtener una fila de la forma más rápida posible, debemos hacerlo a través de su ROWID. Un uso típico suele ser obtener un listado de ROWIDs con un SELECT, y después acceder a cada una de las filas directamente con la condición del ROWID.

* Las llaves primarias obligatoriamente van a ser índices.
* Las Bases de Datos indexan con un algoritmo llamado:Árboles B+
* Los Árboles B+ son una estructura que va a tener un tronco, tres raíces, de las cuales se van a ir derivando tres raíces más por cada una, hasta donde sea necesario.
* Por defecto todas las Bases de Datos están indexadas, así no le pongamos índices. Lo que sucede es que la Base de Datos siempre obliga a indexar porque siempre tienen un atributo que está oculto, este atributo es RowID.


## 13. Constrains o Restricciones

### Ejemplos de restricciones:

* Validación si una persona tiene cierta edad (> 18 años)
* El campo no puede estar vacío Not Null
* El campo no se puede repetir Unique
* Validación por comparación Check (==, >=, <=, > ,<)


Las restricciones desde la base de datos nos pueden recordar que no podemos ingresar un dato u omitirlo sin importar que no lo hayamos restringido en la capa de aplicación, es como una segunda capa de seguridad.

### Primary key vs Unique

#### Cosas en comun

* Una clave primaria implica un índice único.

#### Cosas que son diferentes

* Sólo puede haber una clave primaria, pero puede haber múltiples índices únicos.
* Una clave primaria implica también NOT NULL, pero un índice único puede ser nulo.

## 14. Capas de abstracción del modelo Entidad-Relación

### Capa Conceptual 

* En esta capa vamos a tener varias entidades, aún sin nombre definido. 
* Las entidades van a tener cada una sus llaves primarias y sus atributos, además van a tener relaciones.
* Para que existan las relaciones “muchos a muchos” se necesitan llaves foráneas en las entidades.

### Capa Lógica 

* El modelo Entidad-Relación para poder procesar las relaciones “muchos a muchos” las va a partir en entidades que se llaman: Entidades Débiles.

### Capa Física

* Este modelo va a ser el paso del modelo lógico hacia la representación que ya va a tener la Base de Datos. 
* En esta capa, ya cada uno de los datos empieza a entrar en las clasificaciones según su tipo de dato.

Cuando tenemos una relacion 1-M (E1 a E2) va a provocar que en la entidad con pata de gallo, E2, tenga una FK de #E1. Para que existan las relaciones “muchos a muchos” se necesitan llaves foráneas en las entidades.

En la Capa de Abstraccion Fisica: Una relacion de 1-M la convertimos a flecha. Algunos ponen nombres a estas relaciones por ej, tenemos una fk de E2: FK_E2.

En fin, estas capas las convertiremos en codigo SQL, y no seran tablas sino que seria un INSERT TABLE (E1 con los atributos correspondientes, acordes al tipo de datos al de BD).

(Paso 1) Identificar Cuáles son las Entidades Resuelven Nuestro Problema
(Paso 2) Identificación de las Relaciones de las Entidades.
(Paso 3) Entidades y Relaciones
(Paso 4) Asignar Atributos a las Entidades.
(Paso 5) Generar un diagrama conceptual
(Paso 6) Modelo lógico
(Paso 7) Identificar nuevos atributos que generan nuestras entidades 
(Paso 8) Construir el Diagrama del Modelo Físico
(Paso 9) Pasar al estándar de la base de datos (SQL)

## 15. Metodología básica de 9 pasos con Barker (Paso 1) Identificar Cuáles son las Entidades Resuelven Nuestro Problema
## 16. Metodología básica de 9 pasos con Barker (Paso 2): Identificación de las Relaciones de las Entidades.
## 17. Metodología básica de 9 pasos con Barker (Paso 3): Entidades y Relaciones
## 18. Metodología de Diseño (Correcciónes del paso 2 y 3)
## 19. Metodología de Diseño (Paso 4): Asignar Atributos a las Entidades.
## 20. Metodología de Diseño (Solución del paso 4): Terminando de Aseignar Atributos a las Entidades
## 21. Metodología de Diseño (Pasos 5, 6 y 7)  5. Generar un diagrama conceptual,  6. Modelo lógico,  7. Identificar nuevos atributos que generan nuestras entidades débil## es.
## 22. Metodología de Diseño (Paso 8): Construir el Diagrama del Modelo Físico
## 23. Metodología de Diseño (Paso 9): Pasar al estándar de la base de datos (SQL)
## 24. Reto con el paso 4 de la Metodología de Diseño
## 25. Atomicidad y consistencia

Atomicidad: Asegura que yo tenga un conjunto de pasos para llegar a ser una transacción exitosa.

Consistencia: Aseguro que tengo un estado válido y pasó a otro estado que sigue siendo válido.

Rollback: Operación que devuelve a la base a algún estado previo (deshaciendo cambios), asegurando así la atomícidad en una transacción.

Commit: Operación que consigna un conjunto de cambios de forma permanente, transacción efectiva (correcta) y finalizada.

## 26. Aislamiento y durabilidad

Aislamiento: Esta propiedad asegura que una operación no puede afectar a otras. Esto asegura que la realización de dos transacciones sobre la misma información sean independientes y no generen ningún tipo de error. Esta propiedad define cómo y cuándo los cambios producidos por una operación se hacen visibles para las demás operaciones concurrentes. El aislamiento puede alcanzarse en distintos niveles, siendo el parámetro esencial a la hora de seleccionar SGBDs.

Durabilidad: (Persistencia). Esta propiedad asegura que una vez realizada la operación, ésta persistirá y no se podrá deshacer aunque falle el sistema y que de esta forma los datos sobrevivan de alguna manera.

## 27. Bases de Datos In-Memory (Cambio de árboles a columnar)

Las bases de datos tradicionales (basada en arboles) hacen una búsqueda por cada uno de los datos de la tabla hasta llegar al resultado.

En las bases de datos In-Memory (columnares), el esquema de búsquedas seleccionan una columna (por ejemplo Identificador) recorriendola hasta llegar al resultado, dando un mejor rendimiento.


## 28. Otros tipos de Bases de Datos en la industria

Una base de datos orientada a grafos representa la información como nodos de un grafo y sus relaciones con las aristas del mismo, de manera que se pueda usar teoría de grafos para recorrer la base de datos ya que esta puede describir atributos de los nodos (entidades) y las aristas (relaciones).

Las Bases de datos por grafos, mas comunmente usadas para predicciones y correlaciones, por las relaciones que se dan entre entidades.

## 29. Bases de Datos In-Memory con indexación de columnar
## 30. Definiendo el Proyecto y Generando Entidades de PlatziStore: Pasos 1 y 2
## 31. Definir la Estructura de la Tabla Cliente del Proyecto: Pasos 3 y 4
## 32. Terminando de Estructurar Nuestras Tablas (Continuación del paso 4)
## 33. Metodología de Diseño (Paso 5): Diagrama Conceptual
## 34. Metodología de Diseño (Paso 6 y 7): Modelo Lógico y Entidades Débiles 
## 35. Solución de atributos de entidad del proyecto - Atributos adicionales a entidad débil creada
## 36. Metodología de Diseño (Paso 8)
## 37. Llevando nuestro proyecto a SQL (Paso 9)
## 38. Terminando la Implementación del Proyecto (Paso 9)
## 39. Dependencias funcionales
## 40. Normalización, llevando el proyecto hasta tercera forma normal (primera forma normal)
## 41. Normalización, llevando mi proyecto hasta tercera forma normal (segunda forma normal)
## 42. Normalización, llevando mi proyecto hasta tercera forma normal (Cuarta y quinta forma normal)
## 43. Comenzando con SQL
## 44. DDL: Data Definition Language y DML: Data Manipulation Languaje
## 45. ACID desde lo no relacional
## 46. CAP
## 47. Scale Out y Scale Up
## 48. ¿Scale out o Scale up?
## 49. DBMS en nube para poder iniciar una aplicación propia
## 50. Estructura básica de un Query 
## 51. Aprendiendo a Hacer más Querys
## 52. Estructura básica del Query con más de una tabla
## 53. Estructura básica del Query con más de una tabla 2
## 54. Tuplas y más tuplas
## 55. Insertar registros
## 56. Joins
## 57. Noo SQL Aplicado, Planteando el Problema
## 58. Aplicando NoSQL: Colecciones y Shards
## 59. Aplicando noSQL: Integración de Comunicaciones y Hardware en una Base de Datos Scale OUT
## 60. Aplicando noSQL: Integrando JSON a Bases de Datos No Relacionales
## 61. Conclusiones del curso


