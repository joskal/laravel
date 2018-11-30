# Laravel
PHP Framework.

## Instalación para Windows 
En Windows podemos optar por instalar primeramente el servidor web local [Laragon](https://laragon.org/) seguido de Laravel a través de [Composer](https://getcomposer.org/).

## Instalación para Mac.
Mediante composer, ir a download y copiar las lineas que se indican y pegarlas en un terminal.
```php
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('sha384', 'composer-setup.php') === '93b54496392c062774670ac18b134c3b3a95e5a5e5c8f1a9f115f203b75bf9a129d5daa8ba6a13e2cc8a1da0806388a8') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"
```
Comprobamos que tenemos instalado composer.
```php
php composer.phar
```

Para mayor comodidad lo renombraremos como `composer` y lo moveremos a `/usr/local/bin`.
```bash
mv ./composer.phar /usr/local/bin/composer
```

Ahora sí que procedemos a la instalación de laravel.
```bash
composer global require laravel/installer

#Comprobamos que se ha instalado correctamente.
laravel

#Descargamos e instalamos valet
composer global require laravel/valet
valet install
```
El siguiente paso será crear un directorio de trabajo. Lo propio sería hacerlo donde tengamos alojadas las webs de nuestro servidor local.
```bash
mkdir ~/sites/laravel
cd ~/sites/laravel

#Agregamos este directorio a los path de valet
valet park
```

Comprobar que tenemos la última versión de valet
```bash
valet on-latest-version
```
Si no es así podemos actualizarlo.
```bash
composer global update laravel/valet
```
