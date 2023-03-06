<img src="https://jorgebenitezlopez.com/github/symfony.jpg">

# Symfony login

Instalación de Symfony y creación de test

# Requisitos

- Symfony CLI: https://symfony.com/download
- PHP: PHP 8.2.3 (cli). Por ejemplo se puede descargar en OSX con: https://formulae.brew.sh/formula/php
- Composer: https://getcomposer.org/download/


# Pasos para la instalación de Symfomy y paquetes

- new symfony users  --version=5.4
- composer require symfony/orm-pack (Sin docker)
- composer require symfony/maker-bundle
- composer require form validator twig-bundle security-csrf annotations
- composer require symfony/security-bundle



# Configuración y creación de entidades

- Modificamos el .env para que genere un sqlite (https://www.sqlite.org/index.html)
- php bin/console make:entity (Creamos la entidad user)
- php bin/console make:crud (Creamos el CRUD de la entidad)
- php bin/console doctrine:schema:update --force (Actualizamos la base de datos) 


# Rutas de la aplicación:

| URL path                    | Description           | 
| :--------------------------:|:---------------------:|
| /user                    |  Listado de usuarios  | 


# Referencias

https://symfony.com/doc/5.4/security/user_providers.html

