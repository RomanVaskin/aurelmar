# Перенос актуального дизайна AURELMAR

Источник: `RomanVaskin/aurelmar-8x`, ветка `v0/aurelmar-homepage-polish`.

Полный source commit: `cae6dbdc99595ec1c072d0835b24c3626a7304ea`.

В source `main` находится исходный v0-снимок `b8b2adb`; выбранная ветка содержит более поздние контраст hero, размеры заголовков, CTA, reveal и мобильное меню. Основной `aurelmar` до переноса — `a953acd`, README и два исследования.

Перенесён снимок файлов, не Git-история. Все пути ниже добавлены без изменения исходных байтов. Конфликтов путей с существующими файлами нет. README основного репозитория дополнен, `research/` не изменён.

## Точный список перенесённых файлов (42)

- `.gitignore`
- `app/globals.css`
- `app/layout.tsx`
- `app/page.tsx`
- `components.json`
- `components/aurelmar/approach.tsx`
- `components/aurelmar/destinations.tsx`
- `components/aurelmar/hero.tsx`
- `components/aurelmar/insights.tsx`
- `components/aurelmar/partners.tsx`
- `components/aurelmar/properties.tsx`
- `components/aurelmar/reveal.tsx`
- `components/aurelmar/services.tsx`
- `components/aurelmar/site-footer.tsx`
- `components/aurelmar/site-header.tsx`
- `components/ui/button.tsx`
- `lib/utils.ts`
- `next.config.mjs`
- `package.json`
- `pnpm-lock.yaml`
- `pnpm-workspace.yaml`
- `postcss.config.mjs`
- `public/apple-icon.png`
- `public/icon-dark-32x32.png`
- `public/icon-light-32x32.png`
- `public/icon.svg`
- `public/images/article-1.png`
- `public/images/article-2.png`
- `public/images/article-3.png`
- `public/images/cyprus.png`
- `public/images/georgia.png`
- `public/images/hero.png`
- `public/images/property-1.png`
- `public/images/property-2.png`
- `public/images/property-3.png`
- `public/images/thailand.png`
- `public/placeholder-logo.png`
- `public/placeholder-logo.svg`
- `public/placeholder-user.jpg`
- `public/placeholder.jpg`
- `public/placeholder.svg`
- `tsconfig.json`

## Границы переноса

Это существующий дизайн v0 с его демонстрационными изображениями, текстами и ссылками. Перенос не подтверждает факты об объектах/ценах и не подключает реальный каталог или backend. Production, DNS, инфраструктура, секреты и публикация не менялись. Source-репозиторий не изменялся, истории не объединялись.

## Результаты проверок

- Зависимости: frozen lockfile установлен без изменения source manifest/lockfile. В среде проверки Node.js 24.19.0 и pnpm 11.19.0; source packageManager=pnpm@12.3.4 сохранён без изменения.
- `tsc --noEmit` — успешно отдельно от Next.js build (source config сохраняет ignoreBuildErrors=true). Повтор после генерации Next.js types — успешно.
- Стандартный `pnpm build` / Next.js 16.4.3 Turbopack — успешно; Google Fonts загружены, главная страница пререндерена.
- Все 42 перенесённых файла побайтно совпадают с Git blobs source commit, в том числе после установки зависимостей и build.
- Оба исследования побайтно совпадают с исходным main. Изначальный текст README сохранён. Все локальные ссылки изображений components/aurelmar разрешаются в public/.
- `git diff --check` — успешно. Нет удалённых исходных файлов, нет merge чужой истории.
- Production/runtime приёмка и deploy не выполнялись.
