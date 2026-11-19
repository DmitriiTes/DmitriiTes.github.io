# Портфолио проектов Теслева Дмитрия

Статическая копия портфолио, перенесённого из Weeek. Опубликовано на GitHub Pages:
**https://dmitriites.github.io/**

Сайт — обычные HTML и CSS, без сборки, фреймворков, JavaScript и внешних CDN. Все ресурсы (стили, обложка, иконки) лежат в этом репозитории.

## Структура

```
index.html            — весь текст портфолио
assets/style.css      — оформление (повторяет документ Weeek)
assets/cover.jpg      — обложка 1440px (десктоп / retina)
assets/cover-720.jpg  — обложка 720px (телефоны)
assets/apple-touch-icon.png, favicon.svg — иконки
.nojekyll             — отключает обработку Jekyll на GitHub Pages
```

## Как редактировать

1. Откройте папку в VS Code: `code ~/Projects/DmitriiTes.github.io`
2. Правьте `index.html`. Каждый проект — блок такого вида:

   ```html
   <hr>
   <h3 id="nazvanie-proekta">🔹 Название проекта</h3>
   <p><b>Описание:</b> Текст.<br><b>Роль: </b>Роль.<br><b>Ссылка:</b> <a href="https://..." target="_blank" rel="noopener noreferrer">Сайт</a></p>
   ```

   - `<br>` — перенос строки внутри абзаца, `<b>` — жирный, `<hr>` — разделитель.
   - Список ссылок: `<ul><li><p><a href="...">Текст</a></p></li></ul>`.
   - `id` у заголовка задаёт прямую ссылку на раздел: `https://dmitriites.github.io/#nazvanie-proekta`. Пишите латиницей, без пробелов, уникально.
3. Посмотреть локально: `python3 -m http.server 8000` в папке проекта и открыть http://localhost:8000

С Claude Code достаточно открыть эту папку и описать изменение словами, например: «добавь проект X после ИНГОССТРАХ с таким описанием…».

## Как опубликовать изменения

```bash
cd ~/Projects/DmitriiTes.github.io
git add -A
git commit -m "Обновление портфолио"
git push
```

GitHub Pages обновляет сайт автоматически через 1–2 минуты после `push` (статус: вкладка **Actions** в репозитории).

## Прямые ссылки на разделы

Каждый проект доступен по якорю, например `#finuslugi-ot-moskovskoy-birzhi`, `#globus`, `#vk-karty`, `#ingosstrah`. Полный список — атрибуты `id` в `index.html`.
