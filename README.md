# Интерфейс для спектрометра

## Ключевые понятия
Проект построен в виде монорепозитория в который входят пакеты `backend`, `frontend` и `types` (общие типы для проекта)
В качестве методологии организации файловой структуры используется [feature-sliced](https://feature-sliced.design/). Основой данной методологии служат три базовых концепции: `слои`, `слайсы` и `сегменты`.
![feature-sliced-scheme](https://feature-sliced.design/assets/images/visual_schema-ca092cc631de8c129dfb48174d0a927a.jpg)

Верхний уровень представляют слои. Любой верхний слой может зависеть от нижележащего, но не наоборот. Например слой `app` может импортировать все остальные слои, т.к. находится на верхнем уровне иерархии. В то же время слой `shared` не может импортировать ничего за рамками слайса.
Более подробно c методологией можно ознакомиться по [ссылке](https://feature-sliced.design/).

## Технологический стэк
- Бэкенд:
    - `fastify` (http-server)
    - `socket.io` (websockets)
    - `typescript`
- Фронтенд:
    - *****
- Пакетный менеджер: `pnpm`

## Старт проекта
В `packages/backend` и `packages/frontend` переименовать `.env.example` в `.env`

```sh
# В консоли запустить установку зависимостей и старт проекта
pnpm i
pnpm dev
```
После установки и запуска можно тестировать работу фронтенда.
