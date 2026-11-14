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
