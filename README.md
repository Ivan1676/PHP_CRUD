# Proyecto CRUD

---
Modulo: Desarrollo Web en Entorno Servidor

Curso: 2º DAW Vespertino (2022-2023)

Centro: CPIFP Los Enlaces

Profesor: Manuel Alejandro Romero [@MAlejandroR](https://github.com/MAlejandroR)

Autor: Carlos Sesma Usarralde

Fecha: 19-1-2023

---

## Descripción

Este proyecto consiste en la creación de un CRUD (Create, Read, Update, Delete) de una base de datos. El proyecto se ha realizado con el lenguaje PHP y la base de datos MySQL/MariaDB.

## Requisitos

- PHP 7.4
- PHPMyAdmin
- MySQL/MariaDB
- Servidor Apache

## Configuración

Para desplegar el proyecto se debe acceder a phpmyadmin con un usuario con permisos de gestion de usuarios y crear un nuevo usuario con permisos de SELECT, INSERT, UPDATE y  DELETE sobre las tablas de la base de datos "dwes".

```mysql
-- A este usuario le daremos permisos de CRUD para las tablas de dwes
USE dwes;
GRANT SELECT, INSERT, UPDATE, DELETE on dwes.* TO 'webuser';
```

Una vez creado debemos editar el archivo credenciales.php.example y cambiar los datos de usuario y contraseña por los del usuario creado anteriormente.

Por último, debemos renombrar el archivo credenciales.php.example a credenciales.php.

Tambien se debe crear la tabla "usuarios" en la base de datos "dwes" con los siguientes campos:

- user(varchar(50))
- pass(varchar(200))

```sql
CREATE TABLE `dwes`.`usuarios` ( `user` varchar(50) NOT NULL , `pass` varchar(200) NOT NULL ) ENGINE = InnoDB
```
