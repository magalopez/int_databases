## WHERE

Es la sentencia que nos ayuda a filtrar tuplas o registros dependiendo de las características que elegimos.

+ La propiedad LIKE nos ayuda a traer registros de los cuales conocemos sólo una parte de la información.
  Un breve resumen del like y uso del %:
    - %termina_en
    - %en la cadena%
    - inicia_con%

  Ejemplo
  ~~~
  SELECT * FROM posts WHERE titulo LIKE ‘%ar%’
  ~~~
  Busca que la cadena que halla en titulo contenga ‘ar’ y no importa en que posición se encuentre, si la cadena ‘ar’ forma parte de titulo, entonces devolverá los registros que cumplan esa condicion.

+ La propiedad BETWEEN nos sirve para arrojar registros que estén en el medio de dos. Por ejemplo los registros con id entre 20 y 30.

+ Las propiedades AND y OR nos sirven para concatenar nuestras condiciones.

Cabe mencionar que los operadores LIKE y BETWEEN pueden ser negados con NOT
NOT LIKE
NOT BETWEEEN

