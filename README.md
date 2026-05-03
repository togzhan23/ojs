# OJS 3.5 — Инструкция по запуску и передаче проекта (Windows)



##  Запуск проекта после включения компьютера

### Шаги:

1. Открыть **MAMP**

2. Нажать:

   * **Start Servers**

3. Открыть браузер и перейти:

```text
http://localhost/ojs-3.5.0-3
```


---

##  Доступ к сайту

### Главная страница журнала:

```text
http://localhost/ojs-3.5.0-3
```

---

### Панель редактора:

```text
http://localhost/ojs-3.5.0-3/index.php/journalArchive/ru/dashboard/editorial
```

---

## Назначение нового администратора

### Шаг 1 — регистрация пользователя

1. Перейти:

```text
http://localhost/ojs-3.5.0-3/index.php/journalArchive/user/register
```

2. Зарегистрировать нового пользователя (новая почта)

---

### Шаг 2 — сделать его админом через базу данных

1. Открыть:

```text
http://localhost/phpMyAdmin5
```
<img width="1417" height="807" alt="image" src="https://github.com/user-attachments/assets/324626e4-4bd1-414d-bea0-7bd37e7a5fc4" />
<img width="1432" height="804" alt="image" src="https://github.com/user-attachments/assets/063511ce-f0e0-4310-92b7-42f43d0a1d0b" />




2. Выбрать базу:

```text
ojs_db
```

---

### Найти пользователя:

Открыть таблицу:

```text
users
```
<img width="1439" height="808" alt="image" src="https://github.com/user-attachments/assets/c129f274-af82-4668-ab67-9e9b94e5df92" />

Найти ID пользователя (например `id = 5`)

---

### Назначить роль администратора:

Открыть таблицу:

```text
user_user_groups
```

Добавить новую строку:

```text
user_id = 5
user_group_id = 1
```

---

📌 Где:

* `1` = Administrator

---

## Альтернатива (через SQL)

Можно выполнить SQL:

```sql
INSERT INTO user_user_groups (user_id, user_group_id)
VALUES (5, 1);
```

---

## Важно

* После изменений перезагрузить страницу
* Новый пользователь получит доступ администратора
* Старого администратора можно оставить или удалить

---

## Полезно знать

* Папка `files` содержит все статьи
* Без неё сайт не будет работать корректно
* База данных = вся информация о пользователях и журнале

---

## Готово

Теперь:

* сайт запускается после включения ПК
* новый администратор назначен
* система полностью рабочая

---
