## 📌 Visão geral do sistema

**Sistema de Gestão de Usuários**

---

## 👤 Usuário

* **Tipo:** Entidade principal do sistema
* **No Java:** classe normal (ex.: `User`)
* **No banco:** tabela `users`
* **Representação no banco:** entidade mapeada (JPA Entity)

### Dados básicos do usuário

* id
* nome
* email
* senha
* data de criação
* data de atualização

---

## 🔐 Papel do usuário (Role)

* **Tipo:** `enum`
* **Exemplos:**

  * ADMIN
  * USER

📌 Uso no mundo real:

* define permissões
* controla o que cada usuário pode fazer

---

## 🚦 Status do usuário

* **Tipo:** `enum`
* **Exemplos:**

  * ATIVO
  * INATIVO
  * BLOQUEADO

📌 Uso:

* controle de acesso
* desativação sem apagar dados

---

## 🗄️ Banco de Dados

* Banco relacional (PostgreSQL ou MySQL)
* Estrutura controlada por **Flyway**
* O banco “não muda na mão”, tudo versionado

### Flyway

* controla criação de tabelas
* controla alterações de estrutura
* garante consistência entre ambientes

---

## 🔁 Operações (CRUD com sentido real)

### Criar usuário

* cadastro inicial
* criado como ATIVO
* role padrão USER

### Consultar usuário

* admin vê todos
* usuário vê apenas o próprio perfil

### Atualizar usuário

* usuário atualiza dados pessoais
* admin atualiza status ou role

### Remover usuário

* remoção lógica (status INATIVO)
* mantém histórico

---

## 📦 DTOs

* **Request DTO:** entrada de dados
* **Response DTO:** saída de dados

📌 Uso:

* não expor entidade
* controlar dados sensíveis (ex.: senha)

---

## 🧱 Camadas do sistema

* Controller → recebe requisições
* Service → regras de negócio
* Repository → acesso ao banco

---

## 🧠 POO aplicada (sem forçar)

* Encapsulamento → atributos privados
* Enum → valores fixos (status, role)
* Abstração → possível classe base (ex.: id, datas)
* Polimorfismo → sobrescrita simples, se necessário

---

## ⚠️ Tratamento básico

* validação de dados
* respostas HTTP adequadas
* mensagens de erro simples

---

## 🎯 Por que isso atende a vaga?

✔ Java + POO
✔ Spring Boot
✔ Hibernate / JPA
✔ REST
✔ Banco relacional
✔ Flyway (diferencial)
✔ Projeto simples e profissional

---

## 🧠 Frase pronta (guarda essa)

> “É um sistema de gestão de usuários, comum em aplicações reais, com controle de acesso, status e persistência versionada via Flyway.”