# Trabalho Individual 01 2021.1

A Gestão de Configuração de Software é parte fundamental no curso de GCES, e dominar os conhecimentos de configuração de ambiente, containerização, virtualização, integração e deploy contínuo tem se tornado cada vez mais necessário para ingressar no mercado de trabalho.

Para exercitar estes conhecimentos, você deverá aplicar os conceitos estudados ao longo da disciplina no produto de software contido neste repositório.

O sistema se trata de uma aplicação Web em Typescript, que é composta de:

- Front-end escrito em React (`chat-app`);
- Back-end dividido em três microsserviços:
  - `users-service`: express + ORM
  - `chat-service`: não implementado
  - `api-gateway`: graphql
- 2 Bancos de Dados MySQL 5.7.20 para users-service e chat-service (mesmo este não tendo sido implementado ainda)
  - `phpmyadmin`, como interface para gerenciamento dos bancos de dados

Para executar a aplicação em sua máquina, basta seguir o passo-a-passo descrito no arquivos README das pastas.

- [users-service](./trabalho_individual/users-service/README.md)
- [chat-service](./trabalho_individual/chat-service/README.md).
- [api-gateway](./trabalho_individual/api-gateway/README.md).
- [chat-app](./trabalho_individual/chat-app/README.md).
- [phpmyadmin](./trabalho_individual/phpmyadmin/README.md).

[Mais datalhes](https://github.com/FGA-GCES/Workshop-Docker-Entrega-01)

## Como rodar

### Pré-requisitos
- Possuir o docker e o docker-compose instalados.
- Criar pasta "data" na raiz do projeto Workshop-Docker-Entrega-01 e dentro duas outras "chat-db-data" e "users-db-data" para mapear como volume nos containers msql.

    Comandos:

      mkdir data
      mkdir data/chat-db-data
      mkdir data/users-db-data

### Serviços
#### Iniciando 
  
  Para subir os serviços:
    
    docker-compose up
  
  Aguarde os serviços subirem e acesse:

    http://localhost:7001
  
#### Parando
  Utilize o comando abaixo para parar os serviços:

    docker-compose stop
  
#### Apagando 
  Para apagar as containers, imagens e networks criados, utilize:

    docker-compose down
  
  
