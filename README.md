# Automação de Testes de API - Login

Este é um projeto cujo objetivo principal é desenvolver as habilidades práticas em automação dos testes de API com diferentes conjuntos de dados, validação dos resultados e a criação de um pipeline de CI/CD utilizando o Git Actions para executar e validar as Collections no Postman de forma automatizada.

---------

### URL Base:
https://postman-treinamento.qacoders-academy.com.br/api

---------

## Postman

Através do Postman, foram criadas as seguintes Collections:
- Signup;
- Login.

---------

Na **collection signup**, nós precisamos dos seguintes dados:
- Nome Completo;
- Email;
- Senha;
- Perfil de Acesso.

Então, na aba _Pre-request_ foram criados scripts para automatizar a criação de massa de dados para os parâmetros:
- Nome Completo;
- Email;
- Perfil de Acesso.

Já os parâmetros Senha e Perfil de Acesso foram definidos em variáveis glabais e de ambiente, respectivamente.

Na aba _Post-response_ foram criados scripts de teste para certificar que não acontecesse nenhum erro na validação dos parâmetros.

---------

Na collection login, nós precisamos dos seguintes dados:
- Email;
- Senha.

Como a geração da massa de dados já foi automatizada na collection signup, então já temos os dados para os testes do login. 

Na aba _Post-response_ foram mantidos os mesmos scripts de teste utilizados na collection singup.

---------

## GitHub Actions

Ao final, as collections foram integradas a um pipeline de CI/CD no GitHub Actions para garantir que todos os testes serão automaticamente realizados ao realizar alterações no repositório.
