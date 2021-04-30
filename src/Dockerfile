FROM node:14.16.1-alpine3.13
WORKDIR /app

# Qualquer mudanca nos arquivos abaixo irao forcar a reconstrucao das camadas seguintes durante o build.
COPY package*.json ./
RUN npm install

# Todos os arquivos serao copiados exceto o que estiver definido no .dockerignore.
# Lembrar de passar o contexto correto para o Docker Deamon durante o build, que no caso é a pasta src.
COPY . .

EXPOSE 8080
CMD ["node", "app.js"]