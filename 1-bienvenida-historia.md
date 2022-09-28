# Bienvenida conceptos básicos y contexto histórico de las Bases de Datos

**Profesor Israel Vasquez** Sr. Web Developer y Data engineering enthusiast y organizer del GDG Cloud Mexico.

### Historia de la persistencia de la información

Hubieron grandes momentos en la historia en la que los humanos sintieron la necesidad de almacenar información más alla 

El almacenamiento en la nube tiene grandes ventajas comparadas con los otros métodos de almacenamiento, puesto que es accesible desde cualquier parte del mundo. Además, es centralizada y puede ser usada por varias personas al mismo tiempo.

### ¿Que *$%/)$ son las Bases de Datos?

Las bases de datos entran cuando hacemos la transición a medios digitales.

#### Se han divido historicamente en dos grandes grupos:

**Relacionales:** En la industria hay varias compañias dedicadas a ser manejadoras de bases de datos relacionales como SQL Server, Oracle, MariaDB, entre otras.

**No relacionales:** Todavia estan avanzando y existen ejemplos muy distintos como cassandra, elasticsearch, neo4j, MongoDB, Firestore, entre otras.

#### Servicios

**Auto administrados:** Es la base de datos que instalas tú y te encargas de actualizaciones, mantenimiento, etc.

**Administradas:** Servicios que ofrecen las nubes modernas como Azure y no debes preocuparte por el mantenimiento o actualizaciones.


### RDB (Base de datos relacionales)

Las bases de datos surgen de la necesidad de conservar la informacion más allá de lo que existe en la memoria RAM.

Las bases de datos basadas en archivos eran datos guardados en texto plano, fáciles de guardar pero muy dificiles de consultar y por la necesidad de mejorar esto nacen las bases de datos relacionales. 

Su inventor Edgar Codd escribio 12 reglas o mandamientos para asegurarse de que toda la filosofia detras de las bases de datos no se perdiera, estandarizando el proceso. 

#### Entidades y Atributos

En base de datos una entidad es la representación de un objeto o concepto del mundo real que se describe en una base de datos. Las entidades se describen en la estructura de la base de datos empleando un modelo de datos. 

### ¿Que es una entidad?

- Es la representacion de un objeto real o abstracto que existe en algun realidad. 
- Tienen propiedades o caracteristicas que deseamos almacenar en una Base de datos.
- Toda entidad debe ser nombrada en singular.
- Cada elemento de una entidad se conoce como **Instancia**.
- Todas las instancias deberian tener los mismos atributos

Para considerar un objeto como entidad este tiene que tener varias instancias y varios atributos. 

### ¿Que es un atributo?

Son las características o propiedades que describen a la entidad (se encierra en un óvalo). Los atributos se componen de:

Los **atributos compuestos** son aquellos que tienen atributos ellos mismos.

Los **atributos llave** son aquellos que identifican a la entidad y no pueden ser repetidos. Existen:

  - Naturales: son inherentes al objeto como el número de serie.
  - Clave artificial: no es inherente al objeto y se asigna de manera arbitraria.


### Tipos de entidades

Existen dos tipos de Entidades, las fuertes y débiles. 

**Entidades fuertes:** son entidades que pueden sobrevivir por sí solas.

**Entidades débiles:** no pueden existir sin una entidad fuerte y se representan con un cuadrado con doble línea.
    - Identidades débiles por identidad: no se diferencian entre sí más que por la clave de su identidad fuerte.
    - Identidades débiles por existencia: se les asigna una clave propia.


### Cómo representar las entidades en bases de datos

Existen varios tipos de notaciones para los modelos entidad relacionamiento. Chen es uno de los más utilizados para diagramar lógicamente la base de datos.

![Chen's Notation](https://static.platzi.com/media/user_upload/ejemplo-notacion-chen-entidades-98a3fc2d-c6c0-4012-9e0e-c51edc2acc40.jpg)