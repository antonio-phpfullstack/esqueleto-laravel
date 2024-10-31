# Esqueleto Gratuito do Laravel 11.x/PostgreSQL

## Ao final do projeto você terá um ambiente:
- PHP 8.3.13
- Nginx, versão mais estável
- Laravel 11.30.0 
- PostgreSQL 13
- PgAdmin, semelhante ao PHPMyAdmin mas para PostgreSQL
- Redis, versão mais estável

**Links Úteis:**

- :tada: [Site: https://phpfullstack.com.br](https://phpfullstack.com.br/)

## Passo a passo para rodar o projeto
**Clone o projeto**
```sh
git clone https://github.com/antonio-phpfullstack/esqueleto-laravel esqueleto-laravel
```
```sh
cd esqueleto-laravel/
```


**Crie o Arquivo .env**
```sh
cp .env.example .env
```


**Atualize essas variáveis de ambiente no arquivo .env**
```dosini
APP_NAME="Esqueleto Laravel"
APP_URL=http://localhost:8000

# Configuração para PostgreSQL
DB_CONNECTION=pgsql
DB_HOST=db           
DB_PORT=5432
DB_DATABASE=esqueleto_laravel  
DB_USERNAME=noreply@phpfullstack.com.br         
DB_PASSWORD=admin        

CACHE_DRIVER=redis
QUEUE_CONNECTION=redis
SESSION_DRIVER=redis

REDIS_HOST=redis
REDIS_PASSWORD=null
REDIS_PORT=6379
```

**No arquivo Dockerfile, altere o nome do usuário para o usuário linux da sua máquina, ex: user=antonio**
```sh
ARG user=seu_usuario_linux
```

**Suba os containers do projeto**
```sh
docker-compose up -d
OU
docker compose up -d
```


**Acesse o container**
```sh
docker-compose exec app bash
OU
docker compose exec app bash
```


**Instale as dependências do projeto**
```sh
composer install
```


**Gere a key do projeto Laravel**
```sh
php artisan key:generate
```


## Acesse o projeto

- :rocket: [http://localhost:8000](http://localhost:8000)

## Acesse o PgAdmin

- :brain: [http://localhost:8080](http://localhost:8080)
- :man: Usuário: noreply@phpfullstack.com.br
- :key: Senha: admin
