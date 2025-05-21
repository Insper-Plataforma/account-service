# Segurança

## Armazenamento de Senha

O sistema **não armazena senhas em texto puro**. Ao criar ou autenticar uma conta:

1. A senha fornecida é transformada via `SHA-256`
2. O hash é codificado em Base64
3. O resultado é armazenado na coluna `tx_sha256` do banco

Exemplo de método:

```java
private String calcHash(String value) {
    MessageDigest digester = MessageDigest.getInstance("SHA-256");
    byte[] hash = digester.digest(value.getBytes(StandardCharsets.UTF_8));
    return Base64.getEncoder().encodeToString(hash);
}
```
---

## Validação

- Senhas com menos de 8 caracteres são rejeitadas com erro HTTP 400.
- A autenticação só ocorre se email e senha gerarem o mesmo hash salvo.

---