## Diagrama Físico: tipos de datos y constraints

Para llevar a la práctica un diagrama debemos ir más allá y darle detalle con parámetros como:

#### Tipos de dato:

  - **Texto**: CHAR(n), VARCHAR(n), TEXT
  - **Números**: INTEGER, BIGINT, SMALLINT, DECIMAL(n,s)NUMERIC(n,s)
  - **Fecha/hora**: DATE, TIME, DATETIME, TIMESTAMP
  - **Lógicos**: BOOLEAN

#### Constraints (Restricciones)

  - **NOT NULL**: Se asegura que la columna no tenga valores nulos
  - **UNIQUE**: Se asegura que cada valor en la columna no se repita
  - **PRIMARY KEY**: Es una combinación de NOT NULL y UNIQUE
  - **FOREIGN KEY**: Identifica de manera única una tupla en otra tabla
  - **CHECK**: Se asegura que el valor en la columna cumpla una condición dada
  - **DEFAULT**: Coloca un valor por defecto cuando no hay un valor especificado
  - **INDEX**: Se crea por columna para permitir búsquedas más rápidas