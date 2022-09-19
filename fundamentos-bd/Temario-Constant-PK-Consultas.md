## Unidad 1: Introduccion a las bases de datos
1. Conceptos basicos
2. Objetivos de las bases de datos
3. Areas de aplicacion de los sistemas de bases de datos
4. Modelos de bases de datos
5. Clasificacion de bases de datos
6. Arquitectura de base de datos
7. Arquitectura del SGBD

## Unidad 2: Diseño de bases de dactos con el modelo E-R
1. El proceso de diseño
2. Modelo Entidad-Relacion
3. Diseño con diagramas E-R
4. Modelo E-R extendido
5. La notacion E-R con UML

## Unidad 3: Modelo relacional
1. Introduccion al modelo relacional
2. Conversion de Modelo E-R a Modelo relacional
3. Esquema de la pase de datos
	1. Integridad de entidad
	2. Integridad referencial
4. Restricciones

## Unidad 4: Normalizacion de bases de datos
1. Conceptos basicos
2. Primera forma normal
3. Dependendcias funcionales y transitivas
4. Segunda forma normal
5. tercera forma normal

## Unidad 5: Algebra relacional
1. Operaciones fundamentales del algebra relacional
2. Algebra relacional extendida

## Unidad 6: Introduccion al lenguaje SQL
1. Caracteristicas
2. Lenguaje de Definicion de Datos (LDD)
3. Lenguaje de Manipulacion de Datos (LMD)

------------------------------------------

# Constraint/Primary key

```SQL
Contraint PK_() primary key;
Foreign key
Null/Not null
```

El Constraint tiene una funcion similar a la Foreign Key
Foreign Key es la llave foranea
Null/not null - Este dice si un valor va a ser nulo o No nulo

```SQL
Create table alumnos(
Id_alumnos number(10) constraint PK-Id_alumnos primary key,
nombre char(30) not null,
edad number(3) null,
genero char(2) not null
);
```

>Nota: este codigo lo utilizaremos/utilizamos para crear nuestra primera tabla durante laboratorio (9-9-22)



```SQL
Insert into Alumnos(ID_alumnos, nombre, edad, genero) values(1, `Jose`, 18, `M`);
```

Seria:
|ID_alumnos|nombre|edad|genero|
|-|-|-|-|
|1|Jose|18|M|

Si se inserta otro dato seria:
```SQL
Insert into Alumnos(ID_alumnos, nombre, edad, genero) values(2, `Ana`, 16, `F`);
```

Seria:
|ID_alumnos|nombre|edad|genero|
|-|-|-|-|
|1|Jose|18|M|
|2|Ana|16|F|

```SQL
Insert into Alumnos(ID_alumnos, nombre, edad, genero) values(2, ``, 16, ``);
```

|ID_alumnos|nombre|edad|genero|
|-|-|-|-|
|1|Jose|18|M|
|2|Ana|16|F|
|3|---|---|F|

```SQL
Insert into Alumnos(ID_alumnos, nombre, edad, genero) values(4, `Beto`, 16, `M`);
```

|ID_alumnos|nombre|edad|genero|
|-|-|-|-|
|1|Jose|18|M|
|2|Ana|16|F|
|3|---|---|F|
|4|Beto|16|M|
