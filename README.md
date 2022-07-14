# Aprendiendo Oracle SQL

En este repositorio se encuentarn las notas de las lecciones de Oracle SQL. 

### GESTIÓN DE USUARIOS

* #### Creacion de un usuario
```
create user cursooracle2 identified by "123456789"
default tablespace system
temporary tablespace temp
quota unlimited on system;
```
* ### Eliminar un usuario
```
drop user cursooracle2 cascade;
```

### PRIVILEGIOS

* #### Privilegio para conectarse a la base de datos
```
grant create session to cursooracle2;
```
* #### Crear tablas dentro de la base de datos
```
grant create table to cursooracle2;
```
* #### Crear vistas en la base de datos
```
grant create view to cursooracle2;
```
* #### Crear procedimientos
```
grant create procedure to cursooracle2;
```
* #### Para crear secuencias
```
grant create sequence to cursooracle2; 
```
