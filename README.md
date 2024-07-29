# WebChat API

Esta é uma aplicação de WebChat construída com Spring Boot, WebSocket e Lombok. A aplicação permite que usuários se conectem a uma sala de chat pública, enviem mensagens e vejam quando outros usuários entram ou saem do chat.

## Funcionalidades

- Enviar e receber mensagens em tempo real
- Notificação quando um usuário entra ou sai do chat
- Interface de usuário simples para interação com o chat

## Tecnologias Utilizadas

- Spring Boot
- Spring WebSocket
- Lombok
- STOMP
- SockJS
- Swagger

## Estrutura do Projeto

```plaintext
src
├── main
│   ├── java
│   │   └── com
│   │       └── edivan
│   │           └── chat
│   │               ├── config
│   │               │   └── WebSocketEventListener.java
│   │               ├── controller
│   │               │   ├── ChatController.java
│   │               │   ├── ChatMessage.java
│   │               │   └── MessageType.java
│   ├── resources
│   │   └── static
│   │       └── index.html
│   └── js
│       └── main.js
 ```

## Endpoints da API

### Enviar Mensagem

POST /app/chat.sendMessage

{
"sender": "string",
"content": "string",
"type": "CHAT"
}

### Adicionar usuário

POST /app/chat.addUser

{
"sender": "string",
"type": "JOIN"
}