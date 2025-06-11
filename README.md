# Weather Info Service

## Overview
<!--The Weather Info Service is a microservice that provides weather information based on city names. It fetches data from an external weather API and serves it through a RESTful interface.-->
Microsserviço desenvolvido em ambiente Linux (WSL com Ubuntu) e implantado na AWS. Sua principal função é fornecer informações metereológicas obtidas a partir da API externa do OpenWeatherMap.org, com base em nomes de cidades, expondo os dados por meio de uma interface RESTful. O serviço é projetado para ser escalável, modular e facilmente integrável com outras aplicações.

Microservice developed in a Linux environment (WSL with Ubuntu) and deployed on AWS. Its main function is to provide weather information retrieved from the external API of OpenWeatherMap.org, based on city names, exposing the data through a RESTful interface. The service is designed to be scalable, modular, and easily integrable with other applications.

## Estrutura do Projeto 
```
weather-info-service
├── src
│   ├── index.js
│   ├── lambda.js
│   ├── services
│   │   └── weatherService.js
│   ├── controllers
│   │   └── weatherController.js
│   └── utils
│       └── apiClient.js
├── package.json
├── serverless.yml
├── .env
└── README.md
```

## Configuração

1. **Clonar o Repositório**
   ```bash
   git clone <repositorio-url>
   cd weather-info-service
   ```

2. **Instalar Dependências**
   Certifique se o Node.js está instalado. Depois rode o comando:
   ```bash
   npm install
   ```

3. **Configurar Variáveis de Ambiente**
   Crie um arquivo `.env` no diretório raiz e adicione suas chaves API e outras configurações:
   ```
   WEATHER_API_KEY=sua_chave_api_aqui
   ```

4. **Rodando o Serviço Localmente**
   Você pode iniciar o service localmente usando:
   ```bash
   npm start
   ```

5. **Deploy na AWS**
   Para fazer o deploy do serviço usando o framework Serverless, certifique-se de que você tem o Serverless CLI instalado e configurado. Depois, rode:
   ```bash
   serverless deploy
   ```

## Uso
Quando o serviço já estiver rodando, você pode fazer requests para conseguir informações sobre o clima. Por exemplo:
```
GET /weather?city=Tokyo
```

## License
This project is licensed under the MIT License.