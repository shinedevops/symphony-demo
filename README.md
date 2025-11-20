<p align="center">
<a href="https://github.com/shinedevops/symphony-demo">
<img src="https://raw.githubusercontent.com/s-damian/medias/main/technos-logos/symfony.svg">
</a>
</p>

# Example of CRUD with Symfony 6 (6.2)

This example is made by [ShineDevops](https://github.com/shinedevops)

* Admin can manage CRUD of articles.
* Users can view the articles.

## Requirements

* PHP 8.1 || 8.2
* MYSQL
## Configuration - Symfony App

Clone github repository:

```
git clone https://github.com/shinedevops/symphony-demo
```

In terminal, position yourself in the ```symfony-demo``` directory:

```
cd /your_path/symfony-demo/
```

Create and configure your ```.env.local``` file:

```
cp .env.local.example .env.local
```

In your ```.env.local``` file, you need to configure ```DATABASE_URL```.

Install dependencies with composer:

```
composer install || composer update
```

## Database configuration
*  In .env.local
```
DATABASE_URL="mysql://your_name:@127.0.0.1:3306/db_name?serverVersion=mariadb-10.9.4"
```


Create the database:

```
php bin/console doctrine:database:create
```

Run migrations:

```
php bin/console doctrine:migrations:migrate
```

Run local server:

```
php -S 127.0.0.1:8000 -t public
```

## Configuration - Web Server

You have to configure your web server (Linux / Nginx or Apache / MySQL or PostgreSQL / PHP).

## After configuring your Web Server, you can run these demo URLs

* http://127.0.0.1:8000//admin/articles

And you can **Create** / **Read** (listing or show a single article) / **Update** / **Delete** articles.
