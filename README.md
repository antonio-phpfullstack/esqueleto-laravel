# Esqueleto Gratuito do Laravel 11.x/PostgreSQ


Links Úteis:

- :tada: [Site Pessoal](https://phpfullstack.com.br/)

## Passo a passo para rodar o projeto
Clone o projeto
```sh
git clone https://github.com/antonio-phpfullstack/esqueleto-laravel esqueleto-laravel
```
```sh
cd esqueleto-laravel/
```


Crie o Arquivo .env
```sh
cp .env.example .env
```


Atualize essas variáveis de ambiente no arquivo .env
```dosini
APP_NAME="Esqueleto Laravel"
APP_URL=http://localhost:8000

# Configuração para PostgreSQL
DB_CONNECTION=pgsql
DB_HOST=db           
DB_PORT=5432
DB_DATABASE=esqueleto_laravel  
DB_USERNAME=antonio@phpfullstack.com.br         
DB_PASSWORD=admin        

CACHE_DRIVER=redis
QUEUE_CONNECTION=redis
SESSION_DRIVER=redis

REDIS_HOST=redis
REDIS_PASSWORD=null
REDIS_PORT=6379
```


Suba os containers do projeto
```sh
docker-compose up -d
```


Acesse o container
```sh
docker-compose exec app bash
```


Instale as dependências do projeto
```sh
composer install
```


Gere a key do projeto Laravel
```sh
php artisan key:generate
```


Acesse o projeto
[http://localhost:8000](http://localhost:8000)
