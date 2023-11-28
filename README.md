# Aplicação REST Node.js com Express

Esta é uma aplicação simples de servidor REST construída com Node.js e Express. A aplicação permite realizar operações básicas em uma lista de pessoas, como criar, listar, atualizar e excluir.

## Endpoints

### 1. GET /pessoa

Retorna todas as pessoas cadastradas.

Exemplo de requisição:

```bash
curl.exe http://localhost:3001/pessoa
```

### 2. GET /pessoa/:id

Retorna a pessoa cadastrada com o ID especificado.

Exemplo de requisição:

```bash
curl.exe http://localhost:3001/pessoa/1
```

### 3. POST /pessoa

Cria uma nova pessoa com os dados fornecidos no corpo (body) da requisição.

Exemplo de requisição:

```bash
curl.exe -X POST -H "Content-Type: application/json" -d '{"nome": "João", "data_nascimento": "01/01/1990", "email": "joao@gmail.com"}' http://localhost:3001/pessoa
```

### 4. DELETE /pessoa/:id

Exclui a pessoa com o ID especificado.

Exemplo de requisição:

```bash
curl.exe -X DELETE http://localhost:3001/pessoa/1
```

### 5. PATCH /pessoa/:id

Atualiza os campos da pessoa com o ID especificado. Apenas os campos fornecidos no corpo da requisição serão atualizados.

Exemplo de requisição:

```bash
curl.exe -X PATCH -H "Content-Type: application/json" -d '{"nome": "NovoNome"}' http://localhost:3001/pessoa/1
```

## Como executar
1. Certifique-se de ter o Node.js instalado.
2. No terminal, instale as dependências
```bash
npm install
```
3. Execute a aplicação
```bash
node app.js
```

A aplicação estará disponível em http://localhost:3001.