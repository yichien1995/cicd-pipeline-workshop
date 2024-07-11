# Simple Web

Just for CICD pipeline workshop

## Environment

- NodeJS v22

## How to run

```bash
npm install

cp .env.example .env
# edit .env

node src/server.js
```

### API

- GET /
- GET /db

## How to lint & Prettier

```bash
./node_modules/.bin/eslint .

./node_modules/.bin/prettier --write .
```

## How to test

```bash
./node_modules/.bin/mocha --reporter spec

# Generate HTML reporter
./node_modules/.bin/mocha --reporter mochawesome

# Generate Code Coverage Report
./node_modules/.bin/nyc --reporter=html ./node_modules/.bin/mocha --reporter mochawesome
```
