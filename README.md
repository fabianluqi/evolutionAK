# EvolutionAK 🚀

### Sistema de vendas e atendimento automatizado via WhatsApp

O **EvolutionAK** é uma stack backend desenvolvida para automatizar o ciclo comercial de empresas, com foco inicial em produtos personalizados e sublimação. O sistema transforma o WhatsApp em uma central inteligente de atendimento, automação e organização de pedidos.

---

# 🎯 Objetivo

Eliminar gargalos no atendimento manual automatizando:

* FAQ inicial
* triagem de clientes
* captura de pedidos
* notificações
* fluxos comerciais
* integrações automatizadas

O objetivo é permitir que o atendimento humano atue apenas nas etapas críticas ou consultivas.

---

# 🧱 Stack Tecnológica

* **Engine de Chat:** Evolution API
* **Orquestração de Workflows:** n8n (Queue Mode)
* **Banco de Dados:** PostgreSQL
* **Mensageria & Cache:** Redis
* **Infraestrutura:** VPS DigitalOcean
* **Containers:** Docker
* **Gerenciamento:** Easypanel
* **Proxy Reverso / SSL:** Traefik

---

# 🏗️ Arquitetura

A infraestrutura utiliza uma arquitetura desacoplada baseada em microsserviços:

```txt
WhatsApp
   ↓
Evolution API
   ↓
n8n_webhook
   ↓
Redis Queue
   ↓
n8n_worker
   ↓
PostgreSQL
```

Essa abordagem permite:

* processamento assíncrono
* maior estabilidade
* escalabilidade horizontal
* isolamento de responsabilidades
* melhor gerenciamento de carga

> 📌 Documentação completa disponível em:
>
> Documentação completa disponível em: [architecture.md](./docs/architecture.md)

---

# 📂 Estrutura do Projeto

```txt
evolutionAK/
├── docs/                  # Documentação técnica
├── .env.example           # Template de variáveis de ambiente
├── docker-compose.yml     # Infraestrutura Docker
├── README.md              # Guia principal do projeto
└── tasks.md               # Roadmap e backlog técnico
```

---

# 🚀 Roadmap

## Infraestrutura

* [x] VPS DigitalOcean
* [x] Docker
* [x] Easypanel
* [x] SSL automático
* [x] Proxy reverso com Traefik
* [x] Arquitetura Queue Mode (n8n)

## Funcionalidades

* [ ] FAQ automatizado
* [ ] Catálogo inteligente
* [ ] Geração automática de orçamento
* [ ] Fluxo estruturado de pedidos
* [ ] CRM básico
* [ ] Integração OpenAI
* [ ] Automação comercial
* [ ] Notificações automáticas
* [ ] Painel administrativo

---

# ⚙️ Como Rodar

## 1. Clonar o repositório

```bash
git clone https://github.com/seu-usuario/evolutionAK.git

cd evolutionAK
```

---

## 2. Configurar variáveis de ambiente

```bash
cp .env.example .env
```

Depois edite o arquivo `.env` e configure:

* senhas
* domínios
* URLs
* tokens
* credenciais

---

## 3. Subir os containers

```bash
docker compose up -d
```

---

# 🖥️ Deploy via Easypanel

Caso utilize Easypanel:

1. Importe o repositório GitHub
2. Configure os domínios
3. Cole as variáveis na aba **Environment**
4. Realize o deploy dos serviços

As variáveis sensíveis NÃO devem ser commitadas no Git.

---

# 🔒 Segurança

A infraestrutura segue práticas de segurança para ambientes self-hosted.

## Proteções implementadas

* variáveis protegidas via `.env`
* `.gitignore` configurado para secrets
* SSL/TLS automático
* proxy reverso isolando containers
* comunicação interna via rede Docker
* separação de serviços por responsabilidade

## Investigação de Segurança

Foi identificada uma tentativa externa de acesso ao arquivo `.env`.

Teste realizado:

```bash
curl -k https://localhost/.env
```

Resultado:

```txt
404 Not Found
```

Conclusão:
As variáveis de ambiente não estão expostas publicamente.

---

# 📌 Status Atual

| Área           | Status          |
| -------------- | --------------- |
| Infraestrutura | ✅ Operacional   |
| SSL / Proxy    | ✅ Operacional   |
| Queue Mode     | ✅ Operacional   |
| Evolution API  | ⚙️ Configurando |
| Workflows      | 📅 Planejado    |
| IA / OpenAI    | 📅 Planejado    |
| Monitoramento  | 📅 Planejado    |

---

# 📖 Documentação

* `README.md` → visão geral do projeto
* `docs/architecture.md` → arquitetura detalhada
* `.env.example` → template de configuração
* `tasks.md` → backlog técnico e roadmap

---

# ⚠️ Observação

Este projeto encontra-se em evolução contínua e a arquitetura pode sofrer alterações conforme novas integrações, automações e necessidades de escalabilidade forem adicionadas.
