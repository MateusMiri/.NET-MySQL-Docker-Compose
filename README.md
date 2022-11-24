# BIBLIOTECA DE LIVROS ON DOCKER 
<div id="top"></div>

## 💡 Sobre o projeto
Repositório do Trabalho sobre Docker Compose - Sistemas Operacionais/Atitus 02/2022

Esse repositório contém arquivos com uma sede de Banco de Dados MySQL sobre livros, imitando uma biblioteca, eles serão visualizados em modo JSON com:
>
> numeração única por ID
>
> strings relatando o nome dos livros
>
> e strings com as descrições dos mesmos
>

## :envelope: Conteúdo

* Docker/Docker Compose e Containers 🗸

* Ubuntu e Virtual Machines 🗸

* Banco de Dados MySQL 🗸

* Visualização de uma "Biblioteca" com um catálogo de livros 🗸


## 👀 Pré - Requisitos

Frameworks e Bibliotecas necessárias durante o processo:

* [Ubuntu](https://ubuntu.com/download)
* [Docker](https://docs.docker.com/engine/install/ubuntu/)
* [MySQL 5.7.13](https://www.mysql.com/downloads/)
* [Asp.net](https://dotnet.microsoft.com/en-us/apps/aspnet)
* [Docker Compose](https://docs.docker.com/compose/install/)
* [GitHub](https://github.com/tometchy/Docker-compose-dotnet-core-and-mysql.git)
* Back-End: #C



## 💻 Execução 

1. Baixar os documentos do repositório na sua máquina VM para que a biblioteca fique disponível e os exemplos possam ser visualizados futuramente;


2. Para rodar o Container e criar as imagens, basta rodar o comando (o --build é opcional, utilizado para atualizar quaisquer mudanças): 
 * docker compose up = busca o arquivo.yml e constrói tudo = redes, imagens, etc; 
   
     ```
     docker-compose up -d --build
     ```
     
     
     
 3. Para limpar Containers e Redes, basta rodar o comando: 
 
   
     ```
     docker-compose down 
     ```
     
 
 4. Para visualizar os Containers, Imagens e Portas da VM, como na imagem, basta rodar o comando: 
 
     ```
     docker ps
     ```
     ![image](https://user-images.githubusercontent.com/106711311/203683938-805d603a-0434-4ed5-b874-dae7454a4a72.png)

5. Para acessar o sistema em sua máquina, entre na url:   ``` http://localhost:8080/ ```
* Caso não obter um resultado, espere alguns segundos pois o banco de dados MySQL pode não estar 100% inicializado;
 
   * pela Máquina Virtual
   
       ``` json
      [
          {
            "id": 1,
            "name": "Dependency Injection Principles, Practices, and Patterns",
            "description": "Book by Steven van Deursen and Mark Seemann"
          },
          {
            "id": 2,
            "name": "Agile Software Development, Principles, Patterns, and Practices",
            "description": "Book by Robert C. Martin"
          }
      ]
       ```
   
   * pelo Host
   
      ![image](https://user-images.githubusercontent.com/106711311/203680530-9f501419-fba8-4143-a4ee-7d3201af9fcf.png)

   


 6. Conteúdo do Docker Compose.yml:
 * Versão
 * Serviços - Containers e seus conteúdos
 * Portas e Dependências
 
     ![image](https://user-images.githubusercontent.com/106711311/203834714-d51db65b-4e8c-4cac-9157-0e53e03006f7.png)

 7. Base da biblioteca montada na linguagem de programação #C: 

 ``` json

namespace ProductLibrary
{
    public class Product
    {
        public int Id { get; }
        public string Name { get; }
        public string Description { get; }

        public Product(int id, string name, string description)
        {
          Id = id;
          Name = name;
          Description = description;
       }
    }
}

 ```


 ``` json

CREATE DATABASE "product-db /*!40100 COLLATE "latint swedish cil" */;
USE 'product-db";

CREATE TABLE 'product' (
       'Id' INT NOT NULL AUTO INCREMENT,
       'Name' TEXT NOT NULL,
       'Description' TEXT NOT NULL,
       INDEX 'Id' ('Id)
)
COLLATE='latin1_ swedish_ci';


INSERT IGNORE INTO product (Id, Name, Description)
VALUES
(1,"Dependency Injection Principles, Practices, and Patterns", "Book by Steven van Deursen and Mark Seemann"),
(2,"Agile Software Development, Principles, Patterns, and Practices", "Book by Robert C. Martin");

 ```

### :mortar_board: Contribuidores

* Luiza Tonatto
* Mateus Miri
* Maria Lina
* Matheus Maschio
* Karine Cagliari
* Inspiração: [tometchy](https://github.com/tometchy/Docker-compose-dotnet-core-and-mysql.git)

