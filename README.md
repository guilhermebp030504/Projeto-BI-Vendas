# Projeto BI com Docker, n8n e Metabase

Sistema de ETL e Business Intelligence utilizando Portainer, PostgreSQL, n8n e Metabase.

---

# Arquitetura

```text
Arquivo Local
     ↓
n8n (ETL / automação)
     ↓
PostgreSQL
     ↓
Metabase (Dashboards e BI)
```

---

# Tecnologias Utilizadas

- Docker
- Portainer
- PostgreSQL
- n8n
- Metabase

---

# Objetivo do Projeto

O projeto automatiza o fluxo de ingestão e visualização de dados:

1. O n8n lê arquivos locais
2. Os dados são processados automaticamente
3. As informações são armazenadas no PostgreSQL
4. O Metabase consome os dados do banco
5. Dashboards e análises são gerados em tempo real

---

# Estrutura do Projeto

```text
.
├── docker-compose.yml
├── .env
├── .gitignore
├── README.md
├── vendas.csv
│
├── n8n/
│   └── workflows/
├── metabase/
```

---

# Como Executar o Projeto

## 1. Clonar o repositório

```bash
git clone https://github.com/guilhermebp030504/Projeto-BI-Vendas.git
```

---

## 2. Entrar na pasta do projeto

```bash
cd Projeto-BI-Vendas
```

---

## 3. Subir os containers

```bash
docker compose up -d
```

---

# Serviços Disponíveis

| Serviço | URL |
|---|---|
| n8n | http://localhost:5680 |
| Metabase | http://localhost:3001 |
| PostgreSQL | localhost:5433 |

---

# Variáveis de Ambiente

Exemplo do arquivo `.env`:

```env
POSTGRES_USER=admin
POSTGRES_PASSWORD=admin
POSTGRES_DB=vendas

POSTGRES_PORT=5433
N8N_PORT=5680
METABASE_PORT=3001
```

---

# Funcionalidades

- Automação de ETL com n8n
- Persistência de dados no PostgreSQL
- Dashboards interativos no Metabase
- Ambiente totalmente containerizado
- Fácil replicação utilizando Portainer

---

# Workflows do n8n

Os workflows exportados ficam em:

```text
n8n/workflows/
```

---

# Possíveis Melhorias Futuras

- Deploy em VPS
- HTTPS com Nginx ou Traefik
- Backup automático do PostgreSQL
- Integração com APIs externas
- Monitoramento e logs
- Pipeline CI/CD

---

# Aprendizados

Este projeto permitiu praticar:

- Docker e Portainer
- ETL e automação
- Integração entre serviços
- Modelagem de banco de dados
- Business Intelligence
- Orquestração de containers

---

# Autor

Desenvolvido por [guilhermebp030504](https://github.com/guilhermebp030504)
