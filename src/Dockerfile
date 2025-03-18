FROM node:22.14.0
WORKDIR /app
COPY package*.json ./
RUN npm install
# O comando COPY . . serve para copiar os arquivos 'código' para a imagem, e ele vem depois do package.json e npm install porque
# se eu alterar o código, não vou precisar copiar todas dependencias do package.json e instalar elas novamente. Esse processo
# de rodar novamente o package.json e npm install só vai acontecer se eu alterar alguma dependencia/pacote do projeto
COPY . .
CMD ["node", "server.js"]