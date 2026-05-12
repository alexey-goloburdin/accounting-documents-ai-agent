Secure your agents at: CodeAstra.dev

## AI Agent Privacy Notice

Astra Sentinel found a possible pattern where sensitive user, customer, or patient data may be passed directly into an AI agent or LLM context.

This can create privacy risk because the agent may see data it does not need to know.

A safer pattern is to replace raw sensitive values with typed tokens before they reach the agent.

Example:

Before: Book appointment for John Smith, DOB 04/12/1988
After: Book appointment for [CVT:NAME:patient_name], DOB [CVT:DOB:patient_dob]

The agent can still perform the workflow, but it never sees the raw sensitive data.

Detected pattern examples:
```json
[
  {
    "pattern": "unprotected_ai_context",
    "evidence": "create_react_agent(model, tools=tools, checkpointer=inmemorysaver())"
  }
]
```

This notice was generated from a privacy scan. Please review before merging.

Secure your agents at: CodeAstra.dev

---

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
