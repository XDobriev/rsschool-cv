# Хамзат Добриев

**Frontend Developer** — готов к релокации

## Контактная информация

- **Email:** XDobriev@yandex.ru
- **Телефон:** +7 (963) 134-26-93
- **Telegram:** [@XDobriev](https://t.me/XDobriev)
- **GitHub:** [github.com/XDobriev](https://github.com/XDobriev)
- **Discord:** xdobriev
- **Сайт:** [avtorstudio.com](https://avtorstudio.com)
- **Локация:** Назрань — удалённо

![Хамзат Добриев](./photo.jpg)

## О себе

Frontend-разработчик с опытом создания SaaS-продукта с реальной монетизацией. Разрабатываю интерфейсы на React и TypeScript, уделяя внимание качеству кода, пользовательскому опыту и продуктовым метрикам. Интересно развиваться в команде, где можно участвовать в развитии продукта, обсуждать решения и учиться у сильных разработчиков. Активно применяю AI-инструменты в ежедневной разработке.

## Навыки

**Frontend:** React, TypeScript, JavaScript ES6+, HTML5 / CSS3, TanStack Query, React Hook Form, TipTap

**Backend & данные:** Supabase, PostgreSQL, SQLite, REST API, FastAPI

**Инструменты:** Git / GitHub Actions, CI/CD, Vercel, Figma, Vitest, Playwright

**AI в разработке:** Claude Code, Cursor

## Пример кода

Фрагмент из [gym95](https://github.com/XDobriev/gym95) — команда `/export` формирует markdown-выгрузку дневника тренировок:

```ts
interface WorkoutEntry {
  date: string;
  exercise: string;
  muscleGroup: string;
  sets: { weight: number; reps: number }[];
}

function buildMarkdownExport(entries: WorkoutEntry[]): string {
  const byDate = entries.reduce<Record<string, WorkoutEntry[]>>((acc, entry) => {
    (acc[entry.date] ??= []).push(entry);
    return acc;
  }, {});

  return Object.entries(byDate)
    .map(([date, dayEntries]) => {
      const rows = dayEntries
        .map(({ exercise, muscleGroup, sets }) => {
          const setsStr = sets.map((s) => `${s.weight}кг×${s.reps}`).join(', ');
          return `- **${exercise}** (${muscleGroup}): ${setsStr}`;
        })
        .join('\n');

      return `## ${date}\n${rows}`;
    })
    .join('\n\n');
}
```

## Опыт работы

### ООО «Курорты Ингушетии» — курорт Армхи
**Специалист по автоматизации бизнес-процессов**
*Октябрь 2021 — март 2026*

- Интеграция TravelLine ↔ G1-Software (скан паспортов на ресепшене): ожидание гостя сократилось на **10 минут**
- Интеграция iiko ↔ DocInBox (Честный Знак): экономия **40 000 ₽/мес**, устранена должность сотрудника склада
- Внедрение Hotbot на сайт курорта: нагрузка колл-центра **−90%** по теме доп. услуг
- Telegram-бот (TypeScript + Grammy.js + SQLite) для онбординга: инструкции, тесты, трекинг — полный цикл от прототипа до прода (NDA)
- Настройка CRM/ERP: Битрикс24, Kaiten, UIS, YouGile, TravelLine, iiko, Medesk

### ООО «Смарт Таргет Центр» — ITHub · KiberOne
**Преподаватель IT-дисциплин**
*Октябрь 2023 — н.в.*

- Курсы: HTML & CSS, алгоритмы и структуры данных, архитектура ИС, основы технической документации
- Разработка учебных материалов, менторинг студентов по современному стеку

## Проекты

### AvtorStudio — в продакшене
React 18 · TypeScript strict · Vite · TipTap · Supabase · GitHub Actions (CI/CD → VPS) · Vercel

SaaS-платформа для писателей с реальной монетизацией: редактор рукописей (TipTap, 4 режима, история версий с diff, автосохранение), авторизация email + Telegram OAuth + VK ID, RLS-политики, подписки/оплата через Робокассу, адаптивный интерфейс, автоматический деплой через GitHub Actions, админ-панель с продуктовыми метриками (DAU/WAU/MAU, retention), экспорт в DOCX/FB2/EPUB/PDF.

[avtorstudio.com](https://avtorstudio.com) · [github.com/XDobriev/writers_studio](https://github.com/XDobriev/writers_studio)

### FinRest — в разработке
Next.js · React 19 · TypeScript · Python / FastAPI · SQLite · Tailwind CSS · shadcn/ui · Recharts

Управленческий учёт для ресторанного бизнеса: загрузка банковских выписок и накладных из Excel, дедупликация, нечёткий поиск (Fuse.js), проводки по статьям ДДС, автоматические отчёты (ДДС, ОПиУ, баланс), дашборд ключевых метрик и графики на Recharts.

[github.com/XDobriev/finrest](https://github.com/XDobriev/finrest)

### gym95 — Node.js
Node.js · TypeScript · Telegraf · Supabase

Telegram-бот — дневник тренировок: упражнения по группам мышц, кардио и бассейн с прогрессией по весам и повторениям; команда `/export` генерирует структурированный markdown. Полный цикл на Node.js.

[github.com/XDobriev/gym95](https://github.com/XDobriev/gym95)

### CV-Editor — vanilla JS
JavaScript ES6+ · HTML5 / CSS3 · DOM · localStorage · GitHub Pages

Конструктор резюме на «голом» JS: живое превью, автосохранение в localStorage, экспорт/импорт JSON, печать в PDF. Чистая статика без сборки.

[xdobriev.github.io/cv-editor](https://xdobriev.github.io/cv-editor) · [github.com/XDobriev/cv-editor](https://github.com/XDobriev/cv-editor)

## Образование

**МФПУ «Синергия»**
Информационные системы и программирование
2021 — 2025

**Purple School**
Frontend Developer — JS, TypeScript, React, Redux Toolkit, Next.js, Git Flow
2025 — 2026

## Английский язык

Уровень: **B1**
