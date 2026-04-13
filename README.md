# 🤖 Agente de Gerenciamento de Tarefas com Trello

Projeto desenvolvido como **Desafio de Projeto do Módulo 3** do **Bootcamp CI&T – Do Prompt ao Agente**, com foco na criação de um agente inteligente para automatizar fluxos de trabalho usando Python, Google ADK e a API do Trello.

---

## 📋 Sobre o Projeto

Este agente conversacional é capaz de gerenciar suas tarefas diárias diretamente no Trello. Ao ser ativado, ele pergunta quais são as atividades do dia, cria cards automaticamente e permite mover tarefas entre as listas **A Fazer**, **Em Andamento** e **Concluído**.

---

## ✨ Funcionalidades

- ✅ **Adicionar tarefas** – Cria cards no Trello com nome, descrição e data de vencimento
- 📋 **Listar tarefas** – Lista todas as tarefas ou filtra por status
- 🔄 **Mudar status** – Move cards entre as listas do board
- 🕐 **Contexto temporal** – Informa a data e hora atual para organizar as tarefas do dia

---

## 🛠️ Tecnologias Utilizadas

| Tecnologia | Descrição |
|---|---|
| [Python 3.10+](https://www.python.org/) | Linguagem principal |
| [Google ADK](https://google.github.io/adk-docs/) | Framework para criação de agentes de IA |
| [Gemini 2.5 Flash](https://deepmind.google/technologies/gemini/) | Modelo de linguagem utilizado pelo agente |
| [py-trello](https://github.com/sarumont/py-trello) | Integração com a API do Trello |
| [python-dotenv](https://pypi.org/project/python-dotenv/) | Gerenciamento de variáveis de ambiente |

---

## 📁 Estrutura do Projeto
```
├── agents/
│   └── AgentTaskManager/
│       ├── __init__.py
│       └── agent.py        # Lógica principal do agente e ferramentas
├── .gitignore
├── requirements.txt
└── README.md
```

---

## 🚀 Como Executar

### Pré-requisitos

- Python 3.10 ou superior
- Conta no [Trello](https://trello.com/) com um board chamado **DIO** contendo as listas:
  - `A Fazer` (ou `To Do`)
  - `Em Andamento` (ou `Doing`)
  - `Concluído` (ou `Done`)
- Credenciais da [API do Trello](https://trello.com/app-key)
- Chave de API do Google (para acesso ao Gemini)

### Instalação

1. **Clone o repositório:**
```bash
   git clone https://github.com/seu-usuario/seu-repositorio.git
   cd seu-repositorio
```

2. **Crie e ative o ambiente virtual:**
```bash
   python -m venv .venv
   source .venv/bin/activate      # Linux/macOS
   .venv\Scripts\activate         # Windows
```

3. **Instale as dependências:**
```bash
   pip install -r requirements.txt
```

4. **Configure as variáveis de ambiente:**

   Crie um arquivo `.env` na raiz do projeto com o seguinte conteúdo:
```env
   TRELLO_API_KEY=sua_api_key
   TRELLO_API_SECRET=seu_api_secret
   TRELLO_TOKEN=seu_token
   GOOGLE_API_KEY=sua_google_api_key
```

5. **Execute o agente:**
```bash
   adk run agents/AgentTaskManager
```

---

## 💬 Exemplo de Uso
```
Agente: Olá! Hoje é 27/03/2026 às 10:00. Quais são suas tarefas para hoje?

Você: Preciso revisar o relatório mensal

Agente: Entendido! Qual a descrição dessa tarefa e a data de vencimento?

Você: Revisar e corrigir o relatório de março, vence hoje

Agente: ✅ Tarefa "Revisar o relatório mensal" criada no Trello! Tem mais alguma tarefa?

Você: Não, por enquanto é só.

Agente: Perfeito! Suas tarefas foram organizadas. Bom trabalho! 🎯
```

---

## 📌 Configuração do Board no Trello

O agente espera um board chamado **DIO** com as seguintes listas (os nomes são flexíveis, conforme o mapeamento abaixo):

| Status | Nomes aceitos |
|---|---|
| A Fazer | `A Fazer`, `To Do`, `TODO` |
| Em Andamento | `Em Andamento`, `Doing` |
| Concluído | `Concluído`, `Concluido`, `Done` |

---

## 🤝 Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir uma *issue* ou enviar um *pull request*.

---

## 📄 Licença

Este projeto foi desenvolvido para fins educacionais no âmbito do Bootcamp CI&T.

---

## 👤 Autor

Desenvolvido como parte do **Bootcamp CI&T – Do Prompt ao Agente, Módulo 3**.
