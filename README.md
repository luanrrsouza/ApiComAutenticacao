# API de Autenticação com JWT, Prisma e MongoDB

Uma API simples de autenticação que permite cadastro, login e listagem de usuários protegida por JWT.

## 🚀 Tecnologias

Este projeto utiliza as seguintes tecnologias:

- **Node.js** + **Express** - Para a estrutura do servidor;
- **MongoDB** + **Prisma ORM** - Para o banco de dados;
- **JWT** - Para autenticação segura;
- **Bcrypt** - Para criptografia de senhas.

## ⚙️ Como rodar o projeto

### 1️⃣ Clone o repositório

```bash
git clone https://github.com/luanrrsouza/ApiComAutenticacao.git
cd ApiComAutenticacao
```

### 2️⃣ Instale as dependências

```bash
npm install
```

### 3️⃣ Configure o arquivo `.env`

Crie um arquivo `.env` na raiz do projeto e adicione as seguintes variáveis:

```env
DATABASE_URL="sua_string_de_conexao_mongodb"
JWT_SECRET="sua_chave_secreta"
```

### 4️⃣ Gere o Prisma Client

```bash
npx prisma generate
```

### 5️⃣ Rode o projeto

```bash
npm run dev
```

## 🔑 Rotas Disponíveis

| Método | Rota      | Protegida | Descrição                   |
|---------|-----------|------------|--------------------------------|
| `POST`  | `/register` | ❌         | Cadastro de usuário           |
| `POST`  | `/login`   | ❌         | Login e geração de token    |
| `GET`   | `/users`   | ✅         | Listagem de usuários cadastrados |

## ✅ Exemplo de Login

### 🔹 Requisição

```http
POST /login
Content-Type: application/json

{
  "email": "email@exemplo.com",
  "password": "123456"
}
```

### 🔹 Resposta

```json
{
  "token": "seu_token_jwt_aqui"
}
```

---



