markdown
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
bash
```git clone https://github.com/polyanalima/agent-carbon-footprint.git
```

2. Crie um arquivo .env na raiz do projeto com suas credenciais do Trello:

env
```TRELLO_API_KEY=seu_api_key
   TRELLO_API_SECRET=seu_api_secret
   TRELLO_TOKEN=seu_token
```

3. Instale as dependências:

bash
```
pip install -r requirements.txt
```

▶️ Execução

1. Ative o ambiente virtual:

powershell
```
.\.lab-dio\Scripts\Activate.ps1
```

2. Vá até a pasta do agente:

powershell
```
cd agents\agent04\agenttaskmanager
```

3. Rode o servidor:

powershell
```
adk web --port 8000
```

⚠️ Se a porta 8000 já estiver ocupada, você pode alterar para outra porta (ex: 8080):

powershell
```
adk web --port 8080
```

4. Acesse o DevUI em:

Código
```
http://127.0.0.1:8000
```
(ou substitua pela porta que você escolheu, ex: http://127.0.0.1:8080)

📋 Exemplos de Uso
➕ Adicionar tarefa
<img width="1256" height="919" alt="image" src="https://github.com/user-attachments/assets/7acb7921-0c4a-465d-b3f2-d3fe9b87999c" />


Usuário: "Fazer compras no mercado"
Agente: ✅ Tarefa adicionada no Trello!


📑 Listar tarefas
<img width="1244" height="890" alt="image" src="https://github.com/user-attachments/assets/7fd85c96-fa60-46e3-9f8e-c86f09fb5c93" />

text
Usuário: Liste todas as tarefas 
Agente: 
Aqui estão as tarefas que você tem para hoje:
Ir ao médico (Status: A fazer) - Consulta de rotina
Fazer compras no mercado (Status: A fazer) - Comprar itens essenciais para a casa: alimentos, produtos de limpeza, etc.
Dar banho no cachorro (Status: Concluído) - Dar banho no cachorro a tarde

🔄 Mudar status
<img width="1253" height="908" alt="image" src="https://github.com/user-attachments/assets/7a8d8f2a-645f-4a2e-a84e-a640d7799cd2" />

text
Usuário: Marque a tarefa "Fazer compras" como concluída
Agente: ✅ 'Fazer compras': A FAZER → CONCLUÍDO


📸 Prints de Execução
Exemplo de card criado no Trello:
<img width="1527" height="733" alt="image" src="https://github.com/user-attachments/assets/a60c96b8-f06c-452f-b1ce-a31de8f2da8a" />


🧩 Estrutura do Projeto
```
text
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

```
✨ Observações
O Trello interpreta datas em UTC, por isso o código converte horários para evitar discrepâncias.

O modelo Gemini tem limite de requisições na versão gratuita (20/dia). Se atingir o limite, aguarde ou configure billing no Google Cloud.
