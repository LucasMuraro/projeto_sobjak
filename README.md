Projeto IoT Agro - API, Front-End e Mensageria

O Projeto IoT Agro é uma aplicação completa desenvolvida para integrar dispositivos IoT voltados ao agronegócio. O sistema possibilita o monitoramento e controle de condições agrícolas, como temperatura, umidade e localização, promovendo uma gestão mais eficiente de propriedades rurais.

🔧 Tecnologias Utilizadas

Backend

Java 17: Linguagem de programação principal.

Spring Boot: Framework utilizado para o desenvolvimento da API REST.

JWT (JSON Web Token): Autenticação e autorização seguras.

MQTT (Message Queuing Telemetry Transport): Comunicação em tempo real com dispositivos IoT.

PostgreSQL: Banco de dados para persistência das informações.

Swagger/OpenAPI: Documentação interativa da API.

Frontend

React: Desenvolvimento da interface web para interação com os dados da API.

Mensageria

Node.js: Implementação de serviços de mensageria para integração e comunicação assíncrona.

DevOps

Docker: Contêinerização das aplicações para facilitar a implantação.

CI/CD: Pipeline de integração e entrega contínua.

📁 Estrutura do Projeto

Models

As principais entidades do sistema incluem:

Atuador: Representa os dispositivos atuadores utilizados nas propriedades agrícolas.

Dispositivo: Dispositivos IoT conectados ao sistema.

Gateway: Hub central de gerenciamento dos dispositivos IoT.

Leitura: Dados coletados pelos sensores (temperatura, umidade, etc.).

Pessoa: Usuários do sistema.

Sensor: Sensores que coletam os dados ambientais.

Controllers

Principais controladores da API:

AuthController: Gerencia autenticação e geração de tokens JWT.

GatewayController: Operações CRUD para gateways IoT.

DispositivoController: Gerenciamento de dispositivos IoT.

SensorDataController: Manipulação de dados coletados pelos sensores.

Mensageria: Implementado em Node.js para comunicação em tempo real.

🛠 Segurança

A autenticação e autorização são realizadas via JWT:

Autenticação: Usuários obtêm um token JWT ao fazer login no endpoint /api/auth/login.

Autorização: Endpoints protegidos exigem o envio do token no cabeçalho Authorization no formato Bearer <TOKEN>.

🚀 Como Rodar o Projeto

Pré-requisitos

Java 17

Maven 3.9+

Node.js

Docker

PostgreSQL

Passos

Clone o repositório:

git clone <URL_DO_REPOSITORIO>
cd projeto-iot-agro

Configure o arquivo application.properties:

spring.datasource.url=jdbc:postgresql://localhost:5432/agro_radar
spring.datasource.username=SEU_USUARIO
spring.datasource.password=SUA_SENHA
jwt.secret=SUA_CHAVE_SECRET_BASE64
jwt.expiration-ms=86400000

Execute a aplicação com Docker Compose:

docker-compose up --build

Acesse a aplicação:

API Backend: http://localhost:8080

Frontend React: http://localhost:3000

Swagger UI: http://localhost:8080/swagger-ui/index.html

📌 Funcionalidades Principais

Autenticação segura com JWT.

CRUD de entidades como gateways, dispositivos e sensores.

Comunicação em tempo real via MQTT.

Interface web amigável para gerenciar dispositivos e visualizar dados.

Contêinerização e orquestração com Docker.

CI/CD automatizado para facilitar o desenvolvimento.

👥 Participantes do Projeto
Alexssander Liesenfeld

Fábio Thumang Longhitano

Lucas Muraro Pietruchalek

Caso tenha dúvidas ou sugestões, fique à vontade para contribuir!

