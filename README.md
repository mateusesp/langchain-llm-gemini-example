# Projeto: Servi�o de IA com Spring Boot + LangChain4j + Gemini

Este projeto foi desenvolvido durante o v�deo [**Aprenda IA com Java LangChain4j | Arquitetura Spring Boot + Gemini na pr�tica**](https://www.youtube.com/watch?v=A5i7D7RAPA4), da Michelli Brito.  
O objetivo � demonstrar como integrar **Intelig�ncia Artificial (IA)** a uma aplica��o **Java com Spring Boot**, utilizando o **LangChain4j** e o modelo **Gemini**, criando um fluxo inteligente capaz de processar solicita��es e acionar ferramentas internas com base no contexto.

---

## ? Objetivo

Criar um **servi�o inteligente** em Java que:
- Conecta o backend Spring Boot com um modelo LLM (Gemini atrav�s da API do Google AI);
- Processa requisi��es textuais de usu�rios;
- Decide dinamicamente se deve apenas responder com o LLM ou acionar l�gicas internas;
- Demonstra a arquitetura base para agentes e fluxos RAG (Retrieval-Augmented Generation) em Java.

---

## ?? Arquitetura do Projeto

A aplica��o segue uma estrutura modular com os seguintes componentes principais:

| Componente | Descri��o |
|-------------|------------|
| **AssistantAIService** | Interface principal anotada com `@AiService`, respons�vel por intermediar a comunica��o entre o usu�rio, o modelo LLM e as ferramentas internas. |
| **AssistantTools** | Classe que define m�todos Java anotados com `@Tool`, que podem ser executados pelo servi�o de IA conforme o contexto da requisi��o. |
| **AssistantConfig** | Classe de configura��o com conex�o ao modelo Gemini via API Key e associa��o entre o AI Service e suas ferramentas. |
| **AssistantController** | Endpoint REST (`/api/assistant`) que recebe requisi��es dos usu�rios e retorna respostas geradas dinamicamente. |

---

## ?? Tecnologias Utilizadas

- **Java 25 (LTS)**
- **Spring Boot 3.5.6**
- **LangChain4j**
- **Gemini API (Google AI Studio)**
- **Maven**
- **Postman (para testes de requisi��es)**

---

## ? Depend�ncias Principais

Configuradas no arquivo `pom.xml`: Spring Boot Starter Web, LangChain4j Core, LangChain4j Gemini.

