# Entidades

## Account

Representa a conta do usuário no domínio da aplicação.

Campos:

- `id`: identificador único
- `name`: nome do usuário
- `email`: email de login
- `password`: senha (em texto puro, usado apenas na criação)
- `sha256`: senha criptografada
- `birthdate`: data de nascimento
- `creation`: data de criação da conta

---

## AccountModel

Entidade JPA que representa a tabela `account` no banco.

- `@Entity`
- Campos mapeados com `@Column`, como `tx_name`, `tx_email`, etc.

---

## AccountParser

Classe utilitária para conversão:

- `AccountIn` → `Account` (entrada)
- `Account` → `AccountOut` (resposta)

---

## AccountRepository

Interface que estende `CrudRepository`.

Métodos:

- `findByEmailAndSha256(email, sha256)`

---

## AccountService

Contém toda a lógica de negócios:

- Validação de senha
- Hash com SHA-256
- Interações com o repositório
- Conversão entre entidades e modelos

---

## AccountResource

Controller REST com endpoints:

- Criação, autenticação, listagem e `whoami`

---
