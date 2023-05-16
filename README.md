# laravel Docker Images

Services:
- Nginx
- PHP-FPM
- MySQL
- [Artisan](https://laravel.com/docs/10.x/artisan)

## Usage

Just copy `docker-compose.yml` to root of your project and run:

```
docker-compose up -d
```

Then check your `.env` file `DB_*` variables:

```
DB_CONNECTION=mysql
DB_HOST=database
DB_PORT=3306
DB_DATABASE=laravel
DB_USERNAME=laravel
DB_PASSWORD=laravel
```

### Artisan
```
docker-compose run artisan
```

## Contributing

### Build Images

```
docker build -t s1doryak/laravel-cli ./cli
docker build -t s1doryak/laravel-fpm ./fpm
docker build -t s1doryak/laravel-nginx ./nginx
```

### Login to Docker Hub

```
docker login
```

### Push Images

```
docker push s1doryak/laravel-cli
docker push s1doryak/laravel-fpm
docker push s1doryak/laravel-nginx
```