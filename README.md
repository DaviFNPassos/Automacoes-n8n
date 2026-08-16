# 📰 Automação de Notícias com IA usando n8n

Automação desenvolvida no **n8n** para coletar notícias através de um feed RSS, utilizar Inteligência Artificial para analisar e selecionar os conteúdos mais relevantes e, posteriormente, organizar as notícias selecionadas como tarefas no **Todoist**.

O projeto foi desenvolvido como um projeto pessoal para estudo e demonstração de conhecimentos em **automação de processos, Inteligência Artificial, APIs, RSS e integração entre ferramentas**.

## 🚀 Objetivo

O objetivo do projeto é automatizar o processo de acompanhamento de notícias.

Em vez de acessar manualmente diversos sites e decidir quais notícias são relevantes, o fluxo realiza esse processo automaticamente:

```text
RSS
 ↓
Coleta das notícias
 ↓
Limitação da quantidade de itens
 ↓
Análise com Inteligência Artificial
 ↓
Seleção das notícias relevantes
 ↓
Organização dos dados
 ↓
Loop pelas notícias selecionadas
 ↓
Criação das tarefas no Todoist
```

## ⚙️ Tecnologias utilizadas

* **n8n** — criação e gerenciamento do workflow
* **RSS** — coleta automática das notícias
* **OpenAI** — análise e classificação dos conteúdos
* **Todoist** — organização das notícias selecionadas
* **Structured Output Parser** — estruturação da resposta da IA

## 🔄 Funcionamento do Workflow

### 1. Manual Trigger

O workflow pode ser iniciado manualmente através do nó:

**When clicking "Execute workflow"**

Esse gatilho é utilizado durante o desenvolvimento e testes da automação.

### 2. RSS Read

O nó **RSS Read** realiza a leitura do feed RSS configurado.

A partir dele, o workflow recebe informações como:

* Título da notícia
* Link
* Descrição
* Data de publicação
* Outras informações disponibilizadas pelo feed

### 3. Limit

Após a coleta das notícias, o nó **Limit** limita a quantidade de itens processados.

No fluxo atual, são processados até **50 itens**, evitando que uma quantidade excessiva de informações seja enviada para a etapa de análise.

### 4. AI Agent

O **AI Agent** é responsável por analisar as notícias recebidas.

A inteligência artificial pode avaliar os conteúdos de acordo com critérios definidos no prompt, como:

* Relevância
* Qualidade da notícia
* Interesse do usuário
* Tema
* Potencial de utilidade
* Prioridade

O objetivo é evitar que todas as notícias coletadas sejam encaminhadas para a etapa seguinte.

### 5. OpenAI Chat Model

O agente utiliza um modelo da **OpenAI** para realizar a análise dos conteúdos.

Essa etapa permite que a automação utilize IA para tomar decisões com base nas informações coletadas pelo RSS.

### 6. Structured Output Parser

O **Structured Output Parser** é utilizado para garantir que a resposta produzida pela IA siga uma estrutura definida.

Isso facilita o processamento das informações pelas etapas seguintes do workflow.

### 7. Edit Fields

O nó **Edit Fields** organiza e ajusta os dados que serão utilizados nas próximas etapas da automação.

Essa etapa permite padronizar as informações antes de enviá-las para o processo de criação das tarefas.

### 8. Loop Over Items

O **Loop Over Items** percorre individualmente cada notícia selecionada.

Isso permite que cada notícia seja processada separadamente antes de ser enviada ao Todoist.

### 9. Todoist

Por fim, a automação utiliza o **Todoist** para criar uma tarefa para cada notícia selecionada pela IA.

Dessa forma, as notícias consideradas mais relevantes ficam organizadas em uma lista de tarefas, facilitando a leitura posterior.

## 🧠 Exemplo de utilização

Imagine que o RSS disponibilize 50 notícias durante o dia.

A automação pode:

1. Coletar as 50 notícias.
2. Enviar os conteúdos para a IA.
3. Analisar a relevância de cada notícia.
4. Selecionar somente as notícias que atendem aos critérios definidos.
5. Organizar as informações.
6. Percorrer cada notícia selecionada.
7. Criar automaticamente uma tarefa no Todoist.

O resultado é uma **curadoria automática de notícias utilizando Inteligência Artificial**.

## 📊 Benefícios da automação

* Redução do trabalho manual
* Curadoria automática de conteúdo
* Utilização de IA para classificação
* Organização das informações
* Integração entre diferentes serviços
* Possibilidade de execução recorrente
* Facilidade para acompanhar notícias relevantes

## 🔐 Segurança

As credenciais utilizadas pelo workflow não devem ser armazenadas no GitHub.

Antes de publicar o projeto, remova ou substitua:

* API Keys
* Tokens
* Senhas
* Credenciais OAuth
* Informações pessoais

No GitHub, recomenda-se disponibilizar apenas o workflow sem as credenciais.

## 📁 Estrutura do projeto

```text
automacao-noticias-n8n/
│
├── README.md
├── workflow/
│   └── noticias-n8n.json
│
├── screenshots/
│   └── workflow.png
│
└── .gitignore
```

## 🛠️ Como utilizar

### 1. Instale ou acesse uma instância do n8n

É possível utilizar o n8n localmente ou através de uma instância hospedada.

### 2. Importe o workflow

Importe o arquivo:

```text
Workflow-noticia-n8n.json
```

### 3. Configure as credenciais

Configure as credenciais necessárias para:

* OpenAI
* Todoist

### 4. Configure o RSS

Adicione o endereço do feed RSS que deseja utilizar.

### 5. Execute o workflow

Execute o workflow através do nó:

```text
When clicking "Execute workflow"
```

Após a execução, as notícias selecionadas pela IA deverão ser encaminhadas para o Todoist.

## 🔮 Melhorias futuras

Algumas melhorias que podem ser adicionadas ao projeto:

* [ ] Executar automaticamente em horários definidos
* [ ] Utilizar múltiplos feeds RSS
* [ ] Criar categorias para as notícias
* [ ] Adicionar sistema de pontuação de relevância
* [ ] Criar prioridades diferentes no Todoist
* [ ] Enviar resumo diário das principais notícias
* [ ] Integrar com Telegram ou WhatsApp
* [ ] Armazenar histórico das notícias processadas
* [ ] Evitar notícias duplicadas
* [ ] Criar um dashboard com estatísticas da automação

## 👨‍💻 Sobre o projeto

Este projeto foi desenvolvido como parte do meu portfólio pessoal para demonstrar conhecimentos práticos em:

**Automação de processos + Inteligência Artificial + Integração de APIs + n8n.**
