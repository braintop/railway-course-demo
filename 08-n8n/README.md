# 08-n8n

n8n על Railway, מה-Image הרשמי `n8nio/n8n`. אין כאן קוד שלנו: רק הגדרות.

## מקומית

```bash
docker compose up -d
# open http://localhost:5678
```

## ב-Railway

1. Add → Docker Image → `n8nio/n8n`
2. Volume על `/home/node/.n8n`
3. Variables מתוך `railway.env.example` (Raw Editor)
4. Networking → Generate Domain על פורט 5678

## Workflow לדוגמה

`add-task-workflow.json`: Webhook שמקבל `title` ומוסיף משימה ל-mongo-api של מפגש 6.
ב-n8n: Import from File, ואז מחליפים את הכתובת ב-HTTP Request לכתובת ה-API שלכם.
