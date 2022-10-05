# Symfony 4 Auth


Este proyecto es una "prueba de concepto" para demostrar cómo construir un sistema de autenticación con Symfony 4 sin dependencias (como FOSUserBundle).

Cubre las siguientes características:

- Registro de usuario, iniciando sesión automáticamente y redirigiéndolo a la página de inicio con un mensaje flash
- Inicio de sesión de usuario con correo electrónico
- Opción Recordarme disponible en el formulario de inicio de sesión
- Configura automáticamente la marca de tiempo created_at del usuario al registrarse usando los eventos del ciclo de vida de Doctrine
- Oyente para evitar que el usuario regrese a páginas anónimas cuando inicie sesión
- Oyente para actualizar automáticamente la última marca de tiempo de inicio de sesión del usuario en cada autenticación exitosa
- Gestión de activos con [@symfony/webpack-encore](https://symfony.com/doc/current/frontend.html)

La información y colaboración corresponden a @fidan. Información clonada para aplicaciones de Login.

Atentamente, Miguel Alvarez.
alvarezgalea@gmail.com


ENGLISH VERSION....

[![Build Status](https://travis-ci.com/fidanf/symfony4-auth.svg?branch=master)](https://travis-ci.com/fidanf/symfony4-auth)

This project is a "proof of concept" to demonstrate how to build an authentication system with Symfony 4 using no dependencies (such as FOSUserBundle).

It covers the following features :

- User registration, automatically logging the user and redirecting him to home page with a flash message
- User login with email
- Remember me option available on the login form
- Automatically sets up the user's created_at timestamp upon registration using Doctrine Lifecycle events
- Listener to prevent the user to go back to anonymous pages when logged in
- Listener to automatically update user's last login timestamp upon every successful authentication
- Assets management with [@symfony/webpack-encore](https://symfony.com/doc/current/frontend.html) 

## Requirements 

- PHP >=7.3

## Setting up

Install dependencies

```bash
composer install
npm install # or yarn install
npm run dev
```

Generate database schema
```bash
php bin/console doctrine:migrations:migrate
```

### Live demo

<https://symfony4-auth.frank-fidanza.fr/>



