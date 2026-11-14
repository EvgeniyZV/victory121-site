# Victory 121 — Авторизованный сервисный центр в Алматы

Официальный адаптивный веб-сайт авторизованного сервисного центра **ТОО «Victory 121»** ([https://victory121.kz/](https://victory121.kz/)).
17 лет опыта профессионального ремонта и обслуживания оргтехники, фотоаппаратов, объективов, мониторов и аудиосистем High-End в Алматы (ул. Розыбакиева, 275А).

---

## 1. Архитектура проекта и стек технологий

Проект реализован на чистом, быстром и безопасном стеке **HTML5 + Modern CSS3 + Vanilla JS (ES6+)** без сторонних тяжеловесных фреймворков:

- **[index.html](./index.html)** — семантическая разметка страницы, включающая:
  - Мета-заголовки безопасности (`Content-Security-Policy`, `referrer="strict-origin-when-cross-origin"`).
  - Верхнюю информационную панель (`.utility-bar`) и липкую шапку (`.site-header`) с логотипом **Victory 121** (Вариант 1: `Manrope ExtraBold` + ледяной циан `#38BDF8` для `121` + фирменный глобус `assets/victory-globe.png`), переключателем языков `РУС / ҚАЗ`, телефоном и кнопкой WhatsApp.
  - Мобильное боковое меню на нативном теге `<dialog id="mobile-drawer">`.
  - Главный экран (`.hero-section`) с фирменной SVG-анимацией электрических импульсов платы (`.hero-tech-bg`) и интерактивной 5-слайдовой каруселью техники (`#hero-carousel`).
  - Секцию 8 авторизованных брендов (`#brands`): **Canon**, **Epson**, **SONY**, **Nikon**, **Samsung**, **Kyocera**, **Катюша**, **Bang & Olufsen** на контрастных белых плашках (`.vendor-plaque`) со строгим соблюдением брендбуков вендоров.
  - Сетку из 6 направлений ремонта (`#services`): принтеры/МФУ (`printers`), камеры (`cameras`), объективы (`lenses`), мониторы/ТВ (`monitors`), аудио High-End (`audio`), корпоративное обслуживание B2B (`b2b`).
  - Интерактивный конструктор заявки в WhatsApp (`#calculator` / `#whatsapp-quiz-form`) с динамическими симптомами и кнопкой **«✎ Другое (описать свою ошибку)»** (`#custom-symptom-box`).
  - Секцию инженерных стандартов (`#about`), контактов и изолированной карты (`#contacts`) и модальное окно деталей услуг (`<dialog id="service-modal">`).
- **[styles.css](./styles.css)** — дизайн-система **Theme 3: Titanium Slate & Ice Silver**:
  - Цветовые токены: `--bg-void: #0b121e`, `--bg-surface: #111b2e`, `--bg-elevated: #16233b`, `--accent-blue: #0284c7`, `--accent-cyan: #38bdf8`, `--accent-silver: #e2e8f0`, `--accent-whatsapp: #10b981`.
  - Адаптивные брейкпоинты: Desktop (`1240px`), Tablet (`<= 1080px`), Mobile (`<= 720px`) с нижней липкой панелью быстрых действий (`.mobile-bottom-bar`).
- **[app.js](./app.js)** — клиентская логика:
  - Двуязычный словарь `I18N` (`ru` / `kz`) и база данных направлений ремонта `SERVICE_DETAILS`.
  - Управление каруселью (`setCarouselSlide`, `startCarousel`, `stopCarousel`).
  - Управление конструктором заявки (`renderSymptomChips`, `syncDeviceChipsUI`, `syncBrandUI`) и защита от XSS (`sanitizeUserText`, использование `replaceChildren()` и `textContent` без `innerHTML`).
- **[.htaccess](./.htaccess)** — серверная конфигурация безопасности для Apache (`Strict-Transport-Security`, `X-Frame-Options: SAMEORIGIN`, `X-Content-Type-Options: nosniff`, `Referrer-Policy`, `Permissions-Policy`, `Content-Security-Policy`).
- **[assets/](./assets/)** — локальные графические ресурсы:
  - `assets/victory-globe.png` — фирменный 3D-глобус логотипа Victory 121.
  - `assets/brands/` — адаптированные под рамку официальные векторные логотипы вендоров (`canon.svg`, `epson.svg`, `sony.svg`, `nikon.svg`, `samsung.svg`, `kyocera.svg`, `katusha.png`, `bang-olufsen.svg`).

---

## 2. Работа с графом проекта (Graphify)

В проект встроен граф знаний **Graphify** в папке [`graphify-out/`](./graphify-out/):
- `graphify-out/graph.html` — интерактивная визуализация графа в браузере.
- `graphify-out/GRAPH_TREE.html` — иерархическое дерево архитектуры проекта.
- `graphify-out/GRAPH_REPORT.md` — полный архитектурный отчёт с ключевыми узлами (God Nodes) и связями.
- `graphify-out/wiki/index.md` — навигационная вики по модулям проекта.
- `graphify-out/graph.json` — машиночитаемый граф для запросов агента.

### Быстрые команды на рабочем компьютере:
```bash
# Установка Graphify (если ещё не установлен на рабочем ПК)
pip install graphifyy

# Запрос к графу проекта
graphify query "Как работает конструктор заявки WhatsApp?"

# Объяснение связей конкретного узла
graphify explain "renderSymptomChips"

# Обновление графа после изменения кода
graphify update .
```

### Локальный запуск сайта для предпросмотра:
```bash
python -m http.server 8121 --bind 127.0.0.1
```
После запуска откройте в браузере `http://127.0.0.1:8121/`.
