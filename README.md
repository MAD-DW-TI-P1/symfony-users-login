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
- composer require symfonycasts/verify-email-bundle
- composer require symfony/mailer 
- composer require --dev symfony/profiler-pack 
- composer require "lexik/jwt-authentication-bundle"



# Configuración y creación de entidades

- Modificamos el .env para que genere un sqlite (https://www.sqlite.org/index.html)
- php bin/console make:user (Creamos la entidad user)
- php bin/console make:registration-form (Con email to verify the user's)
- En env. añadimos: MAILER_DSN="smtp://xxxxx:yyyyy@smtp1.s.ipzmarketing.com:587"
- php bin/console doctrine:schema:update --force (Actualizamos la base de datos)
- php bin/console make:controller Login 
- Añadir el formulario de login y el controlador

- php bin/console lexik:jwt:generate-keypair (En config, jwt creas las claves públicas y privadas)

# TODO

In RegistrationController::verifyUserEmail():
    * Customize the last redirectToRoute() after a successful email verification.
    * Make sure you're rendering success flash messages or change the $this->addFlash() line.
Review and customize the form, controller, and templates as needed.
Run "php bin/console make:migration" to generate a migration for the newly added User::isVerified property.

# Rutas de la aplicación:

| URL path                    | Description           | 
| :--------------------------:|:---------------------:|
| /register                    |  Registro de usuarios  | 


# Referencias

https://symfony.com/doc/5.4/security/user_providers.html
https://symfony.com/doc/master/mailer.html
https://symfony.com/bundles/LexikJWTAuthenticationBundle/current/index.html#installatio
https://symfony.com/doc/5.4/security.html#form-login



