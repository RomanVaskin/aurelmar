# aurelmar
## Дизайн сайта

Актуальный Next.js-дизайн перенесён из `RomanVaskin/aurelmar-8x`, ветка
`v0/aurelmar-homepage-polish`, commit `cae6dbd`. Полный commit, точный список файлов
и границы переноса: [docs/DESIGN_IMPORT.md](docs/DESIGN_IMPORT.md).

Существующие исследования сохранены:

- [Рынок и конкуренты](research/market-and-competitors.md)
- [Deep research](research/deep-research-2026-10-28.md)

### Локальная работа

```bash
pnpm install --frozen-lockfile
pnpm exec tsc --noEmit
pnpm dev
pnpm build
```

Используется packageManager из `package.json`. Сборка загружает шрифты через
`next/font/google`, поэтому нужен доступ к Google Fonts. Дизайн пока содержит
демонстрационные данные; это перенос интерфейса, без merge или deploy.

### Production deploy

Workflow и настройка GitHub Secret/Variable, проверки и порядок первого запуска:
[docs/DEPLOY.md](docs/DEPLOY.md). Merge в `main` запускает деплой; без разрешения
владельца PR не объединять.
