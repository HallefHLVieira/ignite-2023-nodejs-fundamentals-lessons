![GitHub repo size](https://img.shields.io/github/repo-size/HallefHLVieira/ignite-2023-nodejs-fundamentals-lessons)

## 📝 ignite-2023-nodejs-fundamentals-lessons 🇺🇸️ 🇬🇧️
This is a API whitout external deps.

## 📝 ignite-2023-fundammentos-de-nodejs-exercicios 🇧🇷️ 🇵🇹️

Este é um projeto construído por meio das aulas do módulo 01 da trilha 2023 de NodeJS.

- Este módulo foi focado em entender como funciona:
- [x] streams
- [x] regex
- [x] métodos http
- [x] banco de dados em arquivo

- Para melhor entendimento, o projeto foi desenvolvido sem nenhuma dependẽncia externa, foi utilizado apenas libs dos próprio NodeJS.

### 🚀 Executando o projeto <01-fundamentos-nodejs>

- Para instalar o <01-fundamentos-nodejs> não requer nenhum comando específico.
- Para executa-lo basta usar o comando: 
```
npm run dev
```

#### Rotas da aplicação

- Esse projeto possui quatro rotas básicas: Criar, editar, buscar e deletar um registro no banco.
- Segue abaixo o Curl de cada endpoint para testes.

- Para criar um novo registro, será necessário informar 2 parâmmetros no body da request
```
curl --request POST \
  --url http://localhost:3333/users \
  --header 'Content-Type: application/json' \
  --data '{
	"name": "{SEU_NOME}",
	"email": "{SEU_EMAIL}"
}'
```

- Para buscar um registro, será necessário informar 1 parâmetro como query params
``` 
curl --request GET \
  --url 'http://localhost:3333/users?%20search={NOME_DO_REGISTRO}' \
  --header 'Content-Type: application/json'
```

- para editar um registro, será necessário informar os parâmetros no body da request + id do registro na rota da request
```
curl --request PUT \
  --url http://localhost:3333/users/{UUID_AQUI} \
  --header 'Content-Type: application/json' \
  --data '{
	"name": "{SUA_ALTERAÇÃO}",
	"email": "{SUA_ALTERAÇÃO}"
}'
```
- Para deletar um registro, será necessário informar o id do registro na rota da request
```
curl --request DELETE \
  --url http://localhost:3333/users/{UUID_AQUI} \
  --header 'Content-Type: application/json'
```