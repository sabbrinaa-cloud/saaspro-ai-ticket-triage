# SaaSPro AI Ticket Triage

Sistema inteligente de triagem de tickets desenvolvido com n8n, OpenAI, Gmail e Trello.

## Objetivo

Automatizar o recebimento, classificação e tratamento inicial de tickets de suporte técnico utilizando Inteligência Artificial.

---

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

---

## Arquitetura

![Arquitetura](docs/arquitetura.png)

---

## Fluxo

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

## Tecnologias

- n8n
- OpenAI GPT
- Gmail API
- Trello API
- Google Sheets
- HTML
- JSON

## Cenários Testados

### Ticket Técnico

- Classificação correta
- Resposta automática
- Aprovação humana

### Ticket Crítico

- Prioridade crítica
- Escalonamento automático

### Assunto Fora do Escopo

- Bloqueio pelo guardrail
- Email orientativo ao usuário

### LGPD

- Orientação para não envio de dados sensíveis

## Autor

Sabrina Leite de Sá

Analista de Dados | Business Intelligence | Automação com IA
