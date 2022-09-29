# Normalización

[Fundamentos de la normalización de bases de datos](https://learn.microsoft.com/es-mx/office/troubleshoot/access/database-normalization-description)


La normalización como su nombre lo indica nos ayuda a dejar todo de una forma normal. Esto obedece a las 12 reglas de Codd y nos permiten separar componentes en la base de datos:

Ejemplo Sin Normalizar
  ![SN](assets/SN.png)

  - Primera forma normal (1FN): Atributos atómicos (Sin campos repetidos)
  ![1FN](assets/FN1.png)

  - Segunda forma normal (2FN): Cumple 1FN y cada campo de la tabla debe depender de una clave única.
  ![2FN](assets/FN2.png)

  - Tercera forma normal (3FN): Cumple 1FN y 2FN y los campos que NO son clave, NO deben tener dependencias.
  ![3FN](assets/FN3.png)

  - Cuarta forma normal (4FN): Cumple 1FN, 2FN, 3FN y los campos multivaluados se identifican por una clave única.
  ![4FN](assets/FN4.png)


A términos prácticos la normalización consiste en ir descomponiendo tu tabla en pequeñas tablas que hacen referencia a ciertas entidades que se empiezan a relacionar con otras, y acabamos relacionándolas por medio de su id, así las referenciamos, y esto trae muchas ventajas, de entre ellas, podemos cambiar un dato en un solo lugar y esto se propagará a todos los lugares a donde este apunte.
