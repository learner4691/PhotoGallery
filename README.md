# Photo Gallery API

## Описание

Многофункциональное приложение для загрузки, отображения и управления фотографиями. Поддерживает регистрацию, аутентификацию и персонализированные галереи пользователей.

---

## 🚀 Возможности

- 🔐 Регистрация и вход пользователей
- 📸 Загрузка изображений
- 🖼️ Просмотр всех фото и фото конкретного пользователя
- ❌ Удаление своих фото
- 🔒 Защищённые маршруты (`ProtectedRoute`)
- 🧠 Состояние через Redux 
- ⌛ Загрузка и обработка ошибок
- 📦 Хранение изображений на сервере

## Стек технологий

### Frontend:
- **React** + **React Router v6**
- **Redux**
- **Material UI**
- **Axios**
- **JWT авторизация**
- **ProtectedRoute** для защиты маршрутов
- **Snackbar-уведомления**

## Функционал

### Пользователи:
- Регистрация с email, username 
- Вход с валидацией
- Отображение уведомлений (Snackbar)

### Фотографии:
- Просмотр списка всех фотографий
- Просмотр фотографии во всплывающем popup
- Добавление фотографии только авторизованный пользователь 
- Удаление фотографии только автор 
- Клик на имя автора — отображает фотографии загруженные данным автором
- В меню пользователя "My photos" — отображает фотографии текущего пользователя

---

**Структура компонентов:**
  - `App` — корневой компонент с роутами и layout'ом
  - `Register`, `Login` — формы регистрации и авторизации
  - `Photos`, `UserPhotos`, `NewPhoto` — основная бизнес-логика
  - `Form`, `Loader`, `HasAccess`, `AppToolbar` — вспомогательные UI-компоненты

### Backend:
- **Node.js** + **Express**
- **MongoDB** (mongoose)
- **JWT**
- **Multer** (загрузка изображений)


- Поддержка CRUD операций для фотографий и пользователей
- Хранение изображений и маршруты API:
  - `POST /users` — регистрация
  - `POST /users/sessions` — логин
  - `DELETE /users/sessions` — выход 
  - `POST /photos`, `GET /photos`, `GET /photos/user/:id`, `DELETE /photos/:id`


### 🌐 Порты
- **Frontend**: [http://localhost:3000](http://localhost:3000) (по умолчанию для Create React App)
- **Backend**: [http://localhost:8000](http://localhost:8000) (для API)

<!-- ## 📁 Структура проекта

├── backend/                  # Серверная часть (Express + MongoDB)
│   ├── models/               # Mongoose-модели
│   ├── routes/               # Маршруты Express
│   ├── middleware/           # Middleware-функции (авторизация и др.)
│   ├── public/uploads/       # Загруженные изображения
│   ├── serve    # Изображения для фронтенда
│   ├── src/
│   │   └── imager.js             # Точка входа сервера (Express + MongoDB)
│   ├── fixtures.js           # Генерация начальных данных
│   ├── utils/                # Вспомогательные утилиты

├── frontend/                 # Клиентская часть (React)
│   ├── public/  s/     
│   │   ├── components/       # Компоненты 
│   │   ├── containers/       # Основные страницы
│   │   ├── store/            # Redux store и слайсы
│   │   ├── utils/            # Вспомогательные функции
│   │   ├── App.js            # Главный компонент приложения
│   │   ├── axiosPhoto.js   # Настройка axios для API
│   │   ├── constants.js      # Константы проекта
│   │   ├── index.css         # Глобальные стили приложения
│   │   └── index.js          # Точка входа React-приложения, подключение Redux и маршрутизации
│   └── README.md -->
## 📁 Структура проекта

├── backend/                  # Серверная часть (Express + MongoDB)
│   ├── models/               # Mongoose-модели
│   ├── routes/               # Маршруты Express
│   ├── middleware/           # Middleware-функции (авторизация и др.)
│   ├── public/uploads/       # Загруженные изображения
│   ├── server.js             # Точка входа сервера
│   ├── fixtures.js           # Генерация начальных данных
│   ├── utils/                # Вспомогательные утилиты

├── frontend/                 # Клиентская часть (React)
│   ├── public/
│   │   └── images/           # Изображения для фронтенда
│   ├── src/
│   │   ├── components/       # Компоненты 
│   │   ├── containers/       # Основные страницы
│   │   ├── store/            # Redux store и слайсы
│   │   ├── utils/            # Вспомогательные функции
│   │   ├── App.js            # Главный компонент приложения
│   │   ├── axiosPhoto.js     # Настройка axios для API
│   │   ├── constants.js      # Константы проекта
│   │   ├── index.css         # Глобальные стили
│   │   └── index.js          # Точка входа React-приложения
│   └── README.md


## Установка и запуск

```bash
# Клонирование репозитория
git clone https://github.com/learner4691/PhotoGallery.git

# Корневая директория проекта
cd "PhotoGallery"

# Инициализация сабмодулей (frontend и server)
git submodule update --init --recursive

# Установка зависимостей и запуск Backend
cd "PhotoGallery(server)"
npm install
npm start

# Новое окно в bash
# Корневая директория проекта
cd "PhotoGallery"

# Установка зависимостей и запуск Frontend
cd "PhotoGallery(frontend)"
npm install
npm start

📄 Лицензия
Этот проект распространяется без лицензии и предназначен для свободного использования в учебных целях.
