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
   
Crie um arquivo .env na raiz do projeto com suas credenciais do Trello:

```env
TRELLO_API_KEY=seu_api_key
TRELLO_API_SECRET=seu_api_secret
TRELLO_TOKEN=seu_token´´´


Instale as dependências:

'''bash
pip install -r requirements.txt


▶️ Execução
Ative o ambiente virtual:

```powershell
.\.lab-dio\Scripts\Activate.ps1
Vá até a pasta do agente:

powershell
cd agents\agent04\agenttaskmanager
Rode o servidor:

powershell
adk web --port 8000
Acesse o DevUI em:

Código
http://127.0.0.1:8000
📋 Exemplos de Uso
➕ Adicionar tarefa
Código
Usuário: Quero adicionar a tarefa "Fazer compras no mercado"
Agente: ✅ Tarefa adicionada no Trello!
📑 Listar tarefas
Código
Usuário: Liste todas as tarefas em andamento
Agente: 
- Estudar Python (Em Andamento)
- Fazer compras (A Fazer)
🔄 Mudar status
Código
Usuário: Marque a tarefa "Fazer compras" como concluída
Agente: ✅ 'Fazer compras': A FAZER → CONCLUÍDO
📸 Prints de Execução
Exemplo de card criado no Trello:
[Parece que o resultado não era seguro para exibição. Vamos mudar as coisas e tentar outra opção!]

Exemplo do agente respondendo no DevUI:
[Parece que o resultado não era seguro para exibição. Vamos mudar as coisas e tentar outra opção!]

(Substitua link-da-imagem pelos links das imagens que você subir no GitHub ou arraste os prints para o editor do README.)

🧩 Estrutura do Projeto
Código
automacao-trello-python/
│
├── agents/
│   ├── agent04/
│   │   └── agenttaskmanager/
│   │       └── agent.py   # contém o root_agent e funções
│
├── .env                   # credenciais Trello
├── requirements.txt
└── README.md
✨ Observações
O Trello interpreta datas em UTC, por isso o código converte horários para evitar discrepâncias.

O modelo Gemini tem limite de requisições na versão gratuita (20/dia). Se atingir o limite, aguarde ou configure billing no Google Cloud.
