# Arquitetura

## Estrutura de Pastas

```bash
src/main/java/store/account/
│ ├── Account.java # Entidade de domínio
│ ├── AccountModel.java # Entidade JPA
│ ├── AccountParser.java # Conversão entre modelos e DTOs
│ ├── AccountRepository.java # Interface de persistência
│ ├── AccountService.java # Lógica de negócio
│ └── AccountResource.java # Controller REST
└── resources/
│ ├── application.yaml # Configurações de ambiente
│ └── db/migration/ # Scripts Flyway
```
