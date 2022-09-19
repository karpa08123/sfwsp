# Depurar y borrar campos

```SQL
Drop
Truncate table
```

Drop funciona para borrar toda la tabla
Truncate sirve para unicamente borrar todos los datos de la tabla.

-----------------------------------

## Consulta simple con condicional

|Id_pasteleria|pastel|costo|trabajadores|
|-|-|-|-|
|1|choco|10|5|
|2|miel|15|3|

```SQL
Select trabajadores from pasteleria where pastel='miel';
```

