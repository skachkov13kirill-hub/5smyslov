# 5smyslov.ru — Сайт «5 смыслов»

Авторская методика взаимопонимания в паре. 34 статьи + лендинг + блог.

## Стек

- Статика (HTML/CSS/JS), без билдеров
- GitHub Pages + Cloudflare (опционально)
- Шрифты: Lora + Inter (Google Fonts)

## Структура

```
/
├── index.html              Лендинг (Person→WebSite + FAQPage JSON-LD)
├── blog.html               Хаб блога, 4 кластера, 34 статьи
├── about-method.html       О методике (Article + BreadcrumbList + DefinedTermSet)
├── glossary.html           Глоссарий терминов (DefinedTermSet)
├── 404.html
├── articles/               34 HTML-статьи
├── styles.css
├── script.js               Мобильное меню, FAQ, fade-up
├── sitemap.xml             38 URL
├── robots.txt
├── rss.xml                 6 главных статей
├── manifest.json           PWA-readiness
├── favicon.svg, og-image.svg
├── CNAME                   5smyslov.ru
└── .nojekyll               Отключить Jekyll-обработку
```

## Локальный preview

```bash
python3 -m http.server 8767 --directory .
# или через Claude: preview_start name="psiholog-demo"
```

## Деплой

См. подробную инструкцию в [`../DEPLOY_GUIDE.md`](https://github.com/skachkov13kirill-hub/5smyslov/blob/main/DEPLOY_GUIDE.md) — но репозиторий содержит только `site/`, а DEPLOY_GUIDE остаётся в локальной папке проекта.

Краткая последовательность для reg.ru DNS:
1. На reg.ru → DNS → удалить дефолтные записи
2. Добавить 4 A-записи на `@` → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
3. Добавить CNAME `www` → `skachkov13kirill-hub.github.io.`
4. GitHub → Settings → Pages → Custom domain → `5smyslov.ru` → Enforce HTTPS
5. Через 1–24 часа DNS пропагирует и `https://5smyslov.ru` заработает

## Контакты

Проект Кирилла Скачкова, в рамках SEO-агентства DRESSCODE.
