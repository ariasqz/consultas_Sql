# Consulta #1 Sql

## CONSULTAS SQL


1. Para visualizar toda la información que contiene la tabla `usuario` se puede incluir con la instrucción SELECT el caracter `*` o cada una de los campos de la tabla 

- `SELECT * FROM usuario`

![tabla usuario](./img/tabla_usuario.png "Tabla usuario")

2. Seleccionar o visualizar solamente la identificación del usuario.

- `SELECT Identificación FROM usuario`

![tabla usuario](./img/tabla_identificacion.png "Tabla Identificacion")

3. Se desea obtener los registros uya identificacion sean mayores 0 iguales a 150, se debe utilizar la clausula WHERE que especifica las condiciones que deben reunir los registros que se van a seleccionar

`SELECT * FROM usuario WHERE identificacion>='150'`

![tabla usuario](./img/consulta3.png "Tabla igual mayor que")
