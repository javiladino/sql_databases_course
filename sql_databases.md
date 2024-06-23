---
title: Tipos de datos en SQL
markmap:
  colorFreezeLevel: 7
---

### Tipos de datos numéricos

1. **Enteros**
    * `INT` o `INTEGER`: Número entero de tamaño estándar.
    * `SMALLINT`: Número entero de menor rango.
    * `TINYINT`: Número entero de rango muy pequeño (comúnmente en MySQL).
    * `BIGINT`: Número entero de mayor rango.
    
2. **Decimales y de punto flotante**
    * `FLOAT`: Número de punto flotante de precisión simple.
    * `DOUBLE` o `DOUBLE PRECISION`: Número de punto flotante de precisión doble.
    * `DECIMAL` o `NUMERIC`: Número exacto con un número fijo de dígitos decimales. El decimal lo vamos a especificar con la palabra reservada `DECIMAL(10,2)`. El segundo valor va a determinar cuál es la precisión fija de almacenamiento que le estás dando a ese decimal.

### Tipos de datos de caracteres (texto)

1. **Cadenas de caracteres**
    * `CHAR(n)`: Cadena de longitud fija. Si asignas 10 espacios `CHAR(10)` para guardar un "hola", este te va a ocupar esos 10 espacios.
    * `VARCHAR(n)`: Cadena de longitud variable. A nivel de procesamiento, aunque en sintaxis se escriben igual, funcionan diferente en procesamiento. Si asignas 10 espacios para un "hola", solamente ocupará esos 4 espacios del "hola".
    
2. **Textos largos**
    * `TEXT`: Cadena de longitud variable de gran tamaño (comúnmente en MySQL).
    * `CLOB` (Character Large Object): Similar a `TEXT` en otros SGBD.

### Tipos de datos de fecha y hora

* `DATE`: Fecha (año, mes, día).
* `TIME`: Hora (hora, minuto, segundo).
* `DATETIME`: Combinación de fecha y hora.
* `TIMESTAMP`: Fecha y hora, generalmente con capacidad de zona horaria.
* `YEAR`: Año (comúnmente en MySQL).

### Tipos de datos booleanos

* `BOOLEAN`: Valor verdadero o falso (no soportado de forma nativa en algunos SGBD, se puede simular con `TINYINT`).

### Tipos de datos binarios

* `BINARY`: Datos binarios de longitud fija.
* `VARBINARY`: Datos binarios de longitud variable.
* `BLOB` (Binary Large Object): Datos binarios de gran tamaño.

### Tipos de Datos Espaciales
* `GEOMETRY:` Almacena datos de coordenadas geométricas. 

* `POINT:` Almacena un punto en un espacio geométrico. 

* `LINESTRING:` Almacena una línea en un espacio geométrico. 
 
* `POLYGON:` Almacena un polígono en un espacio geométrico. 

### Otros tipos de datos

* `ENUM`: Enumeración de valores predefinidos (comúnmente en MySQL).
* `SET`: Conjunto de valores predefinidos (comúnmente en MySQL).
* `XML`: Datos en formato XML.
* `JSON`: Datos en formato JSON (soportado en PostgreSQL, MySQL y otros).
* `UUID`: Identificador único universal.

### Ejemplos en SQL

Aquí hay algunos ejemplos de cómo se definen columnas con diferentes tipos de datos en una tabla SQL:

```sql
CREATE TABLE ejemplo (
    id INT PRIMARY KEY,
    nombre VARCHAR(50),
    edad SMALLINT,
    salario DECIMAL(10, 2),
    fecha_nacimiento DATE,
    es_activo BOOLEAN,
    foto BLOB
);
