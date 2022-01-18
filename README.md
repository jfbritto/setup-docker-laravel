
# Setup Docker Para Projetos Laravel
### Passo a passo
Clone Repositório

Copie os arquivos docker-compose.yml, Dockerfile e o diretório docker/ para o seu projeto
```sh
cp -r setup-docker-laravel/* seu-projeto/
```

Crie o Arquivo .env
```sh
cd seu-projeto/
cp .env.example .env
```

Atualizar as variáveis de ambiente do arquivo .env
```dosini
APP_NAME=MeuProjeto
APP_URL=http://localhost:8989

DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=nome_que_desejar_db
DB_USERNAME=root
DB_PASSWORD=root
```

Suba os containers do projeto
```sh
docker-compose up -d
```

Acessar o container
```sh
docker-compose exec projeto bash
```


Instalar as dependências do projeto
```sh
composer install
```


Gerar a key do projeto Laravel
```sh
php artisan key:generate
```


Acessar o projeto
[http://localhost:8989](http://localhost:8989)
