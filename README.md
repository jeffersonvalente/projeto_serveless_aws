A aplicação vai ser uma API para poder criar, atualizar, listar e deletar (POST, PUT, GET, DELETE) itens de uma lista de tarefas.

# Objetivo:

A aplicação vai ser uma API para poder criar, atualizar, listar e deletar (POST, PUT, GET, DELETE) itens de uma lista de tarefas.

![diagram](https://user-images.githubusercontent.com/73920079/204959857-08c7beb1-caac-4bb9-a968-3296c3025d78.png)

Ela vai envolver vários serviços da aws como:

Para a API o Amazon API Gateway,

Para a autenticação o Amazon Cognito,

O banco de dados vai ser o Amazon DynamoDB,

As lambdas vão colocar os logs no Amazon Cloudwatch,

Por fim um micro-serviço que vai ser acionado toda vez que um arquivo for colocado dentro do S3, disparando a lambda responsável por criar de forma assíncrona um tópico no SNS.

O SNS dispara a lambda responsável por colocar o dado no banco de dados.
