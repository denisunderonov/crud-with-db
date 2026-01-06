# Список контактов (PHP + MySQL)

Веб-приложение для управления базой данных клиентов с полным CRUD функционалом.

## 🚀 Технологии

- **PHP** - серверная логика
- **MySQL** - база данных
- **HTML5/CSS3** - интерфейс
- **Vanilla JavaScript** - клиентская интерактивность

## 📋 Функционал

**Основные возможности:**
- ✅ Просмотр всех записей (viewer.php)
- ✅ Добавление новых контактов (add.php → form.php)
- ✅ Редактирование записей (edit.php → form_edit.php → edit_record.php)
- ✅ Удаление записей (delete.php → delete_record.php)

**Поля базы данных:**
- Фамилия, Имя, Отчество
- Пол (выбор из списка)
- Дата рождения
- Номер телефона
- Email

## ��️ Структура БД

**База данных:** `notebook`  
**Таблица:** `clients`

```sql
CREATE DATABASE notebook;
USE notebook;

CREATE TABLE clients (
  id INT AUTO_INCREMENT PRIMARY KEY,
  surname VARCHAR(100),
  name VARCHAR(100),
  lastname VARCHAR(100),
  gender VARCHAR(20),
  birthday DATE,
  phone VARCHAR(20),
  email VARCHAR(100)
);
```

## 📁 Структура проекта

```
notelist-PHP-JS-MySQL/
├── index.php           # Главная страница
├── menu.php            # Навигационное меню
├── data.php            # Подключение к БД
├── viewer.php          # Просмотр всех записей
├── add.php             # Форма добавления
├── form.php            # Обработка добавления
├── edit.php            # Выбор записи для редактирования
├── form_edit.php       # Форма редактирования
├── edit_record.php     # Обработка редактирования
├── delete.php          # Выбор записи для удаления
├── delete_record.php   # Обработка удаления
└── style.css           # Стили
```

## ⚙️ Установка и запуск локально

1. **Установите XAMPP/MAMP/OpenServer**

2. **Клонируйте репозиторий:**
```bash
git clone https://github.com/denisunderonov/notelist-PHP-JS-MySQL.git
```

3. **Скопируйте в папку htdocs (или www)**

4. **Создайте БД в phpMyAdmin:**
- Откройте http://localhost/phpmyadmin
- Создайте БД `notebook`
- Создайте таблицу `clients` (SQL выше)

5. **Настройте подключение в data.php:**
```php
$db_host = 'localhost';
$db_user = 'root';       // ваш пользователь
$db_password = 'root';   // ваш пароль
$db_db = 'notebook';
```

6. **Откройте в браузере:**
```
http://localhost/notelist-PHP-JS-MySQL/
```

## 🎨 Особенности

- Адаптивный дизайн
- Простая навигация через меню
- Валидация форм
- Чистый PHP без фреймворков

---
*Автор: Денис Андронов*
