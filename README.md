# Gestao_agencia_turismo
Desafio de 5 dias
# Projeto Gerenciamento de Pacotes Turísticos

## Descrição
Aplicação web full stack para gerenciamento de pacotes turísticos, permitindo cadastro e gerenciamento de destinos, atividades, usuários, login com autenticação JWT e reservas.

---

## Tecnologias Utilizadas

- **Backend:**
  - Node.js
  - Express.js
  - Sequelize ORM (SQLite/MySQL)
  - JWT para autenticação
  - bcrypt para criptografia de senhas

- **Frontend:**
  - React
  - React Router
  - Axios para requisições HTTP

- **Outras Ferramentas:**
  - Postman para testes da API
  - Visual Studio Code

---

## Instalação e Execução

### Pré-requisitos

- Node.js instalado (versão 16+ recomendada)
- npm ou yarn

### Backend

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/seu-projeto.git
Entre na pasta backend e instale as dependências:

bash
Copiar
Editar
cd backend
npm install
Configure as variáveis de ambiente criando um arquivo .env com as seguintes variáveis:

ini
Copiar
Editar
JWT_SECRET=seuSegredoAqui
DATABASE_URL=sqlite://./database.sqlite
Inicie o servidor backend:

bash
Copiar
Editar
npm start
O backend estará rodando em http://localhost:3001

Frontend
Entre na pasta frontend:

bash
Copiar
Editar
cd frontend
Instale as dependências:

bash
Copiar
Editar
npm install
Inicie o servidor frontend:

bash
Copiar
Editar
npm start
A aplicação estará disponível em http://localhost:3000

Estrutura do Projeto
Backend
bash
Copiar
Editar
backend/
├── config/           # Configurações do banco de dados e ambiente
├── controllers/      # Funções para lidar com as requisições
├── middleware/       # Middlewares, ex: autenticação JWT
├── models/           # Modelos Sequelize (Usuário, Destino, Atividade, Reserva, etc)
├── routes/           # Rotas da API (ex: usuários, atividades, reservas)
├── server.js         # Arquivo principal para iniciar o servidor
└── .env              # Variáveis de ambiente (não versionado)
Frontend
bash
Copiar
Editar
frontend/src/
├── api.js            # Configuração Axios para comunicação com backend
├── components/       # Componentes React reutilizáveis
├── context/          # Context API para estado global (ex: autenticação)
├── pages/            # Páginas React (Login, ListaUsuarios, etc)
├── App.js            # Componente principal com rotas
└── index.js          # Entrada da aplicação React
Funcionamento Básico
O usuário faz login e recebe um token JWT.

O token é armazenado no localStorage e usado para autenticar requisições.

Usuários autenticados podem criar, editar, deletar destinos, atividades e reservas.

Funcionários usam o sistema para gerenciar reservas de atividades turísticas.

Filtros estão disponíveis para pesquisa de atividades por destino, data e preço.

Testes
Use o Postman para testar endpoints da API, especialmente as que exigem autenticação via token JWT.

Para autenticar, envie no header:

makefile
Copiar
Editar
Authorization: Bearer <seu_token_aqui>
