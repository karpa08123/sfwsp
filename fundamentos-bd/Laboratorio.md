En mi caso se realizo una bd diferente
se realizo un punto de venta con 3 tablas:
articulos, usuarios, ventas

se utilizaron los siguientes comandos:
```SQL
Create table productos(Id_product number(10) Cosntraint Pk_Id_producto primary key, name char(30) not null, price number(3) null);

create table users(Id_user number(10) Constraint Pk_Id_user primary key, name char(30) not null, schelude number(6) not null);
/*al horario se le dio un formato de 6 numeros para poner el dia trabajado en formato DDMMYY */

create table sell(Id_sell number(10) Constraint Pk_Id_sell primary key, name char(20) not null, transaction char(20) not null, tValue number(4) null);
```

Luego se insertaron 3 datos en cada tabla:
##### Productos:
```SQL
Insert into productos(Id_product, name, price) values(1,'doritos', 45);

Insert into productos(Id_product, name, price) values(2,'tostitos', 50);

Insert into productos(Id_product, name, price) values(3,'Sol_pepitas', 20);
```

##### Users:
```SQL
Insert into users(Id_user, name, shelude) values(1,'Antonio',090922);

Insert into users(Id_user, name, shelude) values(2,'Juan',100922);

Insert into users(Id_user, name, shelude) values(3,'Pedro',110922);
```

##### Sell:
```SQL
Insert into sell(Id_sell,name,transaction,tValue) values(1,'Antonio','venta',600);

Insert into sell(Id_sell,name,transaction,tValue) values(2,'Juan','venta',30);

Insert into sell(Id_sell,name,transaction,tValue) values(3,'Pedro','nenta',600);
```

Posterior a esto se realizo una consulta a cada tabla para ver los resultados:
```SQL
Select * from sell;
```

|Id_sell|Name|Transaction|TValue|
|-|-|-|-|
|1|Antonio|venta|600|
|2|Juan|Venta|30|
|3|Pedro|Devolucion|20|


```SQL
Select * from productos;
```

|Id_product|name|price|
|-|-|-|
|1|doritos|45|
|2|Tostitos|50|
|3|Sol_pepitas|20|


```SQL
Select * from users;
```

|Id_user|name|schelude|
|-|-|-|
|1|Antonio|090922|
|2|Juan|100922|
|3|Pedro|110922|


Al final de todo esto se borraron todas las tablas

```SQL
drop table users;

drop table productos;

drop table sell;
```