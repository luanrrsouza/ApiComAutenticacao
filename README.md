API de Autenticação com JWT, Prisma e MongoDB
API simples de autenticação, com cadastro, login e listagem de usuários protegida por JWT.

🚀 Tecnologias
Node.js + Express;
MongoDB + Prisma ORM;
JWT para autenticação;
Bcrypt para criptografia de senhas.


⚙️ Como rodar o projeto
Clone o repositório:
bash
Copiar
Editar
git clone https://github.com/luanrrsouza/ApiComAutenticacao.git
cd ApiComAutenticacao
Instale as dependências:
bash
Copiar
Editar
npm install
Configure o arquivo .env (exemplo abaixo):
env
Copiar
Editar
DATABASE_URL="sua_string_de_conexao_mongodb"
JWT_SECRET="sua_chave_secreta"
Gere o Prisma Client:
bash
Copiar
Editar
npx prisma generate
Rode o projeto:
bash
Copiar
Editar
npm run dev
🔑 Rotas
Método	Rota	Protegida	Descrição
POST	/register	❌	Cadastro de usuário
POST	/login	❌	Login e geração de token
GET	/users	✅	Listar usuários cadastrados
✅ Exemplo de login
http
Copiar
Editar
POST /login
Content-Type: application/json

{
  "email": "email@exemplo.com",
  "password": "123456"
}
Resposta:

json
Copiar
Editar
{
  "token": "seu_token_jwt_aqui"
}
