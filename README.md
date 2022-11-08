# CUCOHealth - Clients API

API para o desafio front end CUCOHealth. 

Created with [JSON Server](https://www.npmjs.com/package/json-server).

## Instalação

**Clone o repositório**

```
$ git clone https://github.com/cucohealth-clients-api.git
$ cd cucohealth-clients-api
```

**Instale as dependências**

```
$ npm install
```

**Inicie a API**

```
$ npm run start
```

## Documentação

Postman Collection: [CUCOHealth - Clients API.postman_collection.json](#)

**Rotas**

```
GET    /clients
GET    /clients/:id
POST   /clients
PUT    /clients/:id
PATCH  /clients/:id
DELETE /clients/:id
```

**Filtros**

Utilize `_like` para buscar em campos especificos

```
GET /clients?name_like=Tiago
```
```
GET /clients?cpf_like=530.124.692-57
```

Ou utilize `q` para buscar em todos os campos

```
GET /clients?q=Tiago
```

**Paginação**

Utilize `_page` e `_limit` (opcional) para paginar os dados retornados.

No response o header retorna os valores `Link` e `X-Total-Count` onde há os links `first`, `prev`, `next`, `last` e total de registros na API.

```
GET /clients?_page=7
GET /clients?_page=7&_limit=20
```

_10 itens são retornados por padrão_

**Ordenação**

Utilize os parâmetros `_sort` e `_order` (ordem crescente por padrão)

```
GET /clients?_sort=name&_order=asc
```

Made with 💙 at CUCOHealth
