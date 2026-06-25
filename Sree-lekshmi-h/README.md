# Daily Quote Generator (n8n)

A simple n8n workflow that automatically fetches a motivational quote, uses AI to explain it, and emails the result daily.

## Features

* Fetches a random quote from ZenQuotes
* Uses Groq AI to generate:

  * Meaning of the quote
  * Student-related example
  * Practical action for the day
  * Motivational one-liner
* Sends the generated content via Gmail
* Runs automatically on a schedule

## Workflow

```text
Schedule Trigger
      ↓
ZenQuotes API
      ↓
AI Agent (Groq)
      ↓
Format Output
      ↓
Gmail
```

## Technologies

* n8n
* Groq AI
* ZenQuotes API
* Gmail API


