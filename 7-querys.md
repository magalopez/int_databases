## QUERYS

Las consultas o queries a una base de datos son una parte fundamental ya que esto podría salvar un negocio o empresa.
Alrededor de las consultas a las bases de datos se han creado varias especialidades como ETL o transformación de datos, business intelligence e incluso machine learning.

### ETL
La palabra ETL correspondería al acrónimo de:
**Extract** (Extraer)
**Transform** (Transformar)
**Load** (Cargar)
**ETL** hace parte del proceso de integración de datos, mas aun es un componente muy importante que completa el resultado final en la relación de aplicaciones y sistemas.

### Estructura básica de un Query

Los queries son la forma en la que estructuramos las preguntas que se harán a la base de datos. Transforma preguntas en sintaxis.

El query tiene básicamente 2 partes: **SELECT** y **FROM** y puede aparecer una tercera como **WHERE**.

La estrellita o asterisco (*) quiere decir que vamos a seleccionar todo sin filtrar campos.

~~~
SELECT city, count(*) AS total
FROM people
WHERE active = true
GROUP BY city
ORDER BY total DESC
HAVING total >= 2;
~~~

## Lista de querys utilizadas

~~~~
-- SELECT titulo AS encabezado, fecha_publicacion AS publicado_en, status AS estado FROM post WHERE status = 'inactivo';

-- SELECT COUNT(*) AS numero_post FROM post;

CREATE TABLE user (
    id int not null auto_increment,
    name varchar(50) not null,
    edad int not null,
    email varchar(50) not null,
    primary key (id)
);

INSERT INTO user (name, edad, email) VALUES ('Nala', 2, 'nala@gmail.com');
INSERT INTO user (name, edad, email) VALUES ('Nadia', 32, 'nadia@gmail.com');
INSERT INTO user (name, edad, email) VALUES ('Maga', 27, 'maga@gmail.com');
INSERT INTO user (name, edad, email) VALUES ('Dan', 35, 'dan@gmail.com');


select * from user where edad > 30;

-- update user set name = 'gabriel' where id = 4;

select * from user where edad > 20 and email = 'maga@gmail.com';

select * from user where edad > 20 and edad < 30 or email != 'nala@gmail.com';

select * from user where edad between 2 and 10;

select * from user where email like '%gmail%';

select * from user where email like 'nala%';

select * from user order by edad asc;
select * from user order by edad desc;

select max(edad) as mayor from user;
select min(edad) as menor from user;

select id as identificador, name as nombre from user;


create table product (
    id int not null auto_increment,
    name varchar(50) not null,
    created_by int not null,
    marca varchar(50) not null,
    primary key (id),
    foreign key (created_by) references user(id)
);

rename table products to product;

insert into product (name, created_by, marca)
values
    ('iPad', 1, 'apple'),
    ('iPhone', 1, 'apple'),
    ('iWatch', 2, 'apple'),
    ('macbook', 1, 'apple'),
    ('iMac', 3, 'apple'),
    ('iPad mini', 2, 'apple');

select * from product;

select u.id, u.email, p.name from user u left join product p on u.id = p.created_by;

select u.id, u.email, p.name from user u right join product p on u.id = p.created_by;

select u.id, u.email, p.name from user u inner join product p on u.id = p.created_by;

select u.id, u.email, p.id, p.name from user u cross join product p;
~~~

