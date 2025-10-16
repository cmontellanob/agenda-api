# habiliar api en laravel
php artisan install:api

## Crear un modelo, su controlador, su migracion, su seeder y su factory
php artisan make:model Persona -mcrsf --api
## Instalar libreria
composer require firebase/php-jwt

# Escribir codigo en el archivo .env
JWT_SECRET=secret
JWT_ALGORITHM=HS256

# Crear el midleware 
php artisan make:middleware JwtMiddleware

# Escribir codigo del midleware
 escribir elcodigo para leer el token  
# Proteger las rutasincluyendo a las que sean necesarias
->middleware(JwtMiddleware::class)
# crear un Controlador para el login
php artinas make:controller LoginController