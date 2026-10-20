# KALORIYA.SYS

Nutrition / calorie tracker. Single-file static app, deployed via GitHub Pages.

## Supabase: новые таблицы — только с GRANT (с 30.10.2026)

Аккаунты и синхронизация — общий Supabase-проект с «Кухней Yoko». Существующие таблицы работают как раньше. Любая таблица, созданная в `public` после 30.10.2026, без явного разрешения отдаёт сайту «permission denied». В том же SQL, где `create table`:

```sql
grant select, insert, update, delete on table public.<имя> to authenticated, service_role;
```

`anon` — только если таблица нужна без входа. Политики RLS работают как прежде.
