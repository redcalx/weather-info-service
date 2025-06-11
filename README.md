# Weather Info Service

## Overview
<!--The Weather Info Service is a microservice that provides weather information based on city names. It fetches data from an external weather API and serves it through a RESTful interface.-->
Microsserviço desenvolvido em um ambiente linux usando o WSL Ubuntu e AWS para realizar o deploy do serviço. Sua função é provisionar informações climáticas através de uma API externa do OpenWeatherMap.org buscando através de nomes de cidades e os servindo através de uma interface RESTful. 

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
   git clone <repository-url>
   cd weather-info-service
   ```

2. **Instalar Dependências**
   Certifique se o  Node.js está instalado. Depois rode o comando:
   ```bash
   npm install
   ```

3. **Configurar Variáveis de Ambiente**
   Crie um arquivo `.env` no diretório raiz e adicione suas chaves API e outras configurações:
   ```
   WEATHER_API_KEY=sua_chave_api_aqui
   ```

4. **Rode o Serviço Localmente**
   You can start the service locally using:
   ```bash
   npm start
   ```

5. **Deploying to AWS**
   To deploy the service using the Serverless Framework, ensure you have the Serverless CLI installed and configured. Then run:
   ```bash
   serverless deploy
   ```

## Usage
Once the service is running, you can make requests to get weather information. For example:
```
GET /weather?city=Tokyo
```

## Contributing
Feel free to submit issues or pull requests if you would like to contribute to the project.

## License
This project is licensed under the MIT License.