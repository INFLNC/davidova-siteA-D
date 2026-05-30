# Davidova.Studio — Showcase section

## 1. Структура файлов

```
davidova-site/
├── work.html                         ← страница-индекс (Pearlfisher-grid + Basement-style)
├── work/
│   ├── gryzzzli.html
│   ├── love-cherry.html
│   ├── cherry-roses.html
│   ├── hazelnut-passion.html
│   ├── cherry-passion.html
│   ├── frutti-di-mare.html
│   ├── delissimo.html
│   ├── wow.html
│   ├── dot-jelly.html
│   └── pzpn.html
└── assets/
    ├── project.css                   ← общий стиль страниц проектов
    ├── img_GRYZZZLI/
    ├── img_LOVECHERRY/
    ├── img_CHERRYROSES/
    ├── img_HAZELNUTPASSION/
    ├── img_CHERRYPASSION/
    ├── img_FRUTTIDIMARE/
    ├── img_DELISSIMO/
    ├── img_WOW/
    ├── img_DOTJELLY/
    └── img_PZPN/
```

## 2. Дизайн-система

Гибрид Pearlfisher × Basement.studio:

| Слой              | Что используется                              |
| ----------------- | --------------------------------------------- |
| **Фон**           | `#0a0a0a` (почти чёрный)                      |
| **Текст**         | `#e8e6e1` (тёплый светлый)                    |
| **Приглушённый** | `#6e6c66` (для лейблов, метаданных)            |
| **Линии**         | `#1f1d1a`                                     |
| **Тег-плашка**    | фон `#1a1816`, текст `#c9c6bf`                |
| **Акцент**        | `#ff2e16` (basement-red — активные ссылки + точка после логотипа + кавычки) |

**Шрифты (Google Fonts):**

| Использование              | Шрифт                  |
| -------------------------- | ---------------------- |
| Display (большие заголовки)| **Anton** (близко к Basement Grotesque condensed) |
| Body / интерфейс           | **Inter Tight** (близко к их Geist/Helvetica)     |
| Технические подписи / счётчики | **JetBrains Mono** (mono-плашки)             |

**Подключение в `<head>` любой страницы:**
```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter+Tight:wght@400;500;600;700&family=Anton&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
```

**Подчёркивание ссылок на ховере** — реализовано через `::after` с
`transform: scaleX(0)` → `scaleX(1)`, идёт слева направо, длится 400ms.

## 3. Папки для рендеров

Каждому проекту — своя папка в `assets/`. **В каждой папке нужно два главных файла:**

- `hero.png` — статичный рендер для карточки и hero-блока
- `hover.mp4` — короткое **луп-видео 3-6 сек** (h.264, без звука), которое включается при наведении на карточку.
  - Если файла нет — карточка просто остаётся статичной, ошибки нет.
  - Альтернативно можно использовать `hover.webm` (тогда поменять `data-src` в `work.html`).

### `assets/img_GRYZZZLI/`
| Файл        | Что положить                                  |
|-------------|-----------------------------------------------|
| `hero.png`  | Статичный hero — кухня с упаковкой            |
| `hover.mp4` | 3-6 сек камера-облёт упаковки или Z-vibration |
| `01.png`    | hero для страницы проекта                     |
| `02.png`    | Брендовый паттерн — диагональный повтор       |
| `03.png`    | Unit-bar (отдельная батончик/упаковка)        |

### `assets/img_LOVECHERRY/`
| Файл        | Что положить                                  |
|-------------|-----------------------------------------------|
| `hero.png`  | Hero — коробка с пралине на шёлке             |
| `hover.mp4` | Splash шоколада или вращение коробки          |
| `01.png`    | hero страницы                                  |
| `02.png`    | Макро лицевой стороны со splash               |
| `03.png`    | Деталь пралине-сердечек                       |
| `04.png`    | Боковой профиль / фольга                      |

### `assets/img_CHERRYROSES/`
| Файл        | Что положить                                  |
|-------------|-----------------------------------------------|
| `hero.png`  | Макро foil-script                             |
| `hover.mp4` | Скольжение света по золотой фольге            |
| `01.png`    | hero страницы                                  |
| `02.png`    | Lineup из шести коробок                       |
| `03.png`    | Three-quarter hero                            |

### `assets/img_HAZELNUTPASSION/`
| Файл        | Что положить                                  |
|-------------|-----------------------------------------------|
| `hero.png`  | Открытый трей с пралине + плашка              |
| `hover.mp4` | Открытие крышки или splash орехов             |
| `01.png`    | hero страницы                                  |
| `02.png`    | Вертикальная упаковка — three-quarter         |
| `03.png`    | Квадратная упаковка — top view                |

### `assets/img_CHERRYPASSION/`
| Файл        | Что положить                                  |
|-------------|-----------------------------------------------|
| `hero.png`  | Открытый трей с пралине + плашка              |
| `hover.mp4` | Splash вишни и шоколада                       |
| `01.png`    | hero страницы                                  |
| `02.png`    | Вертикальная упаковка                         |
| `03.png`    | Квадратная упаковка                           |

### `assets/img_FRUTTIDIMARE/`
| Файл        | Что положить                                  |
|-------------|-----------------------------------------------|
| `hero.png`  | Lineup всех четырёх SKU                       |
| `hover.mp4` | Поворот lineup или последовательное появление |
| `01.png`    | hero страницы                                  |
| `02.png`    | 90 g — slim                                   |
| `03.png`    | 185 g — стандарт                              |
| `04.png`    | 225 g — квадрат                               |
| `05.png`    | 370 g — gift ribbon                           |

### `assets/img_DELISSIMO/`
| Файл        | Что положить                                  |
|-------------|-----------------------------------------------|
| `hero.png`  | Lineup трёх SKU                               |
| `hover.mp4` | Поворот или световой блик                     |
| `01.png`    | hero страницы                                  |
| `02.png`    | Hazelnut & Almond 195 g                       |
| `03.png`    | Hazelnut & Almond Gift 182 g                  |
| `04.png`    | Almond 153 g                                  |

### `assets/img_WOW/`
| Файл        | Что положить                                  |
|-------------|-----------------------------------------------|
| `hero.png`  | Lifestyle hero — мальчик с рюкзаком           |
| `hover.mp4` | Покачивание рюкзака / парящие маршмеллоу     |
| `01.png`    | hero страницы                                  |
| `02.png`    | Просто doypack без сцены                      |
| `03.png`    | Деталь callout-ов с вкусами                   |

### `assets/img_DOTJELLY/`
| Файл        | Что положить                                  |
|-------------|-----------------------------------------------|
| `hero.png`  | Hero — упаковка в центре fruit splash         |
| `hover.mp4` | Splash фруктов и сока                         |
| `01.png`    | hero страницы                                  |
| `02.png`    | Макро цитрусовой половинки                    |
| `03.png`    | Деталь с вишнями сзади                        |

### `assets/img_PZPN/`
| Файл        | Что положить                                  |
|-------------|-----------------------------------------------|
| `hero.png`  | Двойной локап positive + reverse              |
| `hover.mp4` | Эмблема, переключающаяся между состояниями    |
| `01.png`    | hero страницы                                  |

## 4. Рекомендации по форматам

| Тип         | Формат              | Размер                     | Вес    |
| ----------- | ------------------- | -------------------------- | ------ |
| **hero.png**| PNG или JPG (sRGB)  | 2560×1600 px (16:10)       | < 600 КБ |
| **01-05.png**| JPG (sRGB)         | 2400×1500 px минимум       | < 500 КБ |
| **hover.mp4**| h.264, без звука   | 1280×800, 3-6 сек loop, 24fps | < 1.5 МБ |

Для конвертации .mov → .mp4 веб-оптимизированный:
```
ffmpeg -i input.mov -vcodec h264 -acodec aac -strict -2 \
  -vf "scale=1280:-2" -crf 28 -movflags +faststart \
  -an output.mp4
```

## 5. Промпт для замены шрифтов на остальных HTML

Скопируй и отправь следующий промпт в новом чате с уже загруженными другими HTML
твоего сайта (index.html, about.html и т.д.):

---

**Промпт:**

> У меня сайт-портфолио CGI-художника davidova.studio. Я перевела раздел Showcase
> на новый визуальный язык — гибрид Pearlfisher × Basement.studio. Нужно
> применить ту же дизайн-систему ко всем остальным HTML-страницам сайта (которые
> я приложу). Старые шрифты Fraunces и Inter — заменить на новые.
>
> **Дизайн-токены, которые нужно соблюсти везде:**
>
> Цвета (CSS-переменные):
> ```css
> --bg: #0a0a0a;
> --fg: #e8e6e1;
> --muted: #6e6c66;
> --line: #1f1d1a;
> --tag-bg: #1a1816;
> --tag-fg: #c9c6bf;
> --accent: #ff2e16;
> ```
>
> Шрифты (Google Fonts, подключать так):
> ```html
> <link rel="preconnect" href="https://fonts.googleapis.com">
> <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
> <link href="https://fonts.googleapis.com/css2?family=Inter+Tight:wght@400;500;600;700&family=Anton&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
> ```
>
> Применение шрифтов:
> - **Anton** — все большие заголовки (`h1`, `h2`, hero-текст, имена проектов, цитаты, mail-ссылка в футере). Никакого italic, никакого weight — у Anton только regular.
> - **Inter Tight** — основной текст body, параграфы, кнопки, навигация. Weight 400 для текста, 500 для интерактивных элементов и подписей.
> - **JetBrains Mono** — все технические/мета подписи: счётчики `(10)`, лейблы секций (`— Selected Work`), таблица tech-specs (левая колонка), даты, индексы, мелкий копирайт в футере. Weight 400 normally, 500 для контраста.
>
> Правила интерактива:
> - **Подчёркивание ссылок на hover**: через `::after` с `transform: scaleX(0)→scaleX(1)`, происхождение справа на hover, слева на отпуск. Длительность 400ms ease-out.
> - **Активная ссылка в навигации** (например `Showcase` на странице showcase): красный цвет `--accent` и подчёркивание уже видно.
> - Логотип `AD` — Anton 22px, после букв точка красного цвета `--accent` (через `::after`).
> - Hover-меню: маленький моноширинный счётчик `(N)` рядом с пунктом (`Showcase(10)`, `Blog(28)` — basement-style).
>
> Шапка (везде одинаковая):
> ```html
> <header>
>   <a href="index.html" class="logo">AD</a>
>   <nav>
>     <a href="work.html">Showcase<span class="count">(10)</span></a>
>     <a href="about.html">Studio</a>
>     <a href="#contact">Contact</a>
>   </nav>
> </header>
> ```
> Класс `current` к активной ссылке + красный цвет.
>
> **Что НЕ менять:**
> - Структуру разделов (порядок блоков должен остаться)
> - Контент и формулировки
> - Имена файлов и пути
>
> **Что менять:**
> - Все вхождения `font-family: 'Fraunces'` → `font-family: 'Anton'` (без italic)
> - Все вхождения `font-family: 'Inter'` → `font-family: 'Inter Tight'`
> - Все вхождения `<em>...</em>` внутри заголовков — убрать тег, оставить только текст (Anton не имеет italic, так что выделение перестаёт работать)
> - Светлая палитра (#f3f1ee и т.п.) → тёмная палитра выше
> - Все ссылки получают анимированное подчёркивание через `::after`
>
> Верни обновлённые HTML по одному файлу.

---

## 6. Hover-анимация — как это работает

В `work.html` каждая карточка содержит:
```html
<img class="static-img" src="assets/img_*/hero.png" ...>
<video class="anim-media" muted loop playsinline preload="none"
       data-src="assets/img_*/hover.mp4"></video>
```

Скрипт лениво подгружает видео (`data-src` → `src`) только при первом hover,
чтобы не грузить весь трафик при загрузке страницы. Если файла нет — скрипт
ловит ошибку и оставляет статичную картинку, без шума в консоли.

## 7. Категории-фильтры

- **Premium Pralines (6)** — Love & Cherry, Cherry Roses, Hazelnut Passion, Cherry Passion, Frutti di Mare, Delissimo
- **Kids & Sweets (3)** — Gryzzzli, WOW, Dot Jelly
- **Identity (1)** — PZPN

Счётчик справа от фильтров пересчитывается автоматически.

## 8. Что делать дальше

1. **Создай папки** `assets/img_*` ровно с теми именами что выше
2. **Загрузи `hero.png`** в каждую — самое первое и главное
3. **Загрузи `hover.mp4`** туда же когда сделаешь анимацию (опционально)
4. **Загрузи `01.png` — `05.png`** для страниц проектов (см. таблицы выше)
5. **Открой `work.html`** — placeholder-ы заменятся на твои визуализации по мере появления файлов
6. **Для остальных страниц сайта** — отправь промпт из раздела 5 в новом чате с прикреплёнными HTML
