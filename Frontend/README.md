# Frontend - ERP Estoque

<p align="center">
<img src="https://skillicons.dev/icons?i=vue,vite,docker,js&perline=4" />
</p>

Frontend responsável pela interface do sistema ERP Estoque.

A aplicação permite o gerenciamento de:

- Produtos
- Compras
- Vendas
- Controle de estoque

O frontend consome a API REST do backend e fornece uma interface administrativa focada em produtividade e simplicidade.

---

# Tecnologias

- Vue 3
- Vite
- PrimeVue
- PrimeIcons
- Axios
- Docker

---

# Estrutura do Frontend

```txt
Frontend
├── public
├── src
│   ├── api
│   ├── assets
│   ├── components
│   ├── composables
│   ├── layouts
│   ├── pages
│   ├── router
│   ├── services
│   ├── stores
│   ├── utils
│   └── ...
│
├── Dockerfile
├── vite.config.js
├── package.json
└── .env.example
```

---

# Executando o Frontend

## 1. Criar arquivo `.env`

```txt
.env.example → .env
```

---

## 2. Instalar dependências

Dentro do container do frontend:

```bash
docker compose exec frontend sh
```

Depois:

```bash
npm install
```

---

## 3. Executar aplicação

Caso necessário:

```bash
npm run dev
```

---

# Ambiente Local

Frontend local:

```txt
http://localhost:5173
```

---

# Estrutura da Interface

A interface foi construída com foco em:

- Simplicidade
- Organização
- Produtividade
- Facilidade de navegação

---

# Layout

O layout foi inspirado no template:

- Sakai (PrimeVue)

Adaptado para atender as necessidades do projeto ERP.

---

# Integração com API

A comunicação com o backend é realizada via:

- Axios
- API REST

Base URL da API:

```txt
http://localhost:8000/api/v1
```

---

# Funcionalidades

## Produtos

- Cadastro
- Listagem
- Controle de estoque

---

## Compras

- Registro de compras
- Atualização automática do estoque
- Atualização do custo médio

---

## Vendas

- Registro de vendas
- Controle automático de estoque
- Exibição de lucro

---

# Organização do Projeto

## Components

Componentes reutilizáveis da aplicação.

---

## Pages

Páginas principais do sistema.

---

## Services

Camada responsável pelas chamadas HTTP da API.

---

## Router

Gerenciamento de rotas da aplicação.

---

## Stores

Gerenciamento de estado global.

---

# Build de Produção

Gerar build:

```bash
npm run build
```

Preview local da build:

```bash
npm run preview
```

---

# Docker

O frontend pode ser executado através do Docker utilizando o `docker-compose` presente na raiz do projeto.

Subir ambiente:

```bash
docker compose up -d
```

---

# Observações

Projeto desenvolvido para fins educacionais e avaliação técnica.
