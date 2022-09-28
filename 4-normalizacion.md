# Normalización

La normalización como su nombre lo indica nos ayuda a dejar todo de una forma normal. Esto obedece a las 12 reglas de Codd y nos permiten separar componentes en la base de datos:

Ejemplo Sin Normalizar
  ![assets/SN.png](SN)

  - Primera forma normal (1FN): Atributos atómicos (Sin campos repetidos)
  ![assets/FN1.png](1FN)

  - Segunda forma normal (2FN): Cumple 1FN y cada campo de la tabla debe depender de una clave única.
  ![assets/FN2.png](2FN)

  - Tercera forma normal (3FN): Cumple 1FN y 2FN y los campos que NO son clave, NO deben tener dependencias.
  ![assets/FN3.png](3FN)

  - Cuarta forma normal (4FN): Cumple 1FN, 2FN, 3FN y los campos multivaluados se identifican por una clave única.
  ![assets/FN4.png](4FN)
