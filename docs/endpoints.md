# Endpoints da API

Base URL: `/account`

---

## POST `/account`

Cria uma nova conta.

### Request Body (JSON)
```json
{
  "name": "Ana Helena",
  "email": "ana@exemplo.com",
  "password": "12345678"
}
```

### Response (201 Created)
```json
{
  "id": "uuid",
  "name": "Ana Helena",
  "email": "ana@exemplo.com"
}
```

---

## GET `/account`

Lista todas as contas registradas.

### Response (200 OK)
```json
[
  {
    "id": "uuid",
    "name": "Ana Helena",
    "email": "ana@exemplo.com"
    }
]
```

---

## POST `/account/auth`

Autentica o usuário com email e senha.

### Request Body (JSON)
```json
{
  "email": "ana@exemplo.com",
  "password": "12345678"
}
```

### Response (200 OK)
```json
{
  "id": "uuid",
  "name": "Ana Helena",
  "email": "ana@exemplo.com"
}
```

---

## GET `/account/{id}`

Retorna informações da conta autenticada (whoami).

### Path Param
- `id` (string): ID da conta.

### Response (200 OK)
```json
{
  "id": "uuid",
  "name": "Ana Helena",
  "email": "ana@exemplo.com"
}
```
---
