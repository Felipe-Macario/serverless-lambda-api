# API REST usando Serverless

Este repositório consiste em um estudo sobre API feita em Node.js usando serverless framework.

# Tecnologias usadas

- Node.js
- Serverless Framework
- AWS Lambda
- DynamoDB

# Criando o projeto

Este estudo foi focado para ser aplicado na AWS. Caso tenham curiosidade de criar o projeto e rodar localmente podem usar esses plugins: [Serverless Offline Plugin](https://www.serverless.com/plugins/serverless-offline) e [Serverless DynamoDB Plugin](https://www.serverless.com/plugins/serverless-dynamodb-local)

### Requisitos

- Node.js
- NPM
- Uma conta na [AWS](https://aws.amazon.com/pt/console/) - Vai precisar de uma conta na AWS para rodar este projeto.
- [Serverless framework](https://www.serverless.com/) - Pode ser instalado usando o comando `npm install -g serverless`

### Fazendo o deploy

1. Use o NPM para instalar os pacotes necessários `npm install`
2. Crie uma conta de acesso programático com acesso de admin no [IAM](https://console.aws.amazon.com/iam/home) da AWS e pegar a chave e a secret.
3. Configure o serverless para usar essa conta, isso pode ser feito usando o serverless no terminal: `serverless config credentials -o --provider aws --key <chave> --secret <secret>`
4. Fazer deploy usando o comando `serverless deploy`
5. Após utilizar o comando `serverless deploy`, vai aparecer as URLs que podemos usar para testar as APIs criadas.

Ao fazer o deploy, é interessante olhar o que foi criado nos seguintes serviços no console:

- Cloud Formation
- S3
- Lambda
- API Gateway
- DynamoDB

Caso de algum erro e queira ver os logs das Lambdas, vá até o detalhe de uma delas e na aba `Monitoramento` no serviço de Lambda, clique em `Visualizar logs no CloudWatch`.
