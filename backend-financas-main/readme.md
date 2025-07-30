# Backend Finanças - GranaGo

Backend para o aplicativo GranaGo, desenvolvido com Node.js, Express, Prisma e SQLite.

## 🚀 Tecnologias

- Node.js
- Express
- Prisma ORM
- SQLite
- TypeScript
- JWT para autenticação
- bcryptjs para criptografia

## 📋 Pré-requisitos

- Node.js (versão 16 ou superior)
- npm ou yarn

## 🔧 Instalação

1. Clone o repositório:

```bash
git clone <url-do-repositorio>
cd backend-financas
```

2. Instale as dependências:

```bash
npm install
# ou
yarn install
```

3. Configure as variáveis de ambiente:

```bash
cp .env.example .env
```

Edite o arquivo `.env` com suas configurações:

```env
DATABASE_URL="file:./dev.db"
JWT_SECRET="sua-chave-secreta-aqui"
PORT=3333
```

4. Execute as migrações do banco de dados:

```bash
npx prisma migrate dev
```

5. Gere o cliente Prisma:

```bash
npx prisma generate
```

## 🏃‍♂️ Como executar

### Desenvolvimento

```bash
npm run dev
# ou
yarn dev
```

O servidor estará rodando em `http://localhost:3333`

## 📊 Banco de Dados

O projeto usa SQLite com Prisma ORM. O arquivo do banco está em `prisma/dev.db`.

### Estrutura do Banco

- **Users**: Tabela de usuários
- **Receives**: Tabela de receitas/despesas

### Comandos úteis do Prisma

```bash
# Visualizar o banco de dados
npx prisma studio

# Resetar o banco
npx prisma migrate reset

# Ver status das migrações
npx prisma migrate status
```

## 🔌 Endpoints da API

### Autenticação

- `POST /users` - Criar usuário
- `POST /sessions` - Fazer login

### Receitas/Despesas

- `GET /receives` - Listar receitas/despesas
- `POST /receives` - Criar receita/despesa
- `PUT /receives/:id` - Atualizar receita/despesa
- `DELETE /receives/:id` - Deletar receita/despesa

## 📝 Scripts Disponíveis

- `npm run dev` - Executa o servidor em modo desenvolvimento
- `npm run build` - Compila o projeto TypeScript
- `npm start` - Executa o servidor em produção

## 🤝 Contribuição

1. Faça um fork do projeto
2. Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.
