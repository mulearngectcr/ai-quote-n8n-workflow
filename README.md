# AI Quote Coach - n8n Workflow

## Overview

An n8n workflow that combines APIs and Large Language Models (LLMs) to generate meaningful insights from inspirational quotes.

The workflow fetches a random quote from an external API, sends it to an AI model for analysis, and emails the generated response to the user.

This project is designed to help learners understand how AI can be integrated into workflow automation using n8n.

---

## Workflow

Manual Trigger
→ HTTP Request (ZenQuotes API)
→ AI Agent / LLM Node
→ Send Email

---

## Features

* Fetches a random inspirational quote
* Uses AI to explain the quote
* Generates a student-friendly example
* Suggests an actionable takeaway
* Sends the generated response via email
* Demonstrates AI-powered workflow automation

---

## API Used

ZenQuotes API

https://zenquotes.io/api/random

Sample Response:

[
{
"q": "Success is not final, failure is not fatal.",
"a": "Winston Churchill"
}
]

---

## AI Prompt

Example Prompt:

You are a personal growth coach.

Quote: {{quote}}
Author: {{author}}

Explain the quote in simple language.

Give one real-life example relevant to students.

Suggest one action the reader can take today.

End with a motivational one-liner.

---

## Expected Output

Quote:
"Success is not final, failure is not fatal."

Author:
Winston Churchill

Meaning:
Every success and failure is temporary.

Example:
A student who fails one exam can still succeed through consistent effort.

Today's Action:
Spend 30 minutes improving a weak subject.

Motivation:
Progress is built one step at a time.

---

## Submission Requirements

* Exported workflow JSON file
* Screenshot of workflow
* Screenshot of successful execution
* README file

---

## Bonus Challenges

* Dynamic email subjects
* Google Sheets integration
* Telegram notifications
* Discord notifications
* Response quality filtering using IF nodes

---

Happy Building 🚀
