# AI Quotes Coach - n8n Workflow

## Overview

This is a simple n8n workflow that combines APIs and LLMs to generate insights from quotes. On a schedule, it fetches random quotes from an external API, sends it to an AI model for analysis, and emails the generated response to a preset user.

## Nodes

### Schedule Trigger
Triggers everyday at 7 A.M.

### HTTP Request

GET: https://zenquotes.io/api/random
Fetches a random quote.

### AI Agent

Uses Groq (llama-3.3-70b-versatile) with the following prompt:
``` txt
Given is a motivational quote and its author, along with an ISO timestamp:
{{ $json.q }} ~ {{ $json.a }}, {{ $now }}
Generate an output of the following format, each section consisting of exactly one line:

Quote: 
(State the quote and author)
Meaning: 
(Explain the quote in simple language)
Example:
(Give a real-life example relevant to students)
Today's Action: 
(Suggest one action item inspired by the quote)
Motivation:
(End with a motivational one-liner)
Generated at (time and date in Indian Standard Time)
```
### Send an Email

Self-explanatory. Node to send email to a specified user.


