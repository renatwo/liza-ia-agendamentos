# 💈 Projeto Liza: AI Appointment Assistant (SaaS)

A **Liza** é uma agente de IA conversacional desenvolvida para automatizar o fluxo completo de agendamentos em barbearias via WhatsApp. O sistema utiliza uma arquitetura baseada em agentes para entender intenções, processar voz e gerenciar o banco de dados de forma autônoma.

## 🧠 Inteligência e Lógica do Agente

O diferencial deste projeto é o uso de um **AI Agent** (LangChain) que atua como orquestrador de ferramentas (tools).

### Principais Funcionalidades:
*   **Processamento Multimodal:** Entende mensagens de texto e áudios nativos do WhatsApp através da integração com **OpenAI Whisper**.
*   **Memória de Curto Prazo:** Implementação de **Postgres Chat Memory**, permitindo que a IA retenha o contexto das últimas 10 interações para um diálogo natural[cite: 1].
*   **Agente Reativo:** A Liza não apenas responde dúvidas, mas executa ações como consultar horários, verificar barbeiros disponíveis e criar agendamentos diretamente no banco de dados[cite: 1].
*   **Gestão de Estado:** Sistema robusto para pausar ou ativar o bot conforme a necessidade do atendimento humano[cite: 1].

## 🛠️ Stack Tecnológica

*   **Orquestrador:** [n8n](https://n8n.io/) (Self-hosted via Docker)[cite: 1].
*   **LLMs:** GPT-4.1 (Raciocínio Lógico) e Whisper-1 (Transcrição de Áudio)[cite: 1].
*   **Backend & DB:** [Supabase](https://supabase.com/) (PostgreSQL) para persistência de dados e Edge Functions[cite: 1].
*   **API de Mensageria:** Evolution API para integração com WhatsApp[cite: 1].

## ⚙️ Configuração do Ambiente

Para replicar este workflow, é necessário configurar as seguintes variáveis de ambiente no n8n:

1.  `OPENAI_API_KEY`: Para processamento de linguagem natural e transcrição.
2.  `SUPABASE_API_KEY`: Para autenticação nas ferramentas de banco de dados.
3.  `EVOLUTION_API_KEY`: Para envio e recebimento de mensagens.


---
*Status do Projeto: Em produção / Escalável.*
