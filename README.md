# BDD DE BIBLIOTECA DE LIVROS ON DOCKER 
<div id="top"></div>

## 💡 Sobre o projeto
Repositório do Trabalho sobre Docker Compose - Sistemas Operacionais/Atitus 02/2022

Esse repositório contém arquivos com uma sede de Banco de Dados MySQL sobre livros, como se fosse uma biblioteca, eles serão visualizados em modo JSON com:
>
> a numeração por ID
>
> as strings relatando o nome dos livros
>
> e as strings com as descrições dos mesmos
>

## :envelope: Conteúdo

* Docker/Docker Compose e Conteiners 🗸

* Ubuntu e Virtual Machines 🗸

* Banco de Dados MySQL 🗸

* Visualização de uma "Biblioteca" com um catálogo de livros 🗸


## 👀 Pré - Requisitos

Frameworks e Bibliotecas necessárias durante o processo:

* [Ubuntu](https://ubuntu.com/download)
* [Docker](https://docs.docker.com/engine/install/ubuntu/)
* [MySQL](https://www.mysql.com/downloads/)
* [Docker Compose](https://docs.docker.com/compose/install/)
* [GitHub](https://github.com/tometchy/Docker-compose-dotnet-core-and-mysql.git)


## 💻 Execução 

1. Baixar os documentos do repositório [tometchy](https://github.com/tometchy/Docker-compose-dotnet-core-and-mysql.git) na sua máquina VM para que a biblioteca fique disponível e os exemplos possam ser visualizados futuramente;


2. Para acessar o sistema em sua máquina, entre na url:   ``` http://localhost:8080/ ```
* Caso não obter um resultado, espere alguns segundos pois o banco de dados MySQL pode não estar 100% inicializado
 
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

   
   
 4. Para rodar o Conteiner e criar as imagens, basta rodar o comando (o --build é utilizado para atualizar quaisquer mudanças): 
 
   
     ```
     docker-compose up -d --build
     ```
     
     
     
 5. Para limpar Conteiners e Redes, basta rodar o comando: 
 
   
     ```
     docker-compose down 
     ```
     
 
 6. Para visualizar os Conteiners da VM, como na imagem, basta rodar o comando: 
 
     ```
     docker ps
     ```
     ![image](https://user-images.githubusercontent.com/106711311/203683938-805d603a-0434-4ed5-b874-dae7454a4a72.png)

 7. Conteúdo do DockerFile:
 
     ![image](https://user-images.githubusercontent.com/106711311/203684422-d3278d54-2b48-424f-abc7-0a645ee4128d.png)



### :mortar_board: Contribuidores

* Luiza Tonatto
* Mateus Miri
* Maria Lina
* Matheus Maschio
* Karine Cagliari
* Inspiração: [tometchy](https://github.com/tometchy/Docker-compose-dotnet-core-and-mysql.git)

