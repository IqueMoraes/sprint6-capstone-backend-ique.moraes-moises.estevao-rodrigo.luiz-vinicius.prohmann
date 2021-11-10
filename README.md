# sprint6-capstone-backend-ique.moraes-moises.estevao-rodrigo.luiz-vinicius.prohmann

# json-server-base

Esse é o repositório com a base de JSON-Server + JSON-Server-Auth já configurada, feita para ser usada no desenvolvimento das API's nos Capstones do Q2.

## Endpoints

### Cadastro

POST /register <br/>

### Login

POST /login <br/>

### Adverts

Neste endpoint é possivel visualizar todos os anuncios

`GET- /adverts`

Authorization: ` Bearer Token`

`FORMATO DA RESPOSTA - STATUS 201`

```json
[
  {
    "userId": 1,
    "date": "10/11/2021",
    "localization": "São Paulo - SP",
    "description": "generc description",
    "name": "Manutenção de geladeira",
    "category": "Serviços",
    "id": 1
  }
]
```

`Post- /adverts`

para criar um novo anuncio é necessário passar a chave "UserID"

Authorization: ` Bearer Token`

`FORMATO DA REQUISIÇÃO - STATUS 201`

```json
{
  "date": "10/11/2021",
  "localization": "São Paulo - SP",
  "description": "generc description",
  "name": "TEste",
  "category": "Serviços",
  "userId": 1
}
```

`FORMATO DA RESPOSTA - STATUS 201`

```json
{
  "date": "10/11/2021",
  "localization": "São Paulo - SP",
  "description": "generc description",
  "name": "TEste",
  "category": "Serviços",
  "userId": 1,
  "id": 2
}
```

### Routines

Neste endpoint é possivel verificar as rotinas dos usuários

`GET- /routines`

Authorization: ` Bearer Token`

`FORMATO DA RESPOSTA - STATUS 201`

```json
[
  {
    "userId": 1,
    "date": "10/11/2021",
    "localization": "São Paulo - SP",
    "description": "generc description",
    "name": "Manutenção de geladeira",
    "category": "Serviços",
    "id": 1
  }
]
```

`Post- /routines`

para criar uma nova rotina é necessário passar o "UserId"

Authorization: ` Bearer Token`

`FORMATO DA REQUISIÇÃO - STATUS 201`

```json
{
  "name": "Molhar as Plantas",
  "category": "habitos",
  "achieved": false,
  "how_much_achieved": 0,
  "userId": 1
}
```

`FORMATO DA RESPOSTA - STATUS 201`

```json
{
  "id": 1,
  "name": "Molhar as Plantas",
  "category": "habitos",
  "achieved": false,
  "how_much_achieved": 0,
  "userId": 1
}
```

### Forum

`GET- /forum`
