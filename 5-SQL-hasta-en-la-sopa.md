## SQL Hasta en la sopa

**SQL** significa **S**tructured **Q**uery **L**anguage y tiene una estructura clara y fija. Su objetivo es hacer un solo lenguaje para consultar cualquier manejador de bases de datos volviéndose un gran estándar.

Ahora existe el **NOSQL** o **N**ot **O**nly **S**tructured **Q**uery **L**anguage que significa que no sólo se utiliza SQLen las bases de datos no relacionales.

## SQL tiene dos grandes sublenguajes:


### DDL

DDL o Data Definition Language que nos ayuda a crear la estructura de una base de datos. Existen 3 grandes comandos:

  * Create: Nos ayuda a crear bases de datos, tablas, vistas, índices, etc.
  * Alter: Ayuda a alterar o modificar entidades.
  * Drop: Nos ayuda a borrar. Hay que tener cuidado al utilizarlo.

**3 objetos que manipularemos con el lenguaje DDL:**

  * Database o bases de datos
  * Table o tablas. Son la traducción a SQL de las entidades
  * View o vistas: Se ofrece la proyección de los datos de la base de datos de forma entendible.


~~~
CREATE DATABASE platziblog;
USE platziblog;

CREATE TABLE platziblog.people

INSERT INTO platziblog.people ( last_name, first_name, address, city)
VALUES ( 'Peredo', 'Eduardo', 'San puta 123', 'Callao'),
       ( 'Bruno', 'Marico', 'San Pedro 684', 'Callao')


ALTER TABLE platziblog.people
CHANGE COLUMN date_of_birth date_of_birth VARCHAR(30) NULL DEFAULT NULL;


ALTER TABLE platziblog.people
DROP COLUMN date_of_birth;
~~~