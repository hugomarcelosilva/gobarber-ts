<h1 align="center">
  <img alt="GoBarber" title="gobarber" src=".github/logo.svg" width="200px" />
</h1>

<h3 align="center">
  GoBarber: back-end, front-end web e mobile
</h3>

<p align = "center">
<a href="https://www.codefactor.io/repository/github/hugo-marcelo/gobarber-ts"><img src="https://www.codefactor.io/repository/github/hugo-marcelo/gobarber-ts/badge" alt="CodeFactor" /></a>
<img alt = "Última confirmação do Github" src = "https://img.shields.io/github/last-commit/hugo-marcelo/gobarber-ts">
<img alt = "Idioma principal do GitHub" src = "https://img.shields.io/github/languages/top/hugo-marcelo/gobarber-ts">
<img alt = "GitHub" src = "https://img.shields.io/github/license/hugo-marcelo/gobarber-ts.svg">
<a href="https://www.codacy.com/manual/hugo-marcelo/gobarber-ts?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=hugo-marcelo/gobarber-ts&amp;utm_campaign=Badge_Grade"><img src="https://api.codacy.com/project/badge/Grade/147d0b2836734c79b7ee5ea035f065b4"/></a>
</p>

<h3 align="center">
  <a href="https://insomnia.rest/run/?label=GoBarber&uri=https%3A%2F%2Fraw.githubusercontent.com%2Fhugo-marcelo%2Fgobarber-ts%2Fmaster%2Fbackend%2FInsomnia.json" target="_blank"><img src="https://insomnia.rest/images/run.svg" alt="Run in Insomnia"></a>
</h3>

## :gear: Back-end

### :information_source: Deploy

- https://gobarber-ts-api.herokuapp.com

### :information_source: Instruções Back-end

#### :whale: Executando com Docker Compose

```bash
# instalar os contâineres da API, PostgreSQL, MongoDB e Redis
docker-compose up -d
```

#### :whale: Executando com Docker localmente

```bash
# instalar PostgreSQL - Banco de dados principal
docker run --name gobarber -e POSTGRES_PASSWORD=docker -p 5432:5432 -d postgres

# instalar MongoDB - Banco de dados para notificações
docker run --name mongodb -p 27017:27017 -d -t mongo

# instalar Redis - Banco de dados para filas
docker run --name redis -p 6379:6379 -d -t redis:alpine

# instalar os pacotes e dependências
yarn
```

---

#### Executando back-end

```bash

# criar estrutura do banco de dados Postgres
yarn typeorm migration:run

# iniciar servidor da aplicação
yarn dev:server

```

---

## :computer: Front-end

### :information_source: Deploy

- https://gobarber-ts-web.herokuapp.com

### :information_source: Instruções Front-end

```bash
#instalar os pacotes e dependências
yarn

# iniciar a aplicação web
yarn start
```

---

## :iphone: Mobile

### :information_source: Instruções Mobile (iOS)

```bash
#instalar os pacotes e dependências
yarn

# iniciar o aplicativo no emulador do iOS
yarn ios
```

### :information_source: Instruções Mobile (Android)

```bash
#instalar os pacotes e dependências
yarn
```

Alterar a variável baseURL em `/src/services/api.js` colocando o ip local ou do emulador

```bash
# inicializar o aplicativo no emulador do Android
yarn android
```

---

## :memo: Licença

Esse projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

---

## :clap: Obrigado

[Rocketseat](https://rocketseat.com.br/) pelo bootcamp!
