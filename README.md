# User Registration and Login API

Esta é uma API de registro e login de usuários construída com Node.js, Express, e Prisma ORM, utilizando o MongoDB como banco de dados. A API foi implementada com suporte a CORS e foi implantada no Vercel.

## Tecnologias Utilizadas

- **Node.js**: Plataforma de desenvolvimento para executar código JavaScript no servidor.
- **Express**: Framework web para Node.js, utilizado para criar o servidor e gerenciar rotas.
- **Prisma ORM**: ORM (Object-Relational Mapping) utilizado para interagir com o banco de dados MongoDB.
- **MongoDB**: Banco de dados NoSQL utilizado para armazenar as informações dos usuários.
- **Vercel**: Plataforma de hospedagem utilizada para o deploy da API.

## Estrutura do Projeto

O projeto contém os seguintes arquivos principais:

- `app.js`: Arquivo principal que contém a configuração do servidor e as rotas da API.
- `.env`: Arquivo de configuração para variáveis de ambiente, onde é especificada a URL do banco de dados.

## Funcionalidades

A API oferece as seguintes funcionalidades:

### Criar um novo usuário

**Endpoint**: `POST /usuarios`

- **Descrição**: Cria um novo usuário no banco de dados.
- **Requisição**: 
  - Body (JSON):
    ```json
    {
      "nickname": "seuNickname",
      "email": "seuEmail@example.com",
      "senha": "suaSenha"
    }
    ```
- **Respostas**:
  - `201 Created`: Retorna o objeto do usuário criado.
  - `400 Bad Request`: Se o nickname ou o email já estiverem em uso.
  - `500 Internal Server Error`: Se ocorrer um erro durante a criação do usuário.

### Login do usuário

**Endpoint**: `POST /usuarios/login`

- **Descrição**: Busca um usuário no banco de dados com base no email e na senha fornecidos.
- **Requisição**:
  - Body (JSON):
    ```json
    {
      "email": "seuEmail@example.com",
      "senha": "suaSenha"
    }
    ```
- **Respostas**:
  - `200 OK`: Retorna o objeto do usuário encontrado.
  - `404 Not Found`: Se não houver usuário com o email e a senha fornecidos.
  - `500 Internal Server Error`: Se ocorrer um erro durante a busca do usuário.

## Instalação

Para rodar esta API localmente, siga os passos abaixo:

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/seu-usuario/seu-repositorio.git
   cd seu-repositorio
