# Личный блог на Jekyll

Лаконичный статический блог, собираемый Jekyll и публикуемый на GitHub Pages.

## Быстрый старт

```bash
# 1. Установка зависимостей
bundle install

# 2. Локальный запуск
bundle exec jekyll serve

# 3. Откройте http://localhost:4000
```

## Добавление статьи

Создайте файл в `_posts/` с именем `YYYY-MM-DD-nazvanie-stati.md`:

```yaml
---
title: "Название статьи"
date: 2026-08-16
tags: [тег1, тег2]
description: "Краткое описание для превью"
---

Текст статьи в Markdown...
```

## Публикация на GitHub Pages

1. Создайте репозиторий `username.github.io`
2. Загрузите файлы в ветку `main`
3. В настройках репозитория включите GitHub Pages (Source: Deploy from a branch → main)
4. Сайт будет доступен по адресу `https://username.github.io`

## Настройка

Отредактируйте `_config.yml`:
- `title` — название блога
- `description` — описание
- `author` — ваше имя
- `url` — адрес сайта
