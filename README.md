# Podcast API

API desenvolvida durante um bootcamp da DIO com Node.js e TypeScript. O projeto lista e filtra episódios de podcasts em vídeo, usando o módulo HTTP nativo do Node, sem Express. A aplicação foi criada para praticar rotas, controllers, services, repositories e leitura de dados em um arquivo JSON local.

## Sobre o projeto

Este projeto simula uma pequena API REST para consulta de episódios de podcasts. A ideia é permitir que uma aplicação cliente, como um site ou app, consiga buscar todos os episódios cadastrados ou filtrar os resultados pelo nome do podcast.

Os dados ficam armazenados em:

```txt
src/repositories/podcasts.json
```

## Funcionalidades

- Listar todos os episódios cadastrados.
- Buscar episódios pelo nome do podcast.
- Retornar respostas em formato JSON.
- Organizar o código em camadas para facilitar manutenção e evolução.

## Tecnologias utilizadas

- Node.js
- TypeScript
- TSX
- TSUP
- HTTP nativo do Node.js

## Estrutura

```txt
src/
  app.ts
  server.ts
  controllers/
    podscasts-controller.ts
  models/
    podcast-model.ts
    podcast-transfer-model.ts
  repositories/
    podcasts-repository.ts
    podcasts.json
  routes/
    routes.ts
  services/
    filter-episodes-service.ts
    list-episodes-service.ts
  utils/
    content-type.ts
    http-methods.ts
    status-code.ts
```

## Como rodar

Instale as dependências:

```bash
npm install
```

Crie ou mantenha o arquivo `.env` na raiz do projeto:

```env
PORT=3333
```

Execute em modo desenvolvimento:

```bash
npm run start:dev
```

Se quiser rodar com reinício automático ao salvar alterações:

```bash
npm run start:watch
```

## Rotas da API

### Listar episódios

```http
GET /api/list
```

Exemplo:

```txt
http://localhost:3333/api/list
```

### Filtrar por podcast

```http
GET /api/podcasts?p=flow
```
