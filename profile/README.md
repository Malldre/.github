# Malldre - SaaS de Gestão Logística

Malldre é um **SaaS completo de gestão logística**, originalmente desenvolvido como um **WMS acadêmico**, que evoluiu para oferecer funcionalidades avançadas de **controle de armazéns, estoques e operações logísticas**. O sistema é modular, extensível e cloud-ready, utilizando **serverless architecture** na AWS.

---

## 🔹 Funcionalidades Principais

* **Controle de Usuários e Multiempresa (SaaS)**

  * Autenticação via **Cognito**
  * Perfis e permissões de acesso por empresa
* **Gestão de Estoque e Armazenagem**

  * Produtos, fornecedores e grupos de produtos
  * Controle de cargas e pacotes
  * Prateleiras, racks e tipos de prateleiras (herdado do WMS acadêmico)
  * Organização 3D de armazéns (Zonas, Colunas, Fileiras)
* **Transações Operacionais**

  * Entrada e saída de cargas
  * Movimentação entre prateleiras e racks
* **Recursos SaaS Avançados**

  * Dashboards e relatórios de BI
  * Integrações com ERPs e marketplaces
  * Suporte a múltiplos armazéns e clientes
  * APIs abertas para integração externa
* **Cloud & Serverless**

  * API baseada em **AWS Lambda**
  * JWT Authorizer via **Cognito**
  * CI/CD com **GitHub Actions**
  * Infraestrutura gerenciada via **Terraform**

---

## 🔹 Arquitetura

* **Backend/API**

  * **Node.js 22.xx**
  * **TypeScript**
  * **Express.js**
  * **Prisma ORM** para PostgreSQL
* **Banco de Dados**

  * PostgreSQL (hosted, ex: Railway ou AWS RDS)
  * Modelos: Usuário, Empresa, Produto, Carga, Prateleira, Rack, Transação
* **Infraestrutura**

  * **Serverless**: AWS Lambda, API Gateway, S3, Cognito
  * IaC com Terraform
* **Autenticação e Multitenancy**

  * JWT via **Cognito Authorizer**
  * Tokens armazenados em cookies para sessões persistentes
  * Isolamento de dados por empresa/cliente

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
