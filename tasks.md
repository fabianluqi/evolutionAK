# 🚀 Roadmap de Evolução da Infraestrutura

---

## 🛡️ FASE 1 — Estabilizar a Infraestrutura Atual
**Objetivo:** Garantir a resiliência do sistema e eliminar vazamentos de dados.

*   [ ] **GitHub Organizado**
    *   Limpar repositórios obsoletos.
    *   Padronizar commits e branches.
*   [x] **Documentar Arquitetura Atual**
    *   Mapear fluxos de dados.
    *   Criar diagramas de componentes atuais.
*   [ ] **Validar Firewall e Exposição Pública**
    *   Bloquear portas desnecessárias.
    *   Revisar regras de entrada e saída.
*   [ ] **Remover Exposição do Easypanel**
    *   Restringir acesso externo ao painel.
    *   Utilizar VPN ou túneis seguros.
*   [x] **Organizar Segredos**
    *   Auditar arquivos `.env`.
    *   Configurar `.gitignore` corretamente.
    *   Rotacionar chaves de API expostas.
*   [ ] **Backup Real do Postgres + Volumes Docker**
    *   Automatizar dumps do banco de dados.
    *   Configurar cópias de segurança dos volumes.
    *   Testar a restauração dos backups.

---

## 🧠 FASE 2 — Entender Profundamente a Stack
**Objetivo:** Dominar as ferramentas para parar de seguir tutoriais cegamente.

*   [ ] **Entender Docker Networking**
    *   Dominar redes isoladas e pontes.
    *   Aprender comunicação interna entre containers.
*   [ ] **Entender Traefik / Proxy Reverso**
    *   Compreender o roteamento de requisições.
    *   Aprender configuração de entrypoints e routers.
*   [ ] **Entender HTTPS / Certificados**
    *   Dominar a geração via Let's Encrypt.
    *   Compreender a renovação automática de TLS.
*   [ ] **Entender Filas do n8n**
    *   Aprender o funcionamento do modo queue.
    *   Gerenciar workers para execução paralela.
*   [ ] **Entender Redis na Prática**
    *   Compreender o Redis como broker de mensagens.
    *   Monitorar o consumo de memória cache.
*   [ ] **Entender Persistência do Postgres**
    *   Estudar escrita em disco e commits.
    *   Otimizar armazenamento de volumes Docker.

---

## 💼 FASE 3 — Transformar em Produto
**Objetivo:** Construir a arquitetura robusta de um SaaS comercial executável.

*   [ ] **Fluxos Reais de Automação WhatsApp**
    *   Criar gatilhos inteligentes de mensagens.
    *   Tratar falhas de envio e retentativas.
*   [ ] **Sistema de Atendimento Humano**
    *   Integrar transição automação-humano sem gargalos.
    *   Configurar filas de atendimento por agentes.
*   [ ] **Separar Ambientes (Dev/Prod)**
    *   Isolar banco de dados de teste.
    *   Garantir chaves de API exclusivas para produção.
*   [ ] **Deploy Reproduzível**
    *   Criar scripts de infraestrutura como código.
    *   Garantir subida do sistema com um comando.
*   [ ] **Domínio Próprio**
    *   Configurar DNS profissional.
    *   Implementar subdomínios organizados para clientes.
*   [ ] **Monitoramento e Alertas**
    *   Configurar métricas de uso de CPU/Memória.
    *   Criar alertas automatizados em caso de queda.
*   [ ] **Escalabilidade**
    *   Preparar o sistema para crescimento horizontal.
    *   Balancear carga entre múltiplos servidores.
*   [ ] **Multi-Cliente / SaaS**
    *   Implementar isolamento estrito de dados por cliente.
    *   Configurar controle de acessos e planos comerciais.
