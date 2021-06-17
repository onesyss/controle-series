<h1 align="center"> Controle de Séries</h1>

<p align="center"><img src="https://laravelnews.imgix.net/images/jetstream.png?ixlib=php-3.3.0" width="500"></p>

<img src="https://img.shields.io/static/v1?label=Status&message=Concluido&color=54CD26&style=for-the-badge&logo=ghost"/>

## Descrição do Projeto
<p align="justify"> Desenvolver uma plataforma capaz de controlar as series já assistidas informando as quantidade
de temporadas e episodios.</p>

## Tópicos

<!--ts-->
   * [Instalação](#instalacao)
      * [Pré Requisitos](#pre_requsito)
      * [Preparando aplicação](#preparando_aplicacao)
   * [Demo da aplicação](#demo)
<!--te-->

<h2 id="instalacao">Instalação</h2>

<h3 id="pre_requsito" >Pré Requisitos</h3>

- Php 7.3 ou superior
- Banco de dados mysql
- Composer
- Node

<h3 id="preparando_aplicacao" >Preparando aplicação</h3>

- Clone este repositório para um repositório local com comando:

    ` git clone <repositorio>`

- Após isso entre no repositório raiz da aplicação e execute o seguinte comando:

    ` composer install`

- A versão atual do composer está encontrando alguns problemas, no caso usei o ilustrado a baixo.

Como posso corrigir esse problema?
Vá em: 

vendor/laravel/framework/src/Illuminate/Foundation/PackageManifest.php
Encontre esta linha e comente-a:

$packages = json_decode($this->files->get($path), true);
Adicione duas novas linhas após a linha comentada acima:

$installed = json_decode($this->files->get($path), true);
$packages = $installed['packages'] ?? $installed;

- Altere o arquivo `.env.example` para somente `.env` e abra ele,
  crie um banco de dados vazio e o configure neste bloco:

    ```
DB_CONNECTION=sqlite
#DB_HOST=127.0.0.1
#DB_PORT=3306
#DB_DATABASE=homestead
#DB_USERNAME=homestead
#DB_PASSWORD=secret
    ```
- Fazendo isso use o comando `php artisan migrate` para gerar todas as tabelas no banco que a aplicação utilizará

- Execute a aplicação com o comando:

    `php artisan serve`

- Por padrão, ele irá executar a aplicação em `localhost:8000/series`, abra o navegador e digite o caminho.

<!-- <h2 id="demo">Demo da aplicação</h2>
 
 - <a href="https://www.tagsolution.com.br/teste_masterix/public">Veja aqui o demo da aplicação</a> -->
