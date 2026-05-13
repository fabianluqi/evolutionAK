````md
# EvolutionAK Stack

### Sistema de vendas automatizado via chat

O EvolutionAK é uma stack backend para automação de atendimento comercial via WhatsApp, inicialmente focada em empresas de personalizados por sublimação.

## 🎯 Objetivo

Automatizar:
- atendimento ao cliente
- orçamentos
- organização de pedidos
- integração com WhatsApp
- encaminhamento para atendimento humano
- integração futura com IA

---

## 🧱 Stack

- PostgreSQL
- Redis
- EvolutionAPI
- n8n
  - n8nEditor
  - n8nWebhook
  - n8nWorker

Infraestrutura hospedada em VPS da DigitalOcean utilizando Docker, Docker Compose e EasyPanel.

---

## 🏗️ Arquitetura

```plaintext
Cliente WhatsApp
        ↓
   EvolutionAPI
        ↓
        n8n
   ↙         ↘
Redis     PostgreSQL
````

---

## 📌 Status Atual

Atualmente o projeto encontra-se em fase de infraestrutura.

A stack já possui:

* VPS configurada
* containers funcionais
* HTTPS configurado
* proxy reverso funcional
* comunicação interna entre containers

Os workflows e automações ainda serão implementados.

---

## 🚀 Roadmap

* atendimento automático inteligente (FAQ)
* encaminhamento para humano
* catálogo automático de produtos
* orçamento automático
* captura de pedido estruturado
* fluxo de atendimento com etapas
* envio e recebimento de mídia
* status de pedido automático
* lembretes automáticos
* notificação interna
* funis de venda automáticos
* upsell automático
* CRM simples
* respostas contextuais
* automação com IA (OpenAI integrado ao n8n)

---

## ⚙️ Como rodar

```bash
git clone <repositorio>

cd evolutionAK

cp .env.example .env

docker compose up -d
```

```
```
