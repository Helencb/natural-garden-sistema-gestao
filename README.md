# Sistema de Gestão — Natural Garden

Sistema web de gestão para a **Natural Garden**, loja de plantas e serviços de jardinagem localizada em Assis - SP, desenvolvido como Projeto Integrador Extensionista (PIE) do curso de Análise e Desenvolvimento de Sistemas.

## Sobre a empresa parceira

A **Natural Garden** (R. Cap. Francisco Rodrigues García, 1093, Centro, Assis - SP), sob responsabilidade de **Dailto Teodoro Batista**, vende plantas, vasos e insumos de jardinagem, além de prestar serviços de poda, paisagismo e manutenção de jardins. Hoje a loja controla vendas, clientes, agenda de serviços e finanças de forma manual (caderno, agenda de papel e WhatsApp), sem nenhum sistema informatizado.

Este projeto tem como objetivo digitalizar essa operação, começando pelo essencial: cadastro de clientes e produtos com controle de estoque, registro de vendas, agenda de jardinagem sem conflitos de horário e um relatório financeiro simples.

Documento de Visão completo disponível em [`/docs`](./docs).

## Funcionalidades do MVP

- Autenticação de usuários (administrador / vendedor)
- Cadastro e busca de clientes
- Cadastro de produtos com controle de estoque
- Registro de vendas com baixa automática de estoque
- Agenda de serviços de jardinagem com verificação de conflito de horário
- Cadastro de despesas e relatório financeiro mensal (receita x despesa)

## Stack Tecnológica

| Camada | Tecnologia |
|---|---|
| Backend | Java 17+ / Spring Boot |
| Frontend | React |
| Banco de Dados | MySQL |
| ORM | Spring Data JPA / Hibernate |
| Autenticação | JWT + hash bcrypt |
| Versionamento | Git + GitHub |
| Deploy | Render/Railway (backend) + Vercel/Netlify (frontend) |

## Estrutura do Repositório

```
natural-garden-sistema-gestao/
├── docs/          # Documento de Visão (PDF) e demais artefatos de documentação
├── backend/       # API REST em Java + Spring Boot
├── frontend/      # Aplicação React
├── database/      # Scripts SQL (criação de tabelas, dados iniciais)
├── .env.example   # Modelo de variáveis de ambiente
├── .gitignore
└── README.md
```

## Como Instalar e Rodar

### Pré-requisitos

- Java 17 ou superior
- Node.js 18 ou superior
- MySQL 8 (local ou em nuvem)
- Maven (ou o wrapper `mvnw` incluso no projeto backend)

### 1. Clonar o repositório

```bash
git clone https://github.com/<seu-usuario>/natural-garden-sistema-gestao.git
cd natural-garden-sistema-gestao
```

### 2. Configurar variáveis de ambiente

Copie o arquivo de exemplo e preencha com seus dados locais:

```bash
cp ..env.example .env
```

### 3. Banco de dados

Crie o banco no MySQL:

```sql
CREATE DATABASE natural_garden_db;
```

Se houver scripts em `/database`, execute-os para criar as tabelas iniciais.

### 4. Backend (Spring Boot)

```bash
cd backend
./mvnw spring-boot:run
```

A API sobe por padrão em `http://localhost:8080`.

### 5. Frontend (React)

```bash
cd frontend
npm install
npm run start
```

A aplicação sobe por padrão em `http://localhost:3000`.

## Autoria

Projeto desenvolvido individualmente por **Helen Cristina Batista**, como parte do Projeto Integrador Extensionista (PIE) — Análise e Desenvolvimento de Sistemas.