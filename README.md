
# Setup Docker Para Projetos PHP 8.1

### Passo a passo
Abra o terminal na maquina WSL 2 e Clone Repositório
```sh
https://github.com/jadirbento/setup-docker-laravel-php81.git nome-do-projeto
```

Entre no diretório do projeto
```sh
cd nome-do-projeto
```

Abra o projeto no VS Code  

########### alterações nos arquivos de setup ##################### 

#app -> appsaas [docker-compose.yml linha:5, deault.conf linha:13] 

#Dockerfile 

-nome do usuario WSL 2- 

ARG user=jadirbento 

ARG uid=1000 

#nome da rede [dminpanelsaas] 

#porta nginx:8083 

#porta host:3383 

#nome do host mysql:host1  [docker-compose.yml linha:31, .env linha:12]

####################################### 


```sh
code .
```

Suba os containers do projeto
```sh
docker-compose up -d
```

Acessar o container (para executar comandos do Composer, exemplo: composer init)
```sh
docker-compose exec app bash
```


Instalar as dependências do projeto
```sh
composer install
```


Acessar o projeto
[http://localhost:8083](http://localhost:8083)
