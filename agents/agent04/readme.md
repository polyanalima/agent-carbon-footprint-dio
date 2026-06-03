# 📌 Projeto: Integração Trello com Python e ADK

## 🚀 Descrição
Este projeto faz parte do desafio da DIO e tem como objetivo criar um **Agente de Organização de Tarefas** utilizando Python, Trello e o Google ADK.  

O agente é capaz de:
- ➕ Adicionar novas tarefas no Trello
- 📑 Listar tarefas por status
- 🔄 Mudar o status de tarefas (ex: "A Fazer" → "Em Andamento" → "Concluído")
- 🕒 Gerar contexto temporal (data e hora atual)

---

## 🛠️ Tecnologias Utilizadas
- Python 3.10+
- Trello API (via `py-trello`)
- Google ADK
- dotenv (para variáveis de ambiente)

---

## ⚙️ Configuração

1. Clone o repositório:
```bash
git clone https://github.com/polyanalima/agent-carbon-footprint.git


2. Crie um arquivo .env na raiz do projeto com suas credenciais do Trello:
```
TRELLO_API_KEY=seu_api_key
TRELLO_API_SECRET=seu_api_secret
TRELLO_TOKEN=seu_token
