# Используем Node.js 18 LTS
FROM node:18-alpine

# Рабочая директория внутри контейнера
WORKDIR /app

# Копируем файлы зависимостей
COPY package*.json ./

# Ставим зависимости
RUN npm install

# Копируем остальные файлы проекта
COPY . .

# Сборка статики (будет лежать в /app/build)
RUN npm run build

# Контейнер слушает порт 8000
ENV PORT=8000
EXPOSE 8000

# Старт — запуск dev-сервера
CMD ["npm", "start"]
