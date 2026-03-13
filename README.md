# ИИ-агент создания акта выполненных работ

Этот ИИ-агент создан как Proof of Concept для создания актов выполненных работ. Агент работает на Python и использует LangChain, в качестве LLM используется GigaChat. Видео про ИИ-агентов и создание своего агента: [https://youtu.be/KFgwXXWT7sQ](https://youtu.be/KFgwXXWT7sQ).

Для запуска создай `.env` файл и укажи в нём токен для подключения к API GigaChat:

```bash
cp .env-example .env
```

Установка зависимостей с пакетным менеджером `uv`:

```bash
uv venv
uv sync
```

Запуск агента:

```bash
uv run main.py "реквизиты.docx"
```
