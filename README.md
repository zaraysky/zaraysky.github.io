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

## Workflow: написание и публикация статей

### 1. Создание черновика

Создайте файл в `_posts/` с именем `YYYY-MM-DD-nazvanie-stati.md`:

```yaml
---
title: "Название статьи"
date: 2026-08-16
tags: [тег1, тег2]
description: "Краткое описание для превью на главной"
---

Текст статьи в Markdown...
```

Правила имени файла:
- Дата в начале: `YYYY-MM-DD-`
- Затем slug (URL-часть): латиница, цифры, дефисы
- Расширение: `.md`

### 2. Локальная проверка

```bash
bundle exec jekyll serve
```

Откройте `http://localhost:4000` — ваша статья появится в списке первой (сортировка по дате убыванию). Проверьте:
- заголовок и описание на главной
- отображение тегов
- форматирование Markdown (списки, код, цитаты)
- внешние ссылки

### 3. Добавление изображений

Положите изображения в папку `assets/images/`, а в статье ссылайтесь на них:

```markdown
![Описание изображения](/assets/images/screenshot.png)
```

### 4. Публикация на GitHub Pages

```bash
# Добавьте новый файл в индекс
git add _posts/2026-08-16-nazvanie-stati.md

# Закоммитьте
git commit -m "Добавлена статья: Название статьи"

# Отправьте в репозиторий
git push origin main
```

GitHub Pages автоматически пересоберёт сайт (обычно в течение 1–2 минут). Обновления появятся по адресу `https://username.github.io`.

### 5. Редактирование опубликованной статьи

Просто внесите правки в файл `.md`, закоммитьте и запушьте — сайт обновится автоматически.

---

## Структура front matter

| Поле | Обязательно | Описание |
|------|-------------|----------|
| `title` | да | Заголовок статьи |
| `date` | да | Дата публикации (YYYY-MM-DD) |
| `tags` | нет | Список тегов `[tag1, tag2]` |
| `description` | нет | Краткое описание для превью на главной |

## Публикация на GitHub Pages (первый раз)

1. Создайте репозиторий `username.github.io` на GitHub
2. Инициализируйте Git в папке проекта:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/username/username.github.io.git
   git push -u origin main
   ```
3. В настройках репозитория (Settings → Pages) включите GitHub Pages:
   - Source: Deploy from a branch
   - Branch: main / (root)
4. Сайт будет доступен по адресу `https://username.github.io`

## Настройка

Отредактируйте `_config.yml`:
- `title` — название блога
- `description` — описание
- `author` — ваше имя
- `url` — адрес сайта (`https://username.github.io`)
