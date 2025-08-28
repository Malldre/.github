# Malldre -  Warehouse Management System (WMS)

![Malldre Logo](link_para_logo_opcional)

Malldre é um **sistema de gerenciamento de armazéns acadêmico** (WMS), desenvolvido como projeto interdisciplinar, com foco em armazenagem de produtos, controle de prateleiras, racks, cargas e transações operacionais. O sistema foi projetado para ser **modular, extensível e cloud-ready**, utilizando **serverless architecture** na AWS e **TypeScript** para APIs e funções Lambda.

---

## 🔹 Funcionalidades Principais

* **Controle de Usuários**

  * Autenticação via **Cognito**
  * Perfis e permissões de acesso
* **Gerenciamento de Estoque**

  * Produtos, fornecedores e grupos de produtos
  * Controle de cargas e pacotes
  * Prateleiras, racks e tipos de prateleiras
  * Organização 3D de armazéns (Zonas, Colunas, Fileiras)
* **Transações Operacionais**

  * Entrada e saída de cargas
  * Movimentação entre prateleiras e racks
* **Fluxo Operacional**

  * Registro completo de operações de armazenagem
  * Controle de empilhamento e capacidade de locações
* **Cloud & Serverless**

  * API baseada em **AWS Lambda**
  * JWT Authorizer via **Cognito**
  * CI/CD com **GitHub Actions**
  * Infraestrutura gerenciada via **Terraform**

---

## 🔹 Arquitetura

* **Backend/API**

  * **Node.js 20.19**
  * **TypeScript**
  * **Express.js**
  * **Prisma ORM** para PostgreSQL
* **Banco de Dados**

  * PostgreSQL (hosted, ex: Railway ou AWS RDS)
  * Modelos: Usuário, Produto, Carga, Prateleira, Rack, Transação
* **Infraestrutura**

  * **Serverless**: AWS Lambda, API Gateway, S3, Cognito
  * IaC com Terraform
* **Autenticação**

  * JWT via **Cognito Authorizer**
  * Tokens armazenados em cookies para sessões persistentes

---

## 🔹 Estrutura do Projeto

```
malldre/
├── lambda-functions/        # Funções Lambda serverless
├── prisma/                  # Models e migrations do Prisma
├── src/
│   ├── controllers/         # Lógica de endpoints
│   ├── services/            # Regras de negócio
│   ├── routes/              # Rotas da API
│   └── validators/          # Validações de requisições
├── terraform/               # Scripts de IaC
├── tests/                   # Testes unitários e de integração
├── package.json
└── README.md
```

---

## 🔹 Tecnologias

* **Linguagens**: TypeScript, SQL
* **Banco de Dados**: PostgreSQL
* **ORM**: Prisma
* **API**: Node.js + Express
* **Cloud**: AWS Lambda, API Gateway, Cognito, S3
* **Infraestrutura**: Terraform
* **CI/CD**: GitHub Actions
* **Testes**: Vitest

---

## 🔹 Instalação e Uso

1. **Clone o repositório**

```bash
git clone https://github.com/usuario/malldre.git
cd malldre
```

2. **Instale dependências**

```bash
npm install
```

3. **Configure variáveis de ambiente**

```env
DATABASE_URL=postgresql://usuario:senha@host:port/banco
COGNITO_CLIENT_ID=xxx
COGNITO_CLIENT_SECRET=xxx
COGNITO_ISSUER_URL=xxx
```

4. **Migrate e seed do banco**

```bash
npx prisma migrate dev
npx prisma db seed
```

5. **Rodar localmente**

```bash
npm run dev
```

---

## 🔹 Testes

```bash
npm run test
```

Utiliza **Vitest** para testes unitários e de integração.

---

## 🔹 Contribuição

1. Fork este repositório
2. Crie sua branch (`git checkout -b feature/nova-funcionalidade`)
3. Commit suas alterações (`git commit -am 'Adicionar nova funcionalidade'`)
4. Push para a branch (`git push origin feature/nova-funcionalidade`)
5. Abra um Pull Request

---

## 🔹 Referências e Recursos

* [Documentação do Prisma](https://www.prisma.io/docs/)
* [AWS Serverless](https://aws.amazon.com/serverless/)
* [Terraform](https://www.terraform.io/)
* [Vitest](https://vitest.dev/)

---

## 🔹 Licença

MIT License © 2025 Adriano Vitoriano da Silva
