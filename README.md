# 🤖 SaaSPro – Intelligent Ticket Triage and Support Automation

Sistema de automação de suporte baseado em Inteligência Artificial, desenvolvido com n8n, OpenAI, Gmail, Trello e Google Sheets.

## 🎯Objetivo

Automatizar o recebimento, classificação e tratamento inicial de tickets de suporte técnico utilizando Inteligência Artificial.

## 📌 Sobre o Projeto

Este projeto demonstra a construção de um fluxo completo de atendimento automatizado utilizando Inteligência Artificial para triagem de tickets.

A solução é capaz de:

- Identificar solicitações válidas de suporte
- Consultar informações de clientes
- Classificar prioridade e categoria
- Gerar respostas automáticas
- Solicitar aprovação humana
- Registrar e acompanhar tickets no Trello

O objetivo é reduzir o tempo de triagem, padronizar respostas e aumentar a eficiência operacional.

## Funcionalidades

- Classificação automática de tickets
- Definição automática de prioridade
- Encaminhamento por equipe responsável
- Consulta de clientes em base corporativa
- Resposta automática gerada por IA
- Aprovação humana antes do envio
- Integração com Gmail
- Integração com Trello
- Controle de prioridades via etiquetas
- Tratamento de assuntos fora do escopo
- Orientação LGPD para conteúdos sensíveis

# 🏗️ Arquitetura da Solução

![Arquitetura Geral](docs/workflow-overview.png)

## 🔍 Visão Geral

O sistema automatiza a triagem inicial de tickets de suporte utilizando Inteligência Artificial, validação de clientes e aprovação humana antes do envio ao usuário.

## 🧩 Componentes

### Gmail

Recebe solicitações de suporte via e-mail.

### n8n

Orquestra todo o fluxo de automação.

### OpenAI

Classifica o ticket, identifica prioridade, equipe responsável e gera resposta sugerida.

### Google Sheets

Base corporativa utilizada para validação de clientes.

### Trello

Centraliza o gerenciamento operacional dos tickets.

## Fluxo Técnico

1. Cliente envia e-mail.
2. Sistema verifica se o assunto pertence ao suporte.
3. Consulta a base corporativa.
4. IA classifica:
   - Categoria
   - Prioridade
   - Equipe responsável
5. Card é criado no Trello.
6. E-mail de aprovação é enviado para a equipe.
7. Analista:
   - Aprova
   - Reprova
8. Sistema:
   - Envia resposta ao cliente
   - Ou encaminha para análise manual

## 📸 Evidências de Execução

### 🔄 Workflow Completo no n8n

![Workflow n8n](docs/ai-triage-engine.png)

### 👤 Aprovação Humana

A resposta gerada pela IA é enviada para validação antes do envio ao cliente.

![Aprovação Humana](docs/human-approval-flow.png)

### 📋 Ticket Resolvido pela IA

Após aprovação, o ticket é movido automaticamente para a coluna correspondente no Trello.

![Trello Board](docs/trello-board.png)

### 📧 E-mail de Aprovação

Mensagem enviada para o analista responsável revisar a resposta sugerida pela IA.

![Email Aprovação](docs/gmail-approval-email1.png)

### 🤖 Resposta Gerada pela IA

Exemplo de resposta construída automaticamente com base na análise do ticket.

![Resposta IA](docs/gmail-approval-email2.png)

### ✅ Aprovação para Envio ao Cliente

Fluxo de confirmação antes da resposta final.

![Aprovação Final](docs/gmail-approval-email3.png)

### 🚫 Tratamento de Assuntos Fora do Escopo

Quando a solicitação não corresponde a suporte técnico, o sistema responde com orientação adequada.

![Email Fora do Escopo](docs/gmail-rejected-email.png)

## 🚀 Benefícios

- Redução do tempo de triagem
- Padronização das respostas
- Governança operacional
- Aprovação humana obrigatória
- Priorização automática
- Integração entre múltiplas plataformas

## 🔀 Fluxo

```text
Novo Ticket
     │
     ▼
Verificação
     │
 ┌───┴────┐
 │        │
Aprovado  Reprovado
 │         │
 ▼         ▼
Agente IA  Email Orientativo
 │
 ▼
Consulta Base Clientes
 │
 ▼
Criação do Card no Trello
 │
 ▼
Aprovação Humana
 │
 ┌───┴────┐
 │        │
Aprovar   Reprovar
 │         │
 ▼         ▼
Cliente   Análise Manual
```

## 🛠️ Stack Tecnológica

- n8n (Workflow Automation)
- OpenAI GPT
- Gmail API
- Trello API
- Google Sheets
- HTML
- JSON

## 🧪 Cenários Testados

### 🎫 Ticket Técnico

- Classificação correta
- Resposta automática
- Aprovação humana

### 🚨 Ticket Crítico

- Prioridade crítica
- Escalonamento automático

### 🚫 Assunto Fora do Escopo

- Bloqueio pelo guardrail
- Email orientativo ao usuário

### 🔒 LGPD

- Orientação para não envio de dados sensíveis

## 📁 Estrutura do Projeto

```text
saaspro-ai-ticket-triage/
│
├── README.md
├── LICENSE
│
├── docs/
│   ├── workflow-overview.png
│   ├── ai-triage-engine.png
│   ├── human-approval-flow.png
│   ├── trello-board.png
│   ├── gmail-approval-email1.png
│   ├── gmail-approval-email2.png
│   ├── gmail-approval-email3.png
│   ├── gmail-rejected-email.png
│   └── Triagem de tickets de IA com aprovação humana.json
│
└── docs/workflow/
```

## 👩‍💻 Autor

**Sabrina Leite de Sá**

Analista de Dados | Business Intelligence | Automação com IA

Tecnologias e Competências:

- Power BI
- SQL
- Python
- n8n
- OpenAI
- Automação de Processos
- ETL
- Analytics

💼LinkedIn: https://www.linkedin.com/in/sabrinaleitedesa/

💻 GitHub: https://github.com/sabbrinaa-cloud

🌐 Portfólio: https://sites.google.com/edu.senai.br/portfolio-sabrina-sa/in%C3%ADcio
