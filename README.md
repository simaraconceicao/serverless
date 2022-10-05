# Certificado Quero Ser Dev

Esse projeto foi gerado usando `aws-nodejs-typescript` template do [Serverless framework](https://www.serverless.com/).

Confira a [documentação](https://www.serverless.com/framework/docs/providers/aws/).

Foi um projeto guiado no curso Ignite da Rocketseat no módulo de backend com Node.js nas aulas da maravilhosa Dani Leão.

É uma aplicação que cria e valida um certificado de conclusão de curso gerando uma versão pdf. 

Se liga no resultado abaixo:

![gif animado comportamento](https://media.giphy.com/media/uXW79BbEKRr9xa7SJW/giphy.gif)

## Instruções de instalação

> **Requerido**: NodeJS `lts/fermium (v.14.15.0)`.

### Usando NPM

- Rode `npm i` para instalar as dependências

## Requests

POST LOCALHOST - criação de certificado
```
    curl --request POST \
    --url http://localhost:3000/dev/generateCertificate \
    --header 'Content-Type: application/json' \
    --data '{
        "id": "581a419d-601d-4787-9528-c287b61653b6",
        "name": "Simara Conceição",
        "grade": "10.00"
    }         '

```

GET LOCALHOST - validação/consulta de certificado
```
    curl --request GET \
  --url http://localhost:3000/dev/verifyCertificate/581a419d-601d-4787-9528-c287b61653b6

```


> :warning: Atenção para fazer o deploy em produção você precisa ter uma conta na AWS e ter configurado na sua máquina as credenciais. Mas as configurações desse projeto te permite rodar localmente.

### Localmente

Para rodar o projeto localmente:

- `npm run dev` 
Para instalar o banco de dados localmente:

- `npm install dynamodb:start` 

Para subir o banco de dados localmente:

- `npm run dynamodb:start` 

### Estrutura do projeto

A codebase está na pasta `src`. This folder is divided in:

- `functions` - contém as lambda functions
- `templates` - contém o template do certificado
- `utils` - contém a configuração do DynamoDB e regra para rodar offline

```
.
├── src
│   ├── functions               # Códigos da Lambda Functions
│   │   ├── generateCertificate.ts
│   │   └── verifyCertificate.ts
│   |
│   └── templates               # Template html de certificado
│   |    └── certificate.hbs         
│   |    └── selo.png
│   │   
│   └── utils                   # Dynamodb config
│       └── dynamodbClient.ts      
│
├── package.json
├── serverless.ts               # Serverless service file
├── tsconfig.json               # Typescript compiler configuration
├── tsconfig.paths.json         # Typescript paths
└── webpack.config.js           # Webpack configuration
```

### Tecnologias usadas

 - Typescript
 - Framework serverless
 - AWS Lambda
 - DynamoDb
 - S3
 - puppeteer e chrome-aws-lambda
 - handlebars
 - dayjs

### Vamos nos conectar?

- [youtube](https://www.youtube.com/queroserdev)
- [instagram](https://www.instagram.com/simara_conceicao)
- [linkedin](https://www.linkedin.com/in/simaraconceicao/)
- [github](https://github.com/simaraconceicao)
- [spotify](https://open.spotify.com/show/59vCz4TY6tPHXW26qJknh3)
- [quero ser dev](https://queroserdev.com)

<br>
Feito com 💜 por Simara Conceição

