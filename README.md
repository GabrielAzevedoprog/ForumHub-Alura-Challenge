# 💬 ForumHub API

<div align="center">
  <img src="https://img.shields.io/badge/status-concluído-brightgreen" alt="Status: Concluído" />
</div>

---

## 📖 Sobre o Projeto

**ForumHub** é uma API REST desenvolvida como parte do **Alura Challenges - Oracle Next Education (ONE)**.
O projeto simula o backend de um fórum de discussões, permitindo operações completas de **CRUD de tópicos** e **autenticação de usuários** via JWT.

Esta aplicação foi um exercício prático para consolidar conhecimentos em **Java com Spring Boot**, abordando:

* Criação de endpoints RESTful
* Integração com banco de dados usando Spring Data JPA e Flyway
* Validações
* Autenticação e segurança com Spring Security + JWT

---

## ✨ Funcionalidades

A API fornece os seguintes endpoints:

| Método | Endpoint        | Descrição                                       |
| ------ | --------------- | ----------------------------------------------- |
| POST   | `/login`        | Autentica o usuário e retorna um token JWT.     |
| POST   | `/topicos`      | Cria um novo tópico.                            |
| GET    | `/topicos`      | Lista os tópicos ativos com paginação.          |
| GET    | `/topicos/{id}` | Retorna os detalhes de um tópico específico.    |
| PUT    | `/topicos/{id}` | Atualiza o título e/ou a mensagem de um tópico. |
| DELETE | `/topicos/{id}` | Realiza a exclusão lógica do tópico.            |

---

## 🛠️ Tecnologias Utilizadas

* ✅ **Java 17+**
* ✅ **Spring Boot**
* ✅ **Spring Data JPA**
* ✅ **MySQL**
* ✅ **Flyway**
* ✅ **Spring Security**
* ✅ **JWT (JSON Web Tokens)**
* ✅ **Lombok**
* ✅ **Jackson Databind**
* ✅ **Maven**

---

## 🚀 Como Executar o Projeto

### ✅ Pré-requisitos

* Java 17 ou superior
* Maven 3.8+
* MySQL Server

---

### 1. Clone o repositório

---

### 2. Configure o banco de dados

1. Crie um banco no MySQL com o nome `forumhub_db`.

2. Abra o arquivo `src/main/resources/application.properties` e insira suas credenciais:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/forumhub_db
spring.datasource.username=seu_usuario
spring.datasource.password=sua_senha

spring.jpa.hibernate.ddl-auto=validate
spring.jpa.show-sql=true
```

> ⚠️ O Flyway se encarregará da criação das tabelas automaticamente ao rodar a aplicação.

---

### 3. Execute a aplicação

Você pode rodar pela linha de comando com:

```bash
mvn spring-boot:run
```

A aplicação estará disponível em:
📍 `http://localhost:8080`

---

## 🔒 Autenticação

Para acessar os endpoints protegidos, é necessário:

1. Realizar login via `/login` passando email e senha válidos.
2. Receber o token JWT no retorno.
3. Enviar o token no header das próximas requisições:

```http
Authorization: Bearer SEU_TOKEN
```

---

## 📄 Licença

Este projeto está licenciado sob a [MIT License](LICENSE).

