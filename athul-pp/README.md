# AI Quote Coach - n8n Workflow

## 📌 Project Overview

This repository contains the n8n workflow for the Day 9 Task. The workflow automates the process of fetching a daily quote, generating a student-focused explanation and action plan using AI (Google Gemini), and delivering it directly via email.

## ⚙️ Workflow Breakdown

1. **Manual Trigger:** Initiates the workflow on demand.
2. **HTTP Request:** Fetches a random quote and author from the `[https://zenquotes.io/api/random](https://zenquotes.io/api/random)` endpoint.
3. **Google Gemini Chat Model (Basic LLM Chain):** Processes the JSON output from the API. Using a structured prompt, the AI generates:
* The core meaning of the quote in simple language.
* A real-life example relevant to engineering students.
* A highly actionable 20-minute micro-action.
* A motivational one-liner.


4. **Send Email:** Delivers the fully formatted response to the target inbox, complete with a dynamic, timezone-aware timestamp (`Asia/Kolkata`).

## 🚀 Features & Challenges Met

* **Strict Output Formatting:** The AI node bypasses standard chat interfaces and uses a strict predefined prompt expression (`Define below`) to guarantee consistent Markdown structure.
* **Dynamic Timestamps:** The email subject line includes a dynamically generated date using n8n's built-in Luxon formatting.
* **Error Handling:** The HTTP Request node is configured to `Continue On Fail` to prevent workflow crashes if the external API rate-limits or goes down.

## 🛠️ How to Import and Run

1. Download the exported `.json` workflow file from this repository.
2. Open your n8n workspace.
3. Click on the three dots (`...`) in the top right corner of the canvas.
4. Select **Import from File** and upload the `.json` file.
5. Double-click the **Google Gemini** node and add your own API credentials.
6. Double-click the **Send Email** node and update the `To Email` address with your destination inbox.
7. Click **Execute Workflow** to test the automation.

---

**Author:** Athul P P | GECTCR