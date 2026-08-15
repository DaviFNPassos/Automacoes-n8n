# 🤖 AI News-to-Task Automation

Automação desenvolvida com **n8n** que utiliza **Inteligência Artificial** para analisar conteúdos recebidos através de um feed RSS e transformar as informações processadas em tarefas estruturadas.

## 🚀 Sobre o projeto

O objetivo deste projeto é demonstrar a aplicação de **automação de workflows + Inteligência Artificial** para coletar, analisar, organizar e transformar informações de forma automatizada.

O workflow utiliza um **Agente de IA** para interpretar os conteúdos recebidos do RSS e gerar uma saída estruturada que pode ser utilizada nas etapas seguintes da automação.

## ⚙️ Fluxo da automação

```text
RSS Feed
   ↓
Limite de itens
   ↓
Agente de IA
   ↓
Modelo de Chat OpenAI
   ↓
Analisador de saída estruturada
   ↓
Editar campos
   ↓
Repetir sobre itens
   ↓
Criar tarefa
```

## 🧠 Tecnologias utilizadas

* **n8n** — Plataforma utilizada para criação e execução da automação
* **OpenAI** — Modelo de Inteligência Artificial utilizado pelo agente
* **AI Agent** — Responsável pela análise e interpretação dos conteúdos
* **RSS Feed** — Fonte dos conteúdos processados
* **Structured Output** — Estruturação das respostas geradas pela IA
* **Data Transformation** — Organização e tratamento dos dados
* **Workflow Automation** — Automação de todo o processo

## 🔄 Funcionamento

### 1. RSS Feed

O workflow recebe conteúdos através de um feed RSS.

### 2. Limite

Controla a quantidade de informações que serão processadas pela automação.

### 3. Agente de IA

O conteúdo recebido é enviado para um agente de Inteligência Artificial responsável por analisar as informações.

### 4. Modelo OpenAI

O agente utiliza um modelo de linguagem da OpenAI para realizar a análise dos conteúdos.

### 5. Analisador de saída estruturada

A resposta gerada pela IA é organizada em um formato estruturado, facilitando o processamento das informações pelas próximas etapas.

### 6. Editar campos

Os dados são tratados e organizados de acordo com as necessidades da automação.

### 7. Repetir sobre itens

Cada item recebido é processado individualmente.

### 8. Criar tarefa

Após o processamento, as informações são utilizadas para gerar uma tarefa automaticamente.

## 🎯 Objetivos do projeto

* Praticar automação de processos utilizando n8n
* Integrar Inteligência Artificial em workflows
* Trabalhar com dados provenientes de RSS
* Utilizar modelos de linguagem para análise de informações
* Estruturar respostas geradas por IA
* Automatizar a criação de tarefas
* Desenvolver conhecimentos em integração e automação

## 📚 Conhecimentos aplicados

Este projeto demonstra conhecimentos em:

* Automação de workflows
* Inteligência Artificial
* Agentes de IA
* Integração com modelos de linguagem
* Processamento de dados
* RSS
* Structured Output
* Iteração de dados
* Transformação de informações
* Automação baseada em IA

## 🔧 Como utilizar

1. Tenha uma instalação do **n8n** configurada.
2. Importe o código em JSON no repositorio:
3. Configure as credenciais necessárias para utilização do modelo da OpenAI.
4. Configure o feed RSS desejado.
5. Execute o workflow.

## 🔐 Segurança

As chaves de API, tokens e outras informações sensíveis **não devem ser publicadas no GitHub**.

As credenciais devem ser configuradas diretamente no n8n através do sistema de credenciais da plataforma.

## 📁 Estrutura do projeto

```text
ai-news-to-task-automation/
│
├── README.md
│
├── workflow/
│   └── ai-news-to-task.json
│
└── screenshots/
    └── workflow.png
```

## 📌 Status

**Concluído — projeto desenvolvido para estudos e portfólio.**

## 👨‍💻 Autor

**Davi Fiães Naves Passos**

Estudante de Ciência da Computação com interesse em:

* 🤖 Inteligência Artificial
* ⚙️ Automação
* 🔗 Integração de APIs
* 🐍 Python
* 🔄 n8n
