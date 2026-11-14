# GEMINI.md — Victory 121 (`victory121.kz`)

> **ОБЯЗАТЕЛЬНОЕ ПРАВИЛО ПЕРЕД НАЧАЛОМ ЛЮБОЙ РАБОТЫ:**
> **Сначала изучи граф знаний проекта в папке `graphify-out/`, и только после этого приступай к чтению или редактированию файлов.**

## 1. Порядок работы с графом (`graphify-out/`)
Перед тем как вносить изменения или искать код вручную:
1. Прочитай точку входа для агента: `graphify-out/wiki/index.md` или архитектурный отчет `graphify-out/GRAPH_REPORT.md`.
2. Если установлен CLI `graphify` (`pip install graphifyy`), используй запросы к графу:
   - `graphify query "<вопрос или компонент>"` — быстрый поиск связанного подграфа
   - `graphify explain "<имя узла>"` — все связи конкретного узла и точные строки кода
   - `graphify path "<Узел А>" "<Узел Б>"` — кратчайший путь между компонентами
   - `graphify god-nodes` — ключевые узлы архитектуры
3. После внесения изменений в код обнови граф командой `graphify update .` (и при необходимости `graphify export html` / `graphify export wiki`).

## 2. Неизменяемые дизайн- и бренд-правила проекта
- **Цветовая схема (Вариант 3 — Titanium Atelier & Sapphire Glow):** фон `#080D1A`, карточки `#10192E`, акцент `#2563EB` (Sapphire), свечение `#38BDF8` (Ice Cyan).
- **Логотип Victory 121 (Вариант 1):** `Manrope ExtraBold` (`Victory` чисто-белый `#FFFFFF`, `121` — контрастный Ice Cyan `#38BDF8` с мягким свечением) + 3D-глобус `./assets/victory-globe.png`.
- **Логотипы вендоров (`./assets/brands/`):** Canon, Epson, SONY, Nikon, Samsung, Kyocera, Катюша, Bang & Olufsen — строго в оригинальных цветах брендбуков на белых плашках `.vendor-plaque` (`76px`).
- **Безопасность:** без `innerHTML` (только `replaceChildren()` и `textContent`), санитизация `sanitizeUserText()`, строгий `Content-Security-Policy` в `index.html` и `.htaccess`.

## 3. Хостинг PS.kz / Plesk и автодеплой (`victory121.kz`)
- **Сервер Plesk:** `srv-plesk14.ps.kz` (`https://srv-plesk14.ps.kz:8443`, вход через `https://console.ps.kz/plesk/shared/17766`).
- **Структура папок на сервере:**
  - `/victory121-site` — наш новый сайт, привязанный через модуль **Plesk Git** к репозиторию `https://github.com/EvgeniyZV/victory121-site.git` (ветка `main`). Обновляется автоматически при каждом `git push` через Webhook.
  - `/new.victory121.kz` — текущая активная папка (`Document Root`) старого сайта на WordPress (сохранена без изменений).
  - `/httpdocs` — архив старого сайта 2012–2024 гг. (сохранён без изменений).
- **Переключение основного домена по команде пользователя:**
  - В панели Plesk (`victory121.kz` → **Настройки хостинга**) изменить поле **Корневая папка (`Document Root`)** с `new.victory121.kz` на `victory121-site` и нажать **ОК**.

