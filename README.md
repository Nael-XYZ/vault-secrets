# Vault Secrets 🔑

HashiCorp Vault configuration for enterprise secrets management.

## Engines

| Engine | Purpose | TTL |
|--------|---------|-----|
| KV v2 | Static secrets | Unlimited |
| Database | Dynamic DB creds | 1 hour |
| Transit | Encryption-as-a-service | N/A |
| PKI | Internal TLS certs | 1 year |

## Quick Start

```bash
vault server -config=vault.hcl
vault init -key-shares=5 -key-threshold=3
vault unseal
```

## License

MPL-2.0