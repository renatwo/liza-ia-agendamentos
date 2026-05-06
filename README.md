💈 Projeto Liza: AI Appointment Assistant (SaaS)
A Liza é uma agente de IA conversacional desenvolvida para automatizar o fluxo completo de agendamentos em barbearias via WhatsApp. O sistema utiliza uma arquitetura baseada em agentes para entender intenções, processar voz e gerenciar o banco de dados de forma autônoma.

🧠 Inteligência e Lógica do Agente
O diferencial deste projeto é o uso de um Agente de IA (LangChain) que atua como orquestrador de ferramentas.

Principais Funcionalidades:
Processamento Multimodal: Entende mensagens de texto e áudios nativos do WhatsApp através da integração com OpenAI Whisper.

Memória de Curto Prazo: Implementação de Postgres Chat Memory, permitindo que a IA retenha o contexto das últimas interações para um diálogo natural.

Agente Reativo: A Liza não apenas responde dúvidas, mas executa ações como consultar horários, verificar barbeiros disponíveis e criar agendamentos diretamente no banco de dados.

Gestão de Estado: Sistema robusto para pausar ou ativar o bot conforme a necessidade do atendimento humano.

🛠️ Pilha Tecnológica
Orquestrador: n8n (Autohospedado via Docker).

LLMs: GPT-4.1 (Raciocínio Lógico) e Whisper-1 (Transcrição de Áudio).

Backend & DB: Supabase (PostgreSQL) para persistência de dados e Edge Functions.

API de Mensageria: Evolution API para integração com WhatsApp.

⚙️ Configuração do Ambiente
Para replicar este workflow, é necessário configurar as seguintes variáveis de ambiente no n8n:

OPENAI_API_KEY: Para processamento de linguagem natural e transcrição.

SUPABASE_API_KEY: Para autenticação nas ferramentas de banco de dados.

EVOLUTION_API_KEY: Para envio e recebimento de mensagens.
