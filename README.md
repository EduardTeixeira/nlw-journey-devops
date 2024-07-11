# nlw-journey-devops

Tecnologia: Go

Versão: 1.22.4

Porta: 8080

Banco: postgres


# DEV

  Preparação:

    - instalar libs (go mod download && go mod verify)

  Execução:

    - rodar app (go run cmd/journey/journey.go)


# PROD

  Preparação:

    - instalar libs (go mod download && go mod verify)

    - buildar (go build cmd/journey/journey.go)

  Execução:

    - rodar app (journey.exe)

# RODAR DOCKER NO AMBIENTE LOCAL

docker build -t api-journey:v1 .

docker run -d -p 8080:8080 api-journey:v1


docker build -t api-journey:v2 .

docker run -d -p 8080:8080 api-journey:v2


docker-compose up --build -d

# GITHUB
Necessário criar duas configurações dentro do repositório do GitHub, dentro de "Settings > Security > Actions" vamos criar duas variáveis na aba de "Secrets" com os seguintes valores

DOCKERHUB_USERNAME => seu nome de usuário do docker_hub

DOCKERHUB_TOKEN => esse token deve ser gerado dentro do docker_hub