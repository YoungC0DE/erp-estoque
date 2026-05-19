# Backend - ERP Estoque

<p align="center">
<img src="https://skillicons.dev/icons?i=php,laravel,postgres,redis,docker&perline=5" />
</p>

Backend responsável pela API REST do sistema ERP Estoque.

A aplicação gerencia:

- Produtos
- Compras
- Vendas
- Controle de estoque
- Cálculo de custo médio
- Cálculo de lucro

A API segue o padrão REST utilizando versionamento de rotas:

```txt
/api/v1
```

---

# Tecnologias

- Laravel 12
- PHP 8.4
- PostgreSQL
- Redis
- Docker

---

# Estrutura do Backend

```txt
Backend
├── app
│   ├── Http
│   ├── Models
│   ├── Services
│   ├── Rules
│   └── ...
│
├── bootstrap
├── config
├── database
│   ├── migrations
│   ├── seeders
│   └── factories
│
├── routes
├── storage
├── tests
├── Dockerfile
├── composer.json
└── .env.example
```

---

# Executando o Backend

## 1. Criar arquivo `.env`

```txt
.env.example → .env
```

---

## 2. Instalar dependências

Dentro do container da API:

```bash
docker compose exec api bash
```

Depois:

```bash
composer install -o
```

---

## 3. Gerar chave da aplicação

```bash
php artisan key:generate
```

---

## 4. Executar migrations

```bash
php artisan migrate
```

---

# Documentação da API

A documentação é gerada automaticamente utilizando:

- Scramble

Ambiente local:

```txt
http://localhost:8000/docs
```

A documentação contém:

- Endpoints
- Payloads
- Parâmetros
- Responses
- Exemplos de requisição

---

# Estrutura da API

A API utiliza:

- Controllers
- Form Requests
- Services
- Models
- Resources

---

# Regras de Negócio

## Compras

Ao registrar uma compra:

- O estoque do produto é incrementado
- O custo médio do produto é recalculado automaticamente

---

## Vendas

Ao registrar uma venda:

- O estoque do produto é decrementado
- O lucro é calculado automaticamente com base no custo médio atual

---

## Controle de Estoque

A API impede operações inválidas como:

- Venda sem estoque disponível
- Valores inválidos
- Dados inconsistentes

---

# Versionamento

As rotas seguem o padrão:

```txt
/api/v1
```

Exemplo:

```txt
/api/v1/products
```

---

# Testando a API

## Insomnia / Postman

Importe o arquivo:

```txt
import_file_endpoints_insomnia.json
```

Localizado na raiz do projeto.

---

# Variáveis do Insomnia

Caso utilize Scratch Pad:

```json
{
  "url_base_local": "http://localhost:8000/api/v1",
  "url_base_hml": "https://erp_estoque.onrender.com/api/v1"
}
```

---

# Redis

O Redis é utilizado para:

- Cache
- Filas
- Performance de operações

---

# Padrões Utilizados

- REST API
- Versionamento de rotas
- Separação de responsabilidades
- Validação com Form Requests
- Estrutura modular
- Clean Code

---

# Ambiente Local

API local:

```txt
http://localhost:8000
```

Documentação:

```txt
http://localhost:8000/docs
```

---

# Observações

Projeto desenvolvido para fins educacionais e avaliação técnica.
