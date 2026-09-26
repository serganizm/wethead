# wethead

Публичный сайт-ссылка: [wethead.ru](https://wethead.ru).

Одна статическая страница со списком проектов. Плашки ведут на внешние сайты (в основном GitHub Pages). Репозиторий [chords](https://github.com/serganizm/chords) здесь не лежит — только ссылка на него.

## Локально

Открыть `dist/index.html` или поднять любой статический сервер из `dist/`:

```bash
python3 -m http.server 8080 --directory dist
```

Новый проект — одна запись в `dist/projects.js`.

## Деплой

GitHub Actions (`Deploy GitHub Pages`) публикует папку `dist/` на Pages.

Custom domain: `wethead.ru` (файл `dist/CNAME`).

### DNS в Рег.ру (корень `@`)

1. Удалить парковочный `A @ → 95.163.244.138`
2. Четыре A на `@`:
   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`
3. По желанию: `CNAME www → serganizm.github.io.`

Запись `c` не трогать — она для аккордов.

В Settings → Pages: Source = GitHub Actions, Custom domain = `wethead.ru`.
