# **Bases de Datos** 
Las bases de datos son sistemas organizados de almacenamiento de información que permiten la gestión, búsqueda y recuperación de datos de manera eficiente y estructurada. 
> Es un conjunto de datos relacionados entre si, organizados y estructurados de manera que se puedan recuperar, actualizar y gestionar fácilmente. 

Las bases de datos son usadas en una amplia variedad de aplicaciones, desde la gestión de inventarios hasta la investigación científica y gestión de recursos humanos. La mayoría de las bases de datos modernas son gestionadas por sistemas de gestión de bases de datos (DBMS) o (SGBD) que permiten a los usuarios crear, actualizar y consultar los datos de manera eficiente y segura. Existen fundamentalmente dos tipos de bases de datos: las bases de datos [relacionales](https://www.oracle.com/ar/database/what-is-a-relational-database/) y las bases de datos no relacionales o [NoSQL.](https://ayudaleyprotecciondatos.es/bases-de-datos/no-relacional/)

Para propósitos de este curso estudiaremos las bases de datos relacionales. 

## **Bases de datos relacionales:** 
Una base de datos relacional es un tipo de base de datos que almacena y proporciona acceso a puntos de datos relacionados entre si. Se basan en el modelo relacional el cual es una forma intuitiva y directa de representar datos en tablas. En una base de datos relacional, cada fila en una tabla es un registro con una ID única a la que llamaremos clave. Las columnas de la tabla contienen lños atributos de los datos y cada registro suele tener un valor para cada atributo, lo que simplifica la creación de relaciones entre los puntos de datos. 

> ### **Conceptos Fundamentales:** 
> * **Tabla:**  es un modelado de datos donde se guardan los datos recogidos por un programa. Los datos de una tabla mantienen una relación entre si. No pueden existir dos tablas con el mismo nombre o registro. Las tablas son un conjunto de campos (columnas) y registros (filas)
> * **Relaciones:** en una base de datos relacional todos los datos se almacenan y se accede a ellos por medio de relaciones previamente establecidas. Las relaciones que almacenan datos son llamadas **relaciones base** y su implementación es llamada tabla. La relación entre una tabla padre y un hijo  se lleva a cabo por medio de las llaves primarias y llaves foráneas. 
> * **Llave primaria:** es una llave única, puede estar conformada por uno o más campos de la tabla, elegida entre todas las candidatas que define unívocamente a todos los demás atributos de la tabla para especificar los datos que serán relacionados con las demás tablas. 
> * **Llave foránea:** es una referencia a una clave en otra tabla, esta determina la relación existente en dos tablas. Las llaves foráneas no necesitan ser llaves únicas en la tabla donde están y si a donde están referenciadas.

## **MySQL:**
MySQL es un sistema de gestión de bases de datos relacional desarrollado bajo una licencia dual: GPL/Licencia comercial por [Oracle Corporation](https://es.wikipedia.org/wiki/Oracle_Corporation) y está considerada como la base de datos de código abierto más popular del mundo y es una de las más poplares del mundo junto a **Oracle** y **Microsoft SQL Server**. Para acceder a las bases de datos MySQL se pueden utilizar diversos lenguajes de programación, entre ellos podemos encontrar: 
C, C++, C#, Pascal, Java, Python, Visual Basic, etc. 

Para acceder a los sistemas de  bases de datos pordemos usar los siguientes programas: 
* **phpMyAdmin**
* **MySQL Workbench**
* **DBeaver**
* **HeidiSQL**
* **LibreOffice Base**
* **Toad for MySQL**
* **Interfaz por Línea de comandos**

### **Sentencias SQL:** 
SQL o Structured Query Language es un lenguaje estandarizado para acceder y manipular las bases de datos. Para aprender SQL usaremos el siguiente [enlace](https://www.w3schools.com/sql/sql_intro.asp).

### **Creación de bases de datos:** 
Para crear una base de datos podemos usar la interfaz gráfica o la línea de comandos. Aprenderemos a crear una base de datos de ambas formas. 

Creando una base de datos por medio de la línea de comandos: 
```sql
CREATE DATABASE biblioteca;
``` 
Posteriormente seleccionamos la base de datos:
```sql
USE biblioteca;
```
Seguidamente creamos las tablas: *libro*, *autor*, *alumno*, *prestamo*, *bibliotecario*.
```sql
CREATE TABLE autor(
    idautor INT NOT NULL AUTO_INCREMENT,
    nombre VARCHAR(100) NOT NULL,
    apellidos VARCHAR(100),
    fecha_nac DATE NOT NULL,
    fecha_muerte DATE,
    pais VARCHAR(100),
    PRIMARY KEY(idautor)
);

CREATE TABLE libro (
    idlibro INT NOT NULL AUTO_INCREMENT,
    titulo VARCHAR(255) NOT NULL,
    descripcion TEXT(1000),
    idautor INT NOT NULL,
    fechapub DATE NOT NULL,
    isbn VARCHAR(13),
    PRIMARY KEY(idlibro), 
    FOREIGN KEY(idautor) REFERENCES autor(autorid)
);

CREATE TABLE bibliotecario(
    idbiblio INT NOT NULL AUTO_INCREMENT,
    apellidos VARCHAR(100),
    nombre VARCHAR(100),
    PRIMARY KEY (idbiblio)

);

CREATE TABLE alumno(
    idalumno INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    carnet VARCHAR(10) UNIQUE,
    nombres VARCHAR(100),
    apellidos VARCHAR(100)
);

CREATE TABLE prestamo(
    idprestamo INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    idalumno INT,
    idlibro INT,
    idbiblio INT,
    FOREIGN KEY(idalumno) REFERENCES alumno(idalumno),
    FOREIGN KEY(idlibro) REFERENCES libro(idlibro),
    FOREIGN KEY(idbiblio) REFERENCES bibliotecario(idbiblio)
);
```
Observe como se crean primero las tablas independientes ***autor***, ***bibliotecario***, ***alumno*** antes que las tablas que dependen de ellas como el caso de ***libro***, ***prestamo*** de esta manera, cuando el script se ejecute creará una tabla y luego la tabla con referencia a la otra, así no se encontrará con un error al crear una relación a una tabla que no existe.

Notará también que algunas palabras cambian de color al escribirlas, estas son las palabras reservadas de SQL. Las palabras reservadas en este script que requieren especial atención son las siguientes:

* **CREATE:** es una palabra reservada que permite crear, se usa para crear una base de datos, una tabla o un procedimiento almacenado o función etc. 
* **NOT NULL:** es la palabra reservada que le indica a la tabla que ese campo no debe ir vacío, es necesario usarlo en casos donde es obligatorio que haya información
* **PRIMARY KEY:** esta especifica que dicho campo es una llave primaria, generalmente va acompañado de NOT NULL y de AUTO_INCREMENT.
* **AUTO_INCREMENT:** indica que el campo es auto incrementable, funciona únicamente en los campos de tipo INT
* **FOREIGN KEY:** indica que el campo es una llave foránea, seguidamente se debe hacer referencia con **REFERENCES** a la tabla de donde viene el dato.
* **UNIQUE:** representa campos de valor único, es decir aquellos que no pueden repetirse en ningún otro registro de la base de datos





