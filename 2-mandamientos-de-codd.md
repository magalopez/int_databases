# Las 12 reglas de Codd del Modelo Relacional

### 1. REGLA DE LA INFORMACIÓN

Toda la información en una base de datos relacionales se muestra explícitamente en el nivel lógico mediante tablas y solo mediante tablas.

Por tanto, los metadatos (diccionario, catálogo) se representan y manipulan exactamente igual que los datos de usuario, usando quizás el mismo lenguaje (ejemplo SQL).

### 2. REGLA DEL ACCESO GARANTIZADO

Para todos y cada uno de los datos (valores atómicos) de una base de datos relacional se garantiza que son accesibles a nivel lógico utilizando una combinación de nombre de tablar, valor de clave primaria y nombre de columna.

Cualquier dato almacenado en una base de datos relacionales tiene que poder ser direccionado unívocamente. Para ello hay que indicar en qué tabla está, cuál es la columna y cuál es la final primaria.

### 3. TRATAMIENTO SISTEMÁTICO DE VALORES NULOS

Se debe disponer de valores nulos (distintos de la cadena vacía, blancos, 0, etc.) para representar información desconocida o no aplicable de manera sistemática, independientemente del tipo de datos.

Se reconoce la necesidad de la existencia del valor nulo, el cual puede servir para representar, o bien, una información desconocida (ejemplo, no se sabe la dirección de un empleado)

### 4. CATÁLOGO DINÁMICO EN LÍNEA BASADO EN EL MODELO RELACIONAL

La descripción de la base de datos se representa a nivel lógico de la misma manera que los datos normales, de modo que los usuarios autorizados pueden aplicar el mismo lenguaje relacional a su consulta, igual que lo aplican a los datos normales.

Los metadatos se almacenan y se manejan usando el modelo relacional, con todas las consecuencias.

### 5. REGLA DEL SUB-LENGUAJE DE DATOS COMPLETO

Un sistema relacional debe soportar varios lenguaje y varios modos de uso de terminal (ejemplo: rellenar formularios, etc.) Sin embargo, debe existir al menos un lenguaje cuyas sentencias sean expresables, mediante una sintaxis bien definida, como cadenas de caracteres y que sea completo, soportando:

Además, debe tener una interfaz de usuario para hacer consultas, etc. Siempre debe haber una manera de hacerlo todo de manera textual, que es tanto como decir que puede ser incorporado en un programa tradicional. Un lenguaje que cumple esto en gran medida es SQL.

### 6. REGLA DE ACTUALIZACIÖN DE VISTAS

Todas las vistas que son teóricamente actualizables se pueden actualizar también por el sistema.

  - El problema está determinando en las vistas teóricamente actualizables, ya que no está muy claro.
  - Cada sistema puede hacer las suposiciones particulares sobre las vistas que son actualizables.

### 7. INSERT, UPDATE Y DELETE DE ALTO NIVEL

La capacidad de manejar una relación base o derivada como un solo operando se aplica no sólo a la recuperación de los datos (consultas), sino también a la inserción, actualización y borrado de datos.

Esto es, el lenguaje de manejo de datos también debe ser de alto nivel. Algunos sistemas de la cuenta se modifican en las filas de una tabla de una vez.

### 8. INDEPENDENCIA DE LA REPRESENTACIÓN FÍSICA DE DATOS

Los programas de aplicación y actividades del terminal permanecen inalterados a nivel lógico cualesquiera sean los cambios afectuados, tanto en la representanción del almacenamiento, como en los métodos de acceso. 

El modelo relacional es un modelo lógico de datos, y oculta las características de su representación física.

### 9. INDEPENDENCIA DE MODIFICACIONES LÓGICAS DE DATOS

Los programas de aplicación y actividades del terminal permanecen inalterados a nivel lógico cualesquiera sean los cambios que se realicen a las tablas base que preserven la información.

Cuando se modifica el esquema lógico preservando información, no se necesita modificar nada en niveles superiores.

### 10. INDEPENDENCIA DE LAS RESTRICCIONES DE INTEGRIDAD

Las restricciones de integridad para una determinada base de datos relacionales pueden ser definidos en el lenguaje de datos relacionales, y almacenables en el catálogo, no en los programas de aplicación.

Como parte de las restricciones inherentes al modelo relacional (parte de su definición) están: 

  - **Integridad de Entidad**: Toda tabla debe tener una clave primaria.
  - **Integridad de Dominio**: Toda columna de una tabla contendrá valores exclusivamente de un determinado dominio (conjunto de valores válidos).
  - **Integridad Referencial**: Toda clave foránea no nula debe existir en la relación donde es clave primaria.

### 11. INDEPENDENCIA DISTRIBUIDA

Una base de datos relacional es independiente de la distribución.

Las mismas tareas y programas se ejecutan igual en una base de datos centralizada que en una distribuida.

Las bases de datos son fácilmente distribuibles.

### 12. REGLA DE LA NO SUBVERSIÓN

Si en un sistema relacional tiene un lenguaje de bajo nivel, el nivel bajo no puede ser usado para subvenir (saltarse) las reglas de integridad y las restricciones expresadas en los lenguajes relacionales de más alto nivel a la vez.

  - Algunos problemas no se pueden solucional directamente con el lenguaje de alto nivel.
  - Normalmente se usa SQL incorporado en un lenguaje anfitrión para solucionar estos problemas. Se utiliza el concepro de cursor para tratar individualmente las filas de una tabla. En cualquier caso no debe ser posible saltarse las restricciones de integridad impuestos al tratar las filas a ese nivel. 