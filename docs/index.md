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

---

## Integração com Jenkins

Este projeto conta com um arquivo Jenkinsfile (na raiz do repositório) que define uma pipeline de integração contínua para compilar automaticamente o módulo sempre que houver alterações no repositório.

### Para que serve?

- Compilação automatizada: toda alteração no repositório dispara o build do Maven, detectando problemas de compilação antes do merge.

- Imagens Docker consistentes: gera e publica automaticamente imagens multiplataforma, facilitando o deploy em diferentes ambientes (x86_64 e ARM).

- Segurança das credenciais: utiliza credenciais armazenadas no Jenkins (identificador dockerhub-credential), evitando exposição de senhas no código.

Dessa forma, a integração com Jenkins garante que o account-service esteja sempre compilando e empacotado corretamente, com uma imagem Docker pronta para ser implantada nos clusters de produção ou QA.
