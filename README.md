# EvolutionAK Stack
## Sistema de vendas automatizado via chat 
### Este projeto foi criado para o atendimento primario de estabelecimentos para com clientes no Whatsapp.
 Atualmente hospedado em uma VPS da DigitalOcean, foi criada a partir de um script usando EasyPanel e docker-compose.
 Os serviços usados são: Postgres, EvolutionAPI, Redis, e n8n (sendo eles n8nEditor, n8nWebhook e n8nWorker).
 A versão primaria do projeto não apresenta funcionalidade, pois é apenas o modelo de infraestrutura da stack,
 caso desejado replicar o projeto. Futuramente serão implementadas a seguintes funcionalidades: atendimento automático
 inteligente (FAQ), encaminhamento para humano, catálogo automático de produtos, orçamento automático, captura de
 pedido estruturado, fluxo de atendimento com etapas, envio e recebimento de mídia, status de pedido automático,
 lembretes automáticos, notificação interna, funis de venda automáticos, upsell automático, CRM simples,
 respostas contextuais, automação com IA (OpenAI integrado no n8n).
