---
title: Oracle Indexes
author: Kenar716
---

**Indices para mejorar tus consultas**

Los índices en determinadas situaciones pueden mejorar el desempeño de tus consultas a la base de datos.

Un índice es una estructura de datos que es usada para ubicar y acceder  rapidamente a los datos en una tabla (con un pequeño costo adicional de escritura) sin necesidad de buscar renglon por renglon cada vez que se accede a la tabla, los indices puede crearse con una o variables columnas.

En oracle la sintaxis para crear un indice es la siguiente:

```
CREATE INDEX <esquema>.<nombre_indice> ON <esquema>.<nombre_tabla>
(
    <columna1>, <columna2>, ... 
);
```

Cuando  un índice incluye más de una columna se le llama Indice Compuesto y al manejar este tipo de indices es muy importante considerar el orden en que se declaran las columnas.

Para que el indice sea utilizado un una consulta y esta sea vea beneficiada por dicha estructura es necesario que las columnas declaradas en la clausula WHERE utilice la mayoria de las columas en orden jerarquico

Por ejemplo con el siguiente índice:
```
CREATE INDEX IDX_Empleados
    ON T_Empleados (Apellido, Edad, Salario);
```

Si se realiza la consulta:
```
SELECT * FROM T_Empleados WHERE Salario >= 2000;
```

El indice no tendra efecto por que la columna apellido no se utiliza en la clausula WHERE.

Mas sin embargo si realizamos la siguiente consulta si se utiliza el indice, incluso cuando no se especifica la columna salario, y esto es por que se utiliza las primeras dos columnas.
```
SELECT * FROM T_Empleados WHERE Apellido = 'GONZALEZ' AND Edad >= 25;
```
Incluso si se realiza de la siguiente manera se aprovecha el indice por que lo importante es el peso que tienen las columnas en el indice.
```
SELECT * FROM T_Empleados WHERE Apellido = 'RODRIGUEZ' AND Edad >= 25;
```


![Employee Index Example](/assets\images\posts\2018-12-06-oracleindexes\oracle_employee_index.gif)


Al momento de crear indices es muy importante considerar que según la cantidad de registros y las columnas a indexar se puede consumir una gran cantidad de recursos lo cual puede afectar ambientes productivos, las siguientes consultas pueden ayudar a medir la memoria consumida por los Tablespaces Temporales al momento de crear el indice, se recomienda evaluar estas consultas y la creación de indices en ambientes de pruebas o en horarios no productivos, algunas de las siguientes consultas requeriran permisos de DBA.

Determinar el Tablespace Temporal del usuario de la sesión.
```
SELECT USERNAME, DEFAULT_TABLESPACE, TEMPORARY_TABLESPACE
FROM DBA_USERS
WHERE USERNAME = 'Nombre_Usuario';
```

Determinar la cantidad de memoria consumidad por los diferentes procesos de la base de datos.
```
SELECT Username, Machine, Program, OSUser, sum("Chunks (Mb)") SizeMBUsed, Tablespace
FROM
(
    SELECT DISTINCT(se.username), SE.Machine, SE.Program, SE.OSUser
        , to_char(SE.Logon_Time, 'DD-MON HH:MM') Login, SE.SID, SE.Serial#
        , SU.Blocks/1048576 * (to_number(rtrim(P.Value))) AS "Chunks (Mb)", Tablespace
    FROM v$sort_usage SU,
        v$parameter P,
        v$session SE
    WHERE P.Name = 'db_block_size'
        AND SU.Session_Addr = SE.Saddr
        AND SU.Tablespace LIKE '%TEMP%'
    ORDER BY SE.Username, Login, SE.SID
)
GROUP BY Username, Machine, Program, OSUser, Tablespace
ORDER BY Tablespace, SizeMBUsed, Program, Username, Machine, OSUser
;
```

Determinar el tamaño fisico de los Tablespaces de la base de datos.
```
SELECT /* + RULE */  DF.Tablespace_Name "Tablespace",
    DF.Bytes / (1024 * 1024) "Size (MB)",
    SUM(FS.Bytes) / (1024 * 1024) "Free (MB)",
    NVL(ROUND(SUM(FS.Bytes) * 100 / DF.Bytes), 1) "% Free",
    ROUND((DF.Bytes - SUM(FS.Bytes)) * 100 / DF.Bytes) "% Used"
FROM DBA_Free_Space FS,
    (
    SELECT Tablespace_Name, SUM(Bytes) Bytes
    FROM DBA_Data_Files
    GROUP BY Tablespace_Name
    ) DF
WHERE FS.Tablespace_Name (+) = DF.Tablespace_Name
GROUP BY DF.Tablespace_Name, DF.Bytes

UNION ALL

SELECT /* + RULE */ DF.Tablespace_Name TSpace,
    FS.Bytes / (1024 * 1024),
    SUM(DF.Bytes_Free) / (1024 * 1024),
    NVL(ROUND((SUM(FS.Bytes) - DF.Bytes_Used) * 100 / FS.Bytes), 1),
    ROUND((SUM(FS.Bytes) - DF.Bytes_Free) * 100 / FS.Bytes)
FROM DBA_Temp_Files FS,
    (
        SELECT Tablespace_Name, Bytes_Free, Bytes_Used
        FROM v$temp_space_header
        GROUP BY Tablespace_Name, Bytes_Free, Bytes_Used
    ) DF
WHERE FS.Tablespace_Name (+) = DF.Tablespace_Name
GROUP BY DF.Tablespace_Name, FS.Bytes, DF.Bytes_Free, DF.Bytes_Used
ORDER BY 4 DESC;
```

**Nota:** Los indices no son utilizados si la clausula WHERE aplica el operador LIKE sobre una de las columnas del índice.

asdasd
En los siguiente enlaces se puede encontrar información mas detalle acerca de los índices en oracle.
* [https://blogs.oracle.com/sql/how-to-create-and-use-indexes-in-oracle-database](https://blogs.oracle.com/sql/how-to-create-and-use-indexes-in-oracle-database)
* [https://docs.oracle.com/cd/B19306_01/server.102/b14200/statements_5010.htm](https://docs.oracle.com/cd/B19306_01/server.102/b14200/statements_5010.htm)
* [https://docs.oracle.com/cd/B28359_01/server.111/b28310/indexes003.htm#ADMIN11722](https://docs.oracle.com/cd/B28359_01/server.111/b28310/indexes003.htm#ADMIN11722)
* [https://docs.oracle.com/cd/E11882_01/server.112/e40540/indexiot.htm#CNCPT721](https://docs.oracle.com/cd/E11882_01/server.112/e40540/indexiot.htm#CNCPT721)
* [https://richardfoote.wordpress.com/](https://richardfoote.wordpress.com/)