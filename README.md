# AudioTextBot 🎙️➡️📝

AudioTextBot — это Telegram-бот на Node.js, который принимает голосовые или аудиофайлы и преобразует их в текст с помощью модели Whisper.  
Бот поддерживает множество языков и может быть полезен для изучающих языки, журналистов, студентов и всех, кому нужно быстро расшифровать аудио.

## 🚀 Основные возможности

- Прием аудио (voice, audio, document) от пользователя
- Автоматическая транскрибация через Whisper (`large-v3-turbo`)
- Поддержка множества языков
- Отправка текста прямо в Telegram
- Возможность скачать результат как текстовый файл
- Гибкая настройка логирования
- Возможность запуска в Docker

## 🛠️ Технологии

- Node.js + TypeScript
- Telegram Bot API (`node-telegram-bot-api`)
- Whisper (`nodejs-whisper`)
- Docker
- Winston (для логирования)
- ESLint + Prettier (для качества кода)

## ⚙️ Установка

### Локальный запуск

```bash
git clone https://github.com/yourusername/AudioTextBot.git
cd AudioTextBot
cp .env.example .env   # Настройте переменные окружения
npm install
npm run build
npm start
```

### Запуск в Docker

```bash
# Сборка Docker-образа
docker build -t audiotextaibot .

# Запуск контейнера с передачей переменных окружения и пробросом порта
docker run --name audiotextaibot-srv --env-file .env -p 3001:3001 audiotextaibot
```
