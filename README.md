# SaaSPro – Intelligent Ticket Triage and Support Automation

Sistema de automação de suporte baseado em Inteligência Artificial, desenvolvido com n8n, OpenAI, Gmail, Trello e Google Sheets.

## Objetivo

Automatizar o recebimento, classificação e tratamento inicial de tickets de suporte técnico utilizando Inteligência Artificial.

## Sobre o Projeto

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

## Arquitetura da Solução

## Visão Geral

O sistema automatiza a triagem inicial de tickets de suporte utilizando Inteligência Artificial, validação de clientes e aprovação humana antes do envio ao usuário.

## Componentes

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

## Fluxo operacional

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

## Benefícios

- Redução do tempo de triagem
- Padronização das respostas
- Governança operacional
- Aprovação humana obrigatória
- Priorização automática
- Integração entre múltiplas plataformas

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

## Stack Tecnológica

- n8n (Workflow Automation)
- OpenAI GPT (Inteligência Artificial)
- Gmail API (Comunicação)
- Trello API (Gestão de Tickets)
- Google Sheets (Base de Clientes)
- HTML (Templates de E-mail)
- JSON (Estrutura de Dados)

## Cenários Testados

### Ticket Técnico

- Classificação correta da solicitação
- Identificação da equipe responsável
- Geração automática de resposta
- Aprovação humana antes do envio

### Ticket Crítico

- Classificação como prioridade crítica
- Aplicação automática da etiqueta correspondente
- Escalonamento para equipe responsável

### Assunto Fora do Escopo

- Bloqueio pelo guardrail de validação
- Não encaminhamento para a IA
- Envio de e-mail orientativo ao usuário

### LGPD

- Identificação de solicitação inadequada
- Orientação para não compartilhamento de dados sensíveis
- Preservação das boas práticas de segurança da informação

## Resultados

A solução demonstrou a capacidade de:

- Automatizar a triagem inicial de tickets
- Reduzir atividades manuais repetitivas
- Padronizar respostas ao cliente
- Aplicar critérios de priorização automaticamente
- Integrar múltiplas plataformas em um único fluxo
- Manter supervisão humana em decisões críticas

## Autor

**Sabrina Leite de Sá**

Analista de Dados | Business Intelligence | Automação com IA

**Competências:**

- Power BI
- SQL
- Python
- n8n
- OpenAI
- Automação de Processos
