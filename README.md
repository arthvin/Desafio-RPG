# Sistema de Gerenciamento de RPG

Um sistema completo para gerenciamento de personagens e itens mágicos em jogos de RPG, desenvolvido com TypeScript e Node.js.

## ✨ Funcionalidades

### 📜 Personagens
- Criar personagem
- Listar personagens
- Buscar personagem por ID
- Atualizar nome de aventureiro
- Remover personagem
- Adicionar item mágico ao personagem
- Remover item mágico do personagem
- Listar itens mágicos do personagem
- Buscar amuleto do personagem

### 🧪 Itens Mágicos
- Criar item mágico
- Listar itens mágicos
- Buscar item mágico por ID
- Atualizar item mágico
- Remover item mágico

## ⚔️ Regras de Negócio

### Personagens
- Atributos:
  - ID único
  - Nome
  - Nome Aventureiro
  - Classe (Guerreiro, Mago, Arqueiro, Ladino ou Bardo)
  - Nível
  - Lista de Itens Mágicos
  - Força (base + bônus dos itens)
  - Defesa (base + bônus dos itens)
- Na criação, o jogador deve distribuir 10 pontos entre Força e Defesa base.
- Cada personagem pode ter **apenas um Amuleto**.

### Itens Mágicos
- Atributos:
  - ID único
  - Nome
  - Tipo (Arma, Armadura ou Amuleto)
  - Força
  - Defesa
- Restrições:
  - Armas: Defesa = 0
  - Armaduras: Força = 0
  - Amuletos: podem ter Força e Defesa
  - Força e Defesa máximas: 10
  - Não é permitido item com Força e Defesa iguais a 0

## 🛠️ Tecnologias

- **TypeScript**
- **Node.js**
- **Express.js**
- **Swagger** (documentação da API)

## 🚀 Instalação

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/rpg-management-system.git
   cd rpg-management-system
   ```

2. Instale as dependências:
   ```bash
   npm install
   ```

3. Compile o TypeScript:
   ```bash
   npm run build
   ```

4. Inicie a aplicação:
   ```bash
   npm start
   ```

Para desenvolvimento com hot-reload:
```bash
npm run dev
```

## 📡 Endpoints da API

Servidor disponível em: `http://localhost:3000`  
Documentação via Swagger: `http://localhost:3000/api-docs`

### Personagens
- `GET /api/characters` – Listar personagens
- `GET /api/characters/:id` – Buscar por ID
- `POST /api/characters` – Criar personagem
- `PATCH /api/characters/:id/adventurer-name` – Atualizar nome de aventureiro
- `DELETE /api/characters/:id` – Remover personagem
- `GET /api/characters/:characterId/items` – Listar itens do personagem
- `GET /api/characters/:characterId/amulet` – Buscar amuleto do personagem
- `POST /api/characters/:characterId/items/:itemId` – Adicionar item mágico
- `DELETE /api/characters/:characterId/items/:itemId` – Remover item mágico

### Itens Mágicos
- `GET /api/magic-items` – Listar itens mágicos
- `GET /api/magic-items/:id` – Buscar por ID
- `POST /api/magic-items` – Criar item mágico
- `PUT /api/magic-items/:id` – Atualizar item mágico
- `DELETE /api/magic-items/:id` – Remover item mágico

## 🗂️ Estrutura do Projeto

```
.
├── dist/                  # Código compilado
├── src/                   # Código-fonte
│   ├── config/            # Configurações
│   ├── controllers/       # Controladores
│   ├── models/            # Interfaces e modelos
│   ├── routes/            # Rotas da API
│   ├── services/          # Regras de negócio
│   ├── utils/             # Funções utilitárias
│   └── index.ts           # Ponto de entrada
├── package.json           # Dependências e scripts
├── tsconfig.json          # Configuração do TypeScript
└── README.md              # Documentação do projeto
```

## 📄 Licença

Este projeto está licenciado sob a licença ISC.
