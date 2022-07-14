# Aprendiendo Oracle SQL

En este repositorio se encuentarn las notas de las lecciones de Oracle SQL. 

### GESTIÓN DE USUARIOS

* #### Creacion de un usuario
```
CREATE USER cursooracle IDENTIFIED BY "123456789"
DEFAULT TABLESPACE SYSTEM
TEMPORARY TABLESPACE TEMP
QUOTA UNLIMITED ON SYSTEM;
```
* #### Eliminar un usuario
```
DROP USER cursooracle CASCADE;
```
* #### Ver al usuario al que estoy conectado
```
SELECT USER FROM DUAL;
```

### PRIVILEGIOS

* #### Privilegio para conectarse a la base de datos
```
GRANT CREATE SESSION TO cursooracle;
```
* #### Crear tablas dentro de la base de datos
```
GRANT CREATE TABLE TO cursooracle;
```
* #### Crear vistas en la base de datos
```
GRANT CREATE VIEW TO cursooracle;
```
* #### Crear procedimientos
```
GRANT CREATE PROCEDURE TO cursooracle;
```
* #### Para crear secuencias
```
GRANT CREATE SEQUENCE TO cursooracle; 
```

### CREACIÓN DE TABLAS

* #### Ver todas las tablas del sistema
```
select * from all_tables;
```
* #### Crear una tabla
```
CREATE TABLE empleado(
    id_empleado INT NOT NULL,
    nombre VARCHAR2(20),
    direccion VARCHAR2(50),
    documento VARCHAR2(10),
    sueldo  NUMBER(6,2),
    fecha_nacimiento DATE
);
```
* #### Mostrar la estructura de una tabla
```
DESCRIBE empleado;
```
* #### Consultar la tabla
```
SELECT * FROM empleado;
```
* #### Insertar elementos en una tabla
```
INSERT INTO empleado VALUES(003,'Paola','Carrera 18 # 78-24',0147,4000.00, to_date('10/03/1988','dd/mm/yyyy'));
```
