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