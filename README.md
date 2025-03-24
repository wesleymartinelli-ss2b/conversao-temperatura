# Projeto conversão de temperatura
URL: https://github.com/KubeDev/conversao-temperatura

### Sobre o projeto
O projeto conversão de temperatura é um projeto desenvolvido em NodeJS. O projeto tem como objetivo ser um exemplo para a criação de ambiente com containers usando NodeJS.

### Observações do projeto
A aplicação é exposta usando a porta 8080

# Preparando o Container
docker container run --name conversao -it -p 8080:8080 ubuntu /bin/bash
apt-get update
apt-get upgrade -y
apt-get install -y curl
curl -fsSL https://deb.nodesource.com/setup_23.x -o nodesource_setup.sh
chmod +x nodesource_setup.sh
./nodesource_setup.sh
apt-get install -y nodejs
node -v


# Vamos usar o Docker Container Copy para enviar a aplicação para o container
# Abra um novo terminal e acesso o diretório src
docker container cp . 64f35664a98e:/app --> Vai copiar tudo que está no diretório corrente para o container ID = 64f35664a98e no diretório /app

# Acesse o container e o diretório /app
npm install

# Executando a aplicação no Container
node server.js