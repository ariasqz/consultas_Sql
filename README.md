# Consulta #1 Sql

## CONSULTAS SQL


1. Para visualizar toda la información que contiene la tabla `usuario` se puede incluir con la instrucción SELECT el caracter `*` o cada una de los campos de la tabla 

- `SELECT * FROM usuario`

![consulta1](./img/tabla_usuario.png "Tabla usuario")

2. Seleccionar o visualizar solamente la identificación del usuario.

- `SELECT Identificación FROM usuario`

![consulta2](./img/tabla_identificacion.png "Tabla Identificacion")

3. Se desea obtener los registros uya identificacion sean mayores 0 iguales a 150, se debe utilizar la clausula WHERE que especifica las condiciones que deben reunir los registros que se van a seleccionar

`SELECT * FROM usuario WHERE identificacion>='150'`

![consulta3](./img/consulta3.png "Tabla igual mayor que")

4. si se desea obtener los registros cuyo susu apelllidos sean vanegas  o cetina, se utiliza el operador IN que especifica los registros que se quieren visualizar de una tabla

`SELECT apellidos FROM usuario WHERE apellidos IN ('Vanegas','Cetina')`

![consulta4](./img/consulta4.png "consulta4")

o se puede uilizar el operador OR.

`SELECT apellidos FROM usuario WHERE apellidos='Vanegas' OR apellidos='Cetina'`

![consulta4](./img/consulta4_2.png "consulta4")

5. si se desea obtener los registros cuya identificacion sea menor de '110' y la ciudad sea 'Cali', se debe utilizar el operador AND.

`SELECT * FROM usuario WHERE Identificacion<'110' AND ciudad_nac='Cali'`

![consulta5](./img/consulta5.png "consulta5")

6. si se desea obtener los registros cuyos nokbres empiecen por la letra 'A', se debe utilizar el operador LIKE que utiliza los patrones '%' (todos)  '_' (caracter).

`SELECT * FROM usuario WHERE nombre LIKE 'A%'`

![consulta6](./img/consulta6.png "consulta6")

7. si se desea obtener los registros que contengan la letra a

`SELECT * FROM usuario WHERE nombre LIKE '%a%'`

![consulta7](./img/consulta7.png "consulta7")

8. si se desea obtener los registros donde la cuarta letra del nombre sea una 'a'.

`SELECT * FROM usuario WHERE nombre LIKE '____a%'`

![consulta8](./img/consulta8.png "consulta8")

9. si se desea obtener los registros cuya identificacion este entre el intervalo 110 y 150, se deb utilizar la clausula BETWEEN , sirve para especificar un intervalo de valores. 

`SELECT * FROM usuario WHERE Identificacion BETWEEN '110' AND '150'`

![consulta9](./img/consulta9.png "consulta9")

## COMANDO DELETE 

10. para eliminar solamente los registros cuya identificacion sea mayor de 130.

`DELETE FROM usuario WHERE Identificacion>'130'`

![consulta10](./img/consulta10.png "consulta10")

## COMANDO UPDATE 

11. para acualizar la ciudad  de nacimiento de cristian Vanegas, cuya identificacion es 114.

`UPDATE usuario SET ciudad_nac = 'Manizales' WHERE identificacion= '114'`

![consulta11](./img/consulta11.png "consulta11")

## INNER JOIN 

permite obtener datos de dos o mas tablas. cuando se realiza la concatenacion de las tablas, no necesariamente  se debn mostrar todos los datos de las tablas.

## TABLA PEDIDOS

![tabla pedidos](./img/tabla_pedidos.png "tabla pedidos")

12. para visualizar los campo identificacion, nombre, apelidos de la tabla de usuario y nropedido, fecha de compra, fecha de vencimiento  observacion de la tabla pedidos, se debe realizar la siguiente instruccion SQL:

`SELECT usuario.identificacion, usuario.nombre, usuario.apellidos, pedido.nropedido, pedidos.fechaCompra, pedidos.fechaVence, pedidos Observacion, FROM usuario INNER JOIN pedidos ON usuario.identificacion = pedidos.identificacion`

![consulta12](./img/consulta12.png "consulta12")

13. para viualizar todos los campos de las tablas usuarios y pedidos dode identificacion sea mayor que 100, se debe realizar la siguiente instruccion:

`SELECT usuarios.*, pedidos.* FROM usuaruos INNER JOIN pedidos ON usuarios.identificacion = pedidos.identificacion WHERE usuarios.identificacion>100`

![consulta13](./img/consulta13.png "consulta13")
