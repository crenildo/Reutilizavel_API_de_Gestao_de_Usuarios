API REST de gestão de usuários com autenticação JWT

# 📌 Gestão de Usuários – API REST

API REST para **gestão de usuários**, desenvolvida em **Java com Spring Boot**, seguindo boas práticas de arquitetura em camadas, autenticação com **JWT** e persistência de dados com **JPA/Hibernate**.

O projeto foi pensado para ser **escalável**, desacoplado do front-end e facilmente integrável com outras aplicações ou APIs.

---

## 🧠 Visão Geral do Projeto

Esta API permite:

* Criar usuários
* Atualizar dados de usuários
* Buscar usuários
* Remover usuários
* Autenticar usuários via **JWT**
* Controlar acesso com **roles** (ex: ADMIN e USUARIO)

A aplicação expõe endpoints REST que podem ser consumidos por:

* Front-end web
* Aplicativos mobile
* Outras APIs (arquitetura desacoplada)

---

## 🏗️ Arquitetura

O projeto segue uma **arquitetura em camadas**, baseada em boas práticas do Spring:

```
Controller → Service → Repository → Banco de Dados
```

### Camadas:

* **Controller**: recebe requisições HTTP e retorna respostas com status HTTP adequados
* **Service**: contém a regra de negócio
* **Repository**: acesso e persistência de dados
* **DTOs**: transferência de dados entre camadas
* **Security**: autenticação e autorização com JWT

---

## 🛠️ Tecnologias Utilizadas

* **Java**
* **Spring Boot**
* **Spring Security**
* **JWT (JSON Web Token)**
* **Spring Data JPA**
* **Hibernate**
* **MySQL**
* **Flyway** (versionamento de banco de dados)
* **Maven**
* **Postman / Insomnia** (testes de endpoints)

---

## 🔐 Autenticação e Segurança

A autenticação é feita via **JWT**:

1. O usuário realiza login
2. A API gera um token JWT
3. O token deve ser enviado nas próximas requisições
4. O acesso aos endpoints é controlado por **roles**

### Roles disponíveis:

* **ADMIN**: acesso completo
* **USUARIO**: acesso restrito

---

## 🔄 Endpoints Principais

### Autenticação

* `POST /auth/login`

### Usuários

* `POST /usuarios` → criar usuário
* `GET /usuarios` → listar usuários
* `GET /usuarios/{id}` → buscar usuário
* `PUT /usuarios/{id}` → atualizar usuário
* `PATCH /usuarios/{id}` → atualização parcial
* `DELETE /usuarios/{id}` → remover usuário

Todos os endpoints retornam **status HTTP adequados** (`200`, `201`, `204`, `400`, `401`, `403`, `404`).

---

## 🗄️ Banco de Dados

* Banco relacional **MySQL**
* Entidade principal: **Usuário**
* Uso de **Enums** para:

  * Status do usuário (ATIVO, INATIVO, BLOQUEADO)
  * Tipo de usuário (ADMIN, USUARIO)
* Versionamento do schema com **Flyway**

---

## 🚀 Como Executar o Projeto

1. Clone o repositório
2. Configure o banco de dados MySQL
3. Ajuste as variáveis no `application.properties`
4. Execute a aplicação
5. Teste os endpoints com Postman ou Insomnia

---

## 📌 Objetivo do Projeto

Este projeto foi desenvolvido com foco em:

* Aprendizado prático de **backend Java**
* Aplicação de conceitos de **API REST**
* Boas práticas de organização e arquitetura
* Preparação para ambientes reais de desenvolvimento

---

## 📈 Possíveis Evoluções

* Testes automatizados com JUnit
* Paginação e filtros
* Logs e monitoramento
* Deploy em ambiente de nuvem
* Integração com outras APIs

---

## 👨‍💻 Autor Crenildo

Projeto desenvolvido para fins de estudo e aprimoramento em **Java Backend**.

