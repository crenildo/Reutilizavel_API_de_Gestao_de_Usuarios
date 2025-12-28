## 🔹 Spring Boot (base de tudo)

* **O que é:** framework que facilita criar aplicações Java
* **No projeto:**

  * sobe o servidor
  * configura tudo automaticamente
  * integra REST, JPA, Hibernate, Flyway
* **Por que usar:** menos configuração, mais foco no negócio

---

## 🔹 REST

### O que é

* Um **padrão de comunicação** entre sistemas
* Usa HTTP (GET, POST, PUT, DELETE)
* Muito usado em APIs

### O que ele faz no projeto

* Permite que o **front-end converse com o back-end**
* Define como os dados entram e saem do sistema

### Exemplo no mundo real

* Front manda um pedido para criar usuário
* Back responde com os dados criados

> “REST define como o sistema conversa com o mundo externo.”

---

## 🔹 JPA (Java Persistence API)

### O que é

* Uma **especificação**
* Define regras para trabalhar com banco de dados em Java
* Não é uma implementação, é um contrato

### O que ele faz no projeto

* Define como:

  * classes viram tabelas
  * atributos viram colunas
  * relacionamentos funcionam
* Permite trabalhar com banco usando **objetos**, não SQL direto o tempo todo

> “JPA define como o Java se comunica com o banco de dados.”

---

## 🔹 Hibernate

### O que é

* Uma **implementação do JPA**
* É quem realmente faz o trabalho pesado

### O que ele faz no projeto

* Executa as operações no banco:

  * salvar
  * buscar
  * atualizar
  * remover
* Converte:

  * objetos Java → registros no banco
  * registros no banco → objetos Java

👉 Relação clara:

* JPA = regra
* Hibernate = quem executa

👉 Frase simples:

> “Hibernate implementa o JPA e faz a persistência acontecer.”

---

## 🔹 Flyway (o “Fully Array” que você mencionou 😉)

### O que é

* Ferramenta de **versionamento do banco de dados**
* Controla a evolução da estrutura do banco

### O que ele faz no projeto

* Cria tabelas
* Altera colunas
* Mantém histórico das mudanças
* Garante que todo mundo use o **mesmo banco**

### Como ele é usado

* Você cria arquivos de migração
* Cada mudança no banco vira um arquivo
* O Flyway executa na ordem correta

👉 Importante:

* Você **não altera o banco na mão**
* Tudo passa pelo Flyway

👉 Frase profissional:

> “O Flyway garante consistência e controle de versão do banco.”

---

## 🔹 Hibernate + JPA + Flyway (juntos)

No projeto real, funciona assim:

1️⃣ Flyway cria/atualiza o banco
2️⃣ JPA define o mapeamento
3️⃣ Hibernate executa as operações
4️⃣ REST expõe tudo para o front
5️⃣ Spring Boot integra tudo

---

## 🔹 Resumo rápido

* **REST:** comunicação com o front
* 
* **JPA:** define regras de persistência
* 
* **Hibernate:** executa persistência
* 
* **Flyway:** controla mudanças no banco
* 
* **Spring Boot:** junta tudo e sobe a aplicação

---

## No projeto, o Spring Boot facilita a configuração, o REST expõe a API, o JPA define o mapeamento com o banco, o Hibernate executa a persistência e o Flyway controla a evolução da estrutura do banco.

