## El interminable agujero de conejo (Nested queries)

Los Nested queries significan que dentro de un query podemos hacer otro query. Esto sirve para hacer join de tablas, estando una en memoria. También teniendo un query como condicional del otro.

Este proceso puede ser tan profundo como quieras, teniendo infinitos queries anidados.
Se le conoce como un producto cartesiano ya que se multiplican todos los registros de una tabla con todos los del nuevo query. Esto provoca que el query sea difícil de procesar por lo pesado que puede resultar.

~~~
select * from post where post.fecha_publicacion = (
    select max(post.fecha_publicacion) from post
);

select new_table_projection.date, COUNT(*) AS post_count from (
    select date(min(post.fecha_publicacion)) AS date, year(post.fecha_publicacion) AS post_year
    from post
    group by post_year) AS new_table_projection
    group by new_table_projection.date
    order by new_table_projection.date;
~~~