# Account Service

Este microsserviço é responsável por gerenciar contas de usuário, incluindo:

- Criação de contas
- Autenticação por email e senha (com hash SHA-256)
- Listagem e consulta de contas

O serviço é parte de uma arquitetura de microsserviços, utilizando Spring Boot, PostgreSQL e Flyway.

---

## Funcionalidades

- **Criação de Conta**: Permite que novos usuários se registrem no sistema.
- **Listagem de Contas**: Permite visualizar todas as contas registradas.
- **Consulta de Conta**: Permite visualizar detalhes de uma conta específica pelo e-mail e senha.
- **Whoami**: Permite identificar a conta logada.