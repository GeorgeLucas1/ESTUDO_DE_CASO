# Arquitetura de API em Node.js (Node puro)

## Fluxo de uma requisição HTTP

CLIENTE  
↓ faz requisição  
ROUTER (definição de rotas) — seleciona o endpoint  
↓  
MIDDLEWARE (validação e controle) — valida dados, autenticação, autorização  
↓  
CONTROLLER (orquestração) — recebe a requisição e coordena o fluxo  
↓  
SERVICE (regras de negócio) — aplica regras e casos de uso  
↓  
REPOSITORY (acesso a dados) — consulta e persiste informações  
↓  
DATABASE (persistência) — armazena e retorna dados  
↓  
Resposta retorna pelo mesmo caminho até o CLIENTE

## Responsabilidades

- **Router**: mapeia métodos HTTP e URLs para controllers.
- **Middleware**: validações genéricas, autenticação, autorização,schemas, logs.
- **Controller**: entrada e saída da API (req/res).
- **Service**: regras de negócio e casos de uso.
- **Repository**: abstração de acesso ao banco.
- **Database**: persistência de dados.

## Observação

Esse padrão é compatível com princípios de separação de responsabilidades e Clean Architecture.




