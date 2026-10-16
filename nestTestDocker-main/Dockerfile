# Базовый образ на основе которого будет робить приложение
FROM node:20
#расположение файлов внутри контейнера
WORKDIR /usr/src/app
#копирование файлов
COPY package*.json ./
#установка зависимостей
RUN npm ci

COPY . .

RUN npm run build

EXPOSE 3000

CMD ["node", "dist/main"]

