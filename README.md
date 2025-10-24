# Projeto: Serviço de IA com Spring Boot + LangChain4j + Gemini

Este projeto foi desenvolvido durante o vídeo [**Aprenda IA com Java LangChain4j | Arquitetura Spring Boot + Gemini na prática**](https://www.youtube.com/watch?v=A5i7D7RAPA4), da Michelli Brito.  
O objetivo é demonstrar como integrar **Inteligência Artificial (IA)** a uma aplicação **Java com Spring Boot**, utilizando o **LangChain4j** e o modelo **Gemini**, criando um fluxo inteligente capaz de processar solicitações e acionar ferramentas internas com base no contexto.

---

## ? Objetivo

Criar um **serviço inteligente** em Java que:
- Conecta o backend Spring Boot com um modelo LLM (Gemini através da API do Google AI);
- Processa requisições textuais de usuários;
- Decide dinamicamente se deve apenas responder com o LLM ou acionar lógicas internas;
- Demonstra a arquitetura base para agentes e fluxos RAG (Retrieval-Augmented Generation) em Java.

---

## ?? Arquitetura do Projeto

A aplicação segue uma estrutura modular com os seguintes componentes principais:

| Componente | Descrição |
|-------------|------------|
| **AssistantAIService** | Interface principal anotada com `@AiService`, responsável por intermediar a comunicação entre o usuário, o modelo LLM e as ferramentas internas. |
| **AssistantTools** | Classe que define métodos Java anotados com `@Tool`, que podem ser executados pelo serviço de IA conforme o contexto da requisição. |
| **AssistantConfig** | Classe de configuração com conexão ao modelo Gemini via API Key e associação entre o AI Service e suas ferramentas. |
| **AssistantController** | Endpoint REST (`/api/assistant`) que recebe requisições dos usuários e retorna respostas geradas dinamicamente. |

---

## ?? Tecnologias Utilizadas

- **Java 25 (LTS)**
- **Spring Boot 3.5.6**
- **LangChain4j**
- **Gemini API (Google AI Studio)**
- **Maven**
- **Postman (para testes de requisições)**

---

## ? Dependências Principais

Configuradas no arquivo `pom.xml`: Spring Boot Starter Web, LangChain4j Core, LangChain4j Gemini.

