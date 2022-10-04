### GROUP BY

La sentencia group by te permite contar la cantidad de veces que se repite un valor buscado por el grupo seleccionado. Comunmente se utiliza con el contador de filas, el cual es de la forma 
~~~
SELECT COUNT(*) FROM TABLE;
~~~

Podemos combinar ambas sentencias ~~~ GROUP BY COUNT(*) ~~~ para crear una consulta especial. 

Ejemplo: Queremos saber cuantos post se escriben por mes.

~~~
 **SELECT** MONTHNAME(fecha_publicacion) AS MONTH_POST **COUNT**(*) AS POST_CUANTITY **FROM** POST **GROUP BY** MONTH_POST;
~~~

- El orden inicial en una tabla es acorde a como fueron creados los datos.
- El default de la sentencia ORDER BY es ascendente.
- LIMIT es un complemento al ORDER BY y funciona similar a un filtro.
- Cuando se desea hacer una selección de rows, se hace con WHERE, pero cuando se desea hacer una selección de rows agrupados debe hacerse con HAVING.
- El orden de ejecución de los comandos es importante. Ejemplo: HAVING va después de GROUP BY, no puede ir después de ORDER BY porque lanza error de syntaxis.

~~~
SELECT MONTHNAME(fecha_publicacion) AS post_month, estatus, COUNT(*) AS post_quantity
FROM posts
GROUP BY estatus, post_month
HAVING post_quantity > 1
ORDER BY post_month;
~~~
