# README

# Loans For Good

Este é um projeto que tem como o objetivo a criação de um API para análise e concessão de crédito feita com Django, Postgresql, Redis e Celery no back-end e React no front-end.

Neste repositório encontra-se submódulos tanto do [back-end](https://github.com/MiqueiasRihs/digitalsys-code-challenge/tree/cae12d135f1e466ad1a67e86bfb7888e7ae6e004) quanto do [front-end](https://github.com/MiqueiasRihs/digitalsys-code-challenge-front-end/tree/84f7811ff504b932ec190a4fbc6bdb692910a770), foi feito dessa forma para que ficasse mais fácil de subir todo o sistema com apenas um `docker-compose up`, mas o código de cada parte pode ser encontrada em seus respectivos repositórios.

## Rodando o projeto

Para rodar o projeto, siga os passos abaixo:

1. Clone este repositório em sua máquina local.
2. Com o Docker instalado, execute o comando `docker-compose up`.

O servidor estará disponível em [http://localhost:3000](http://localhost:3000/) com o formulário para ser preenchido, já o back-office estará presente em [http://localhost:8000/admin](http://localhost:8000/admin)

## Acessos

Para acessar o back-office está sendo criado automaticamente um usuário inicial para testes no momento em que o contêiner sobe, os acessos são:

```bash
usuário: admin
senha: admin
```

## Métodos Disponíveis

### POST /analise-de-cliente

Este método recebe um JSON contendo todos os dados solicitados no formulário e encaminha para a API externa de análise de crédito através do Celery. 

### GET /analise-de-cliente

Este método retorna uma lista de campos para serem exibidos e preenchidos no front-end.

## Testes

Os testes unitários são realizados no momento em que o contêiner sobe, mas para rodar os testes no momento de desenvolvimento, você pode:

1. No terminal rodar o comando `pytest`.
