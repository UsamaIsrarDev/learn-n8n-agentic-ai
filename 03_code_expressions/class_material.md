Class 05 : Started with code expression

# Low-Code & No-Code Full Stack + N8N Expressions Guide

## Overview

This document explains **No-Code vs Low-Code**, **N8N workflows**, **Full Stack concepts**, and practical details about **Expressions, Data Types, JSON, and Workflow Automation**.  
It also includes **exams, certifications, and learning paths** for students.

---

## No-Code vs Low-Code

- **No-Code** → Fully drag & drop, no coding required.
- **Low-Code** → Drag & drop + ability to write custom code (JavaScript/Python).

---

## N8N (Low-Code Automation Platform)

- Build workflows with drag & drop.
- Write **JavaScript expressions** inside nodes for custom logic.
- Connect **Frontend & Database** via **Webhooks**.

---

## 🏗 Full Stack Meaning

- **Frontend** → User Interface (UI/UX).
- **Backend** → APIs & Business Logic.
- **Database** → Data storage.
- **Full Stack** → Combination of all layers.

### Stack Concept

A **stack** is multiple layers connected together:

```
UI → API → Database → Business Logic → AI Agents
```

---

## 🛠 Tools in Low-Code Full Stack

- **UX Pilot** → Generate UI/UX designs (No-Code).
- **Lovable** → Convert designs into frontend code (Low-Code).
- **N8N** → Automations, APIs, workflows (Low-Code).
- **Supabase** → Database + Authentication (PostgreSQL + Vector Search).
- **MCP (Model Context Protocol)** → Integration layer between tools.

```
https://uxpilot.ai/a/ui-design?page=4E1oruMAFhqwV13b9Lfi
```

```
https://lovable.dev/
```

```
https://usamaisrar.app.n8n.cloud/workflow/DtIpJJ4mliKV9H0U
```

---

## 🔄 Workflow Summary

1. **UX Pilot** → Create UI Design.
2. **Lovable** → Export design into frontend code.
3. **N8N** → Build workflows, APIs, automations.
4. **Supabase** → Database + Auth system.
5. **MCP** → Connect everything together.

---

## 🤖 AI + Prompt Engineering

- **Prompt Engineering** = Giving clear instructions to AI to generate **designs, UIs, workflows, and agents**.

---

## 🎯 Step-by-Step Learning Path

- **Step 00** → Prompt Engineering + Context Engineering.
- **Step 01-02** → Basics (Intro to No-Code & Low-Code).
- **Step 03** → Expressions (JS code in N8N).
- **Step 04+** → Agent creation in N8N.
- **Step 05** → MCP Servers (Client + Server).
- **Step 06** → Connect Lovable (Frontend) with N8N (Backend).
- **Step 07** → Import UX Pilot Design → Lovable.
- **Step 08** → Full End-to-End App (Frontend + N8N + Supabase + Agents).

---

## 📝 Exams & Certification

### Exam 1 – Prompt & Context Engineering

- Covers **Step 00**.
- **15 Questions**.
- Scenario-based (business use cases).
- Tests ability to design prompts & workflows.

### Exam 2 – Full Stack Low-Code / Agentic AI

- Covers **Steps 01–08**.
- ~140+ Questions.
- Students → 2 free attempts.
- Non-students → Paid (₹1000/attempt).
- **Proctored exam** (online, monitored).
- Certificates will be **publicly verifiable**.

---

## 💰 Lovable Pricing

- Free usage/testing available.
- Paid plan required for full features.
- Student joke: _“Spend money on Lovable or Pizza 🍕”_.

---

## 🖥 N8N Expressions – Core Concepts

### Expression Syntax

- Always wrapped in **`{{ }}`**.
- Example:

```js
{
  {
    $json.firstName + " " + $json.lastName;
  }
}
```

👉 Output → `"Junaid Khan"`

### Types of Data You Can Use

- **String** → `"Hello"`
- **Number** → `24`
- **Boolean** → `true/false`
- **Array** → `["HTML","CSS"]`
- **Object** → `{"name": "Usama"}`

---

## 📊 Examples of Expressions

- **Concatenation (Full Name):**

```js
{
  {
    $json.firstName + " " + $json.lastName;
  }
}
```

- **Math Operation:**

```js
{
  {
    $json.age + 2;
  }
}
```

- **Boolean Condition:**

```js
{
  {
    $json.age > 18;
  }
}
```

- **Date Handling (Luxon Library):**

```js
{
  {
    $now.toISODate();
  }
}
```

- **Access Node Data:**

```js
{
  {
    $node["Student Data"].json.firstName;
  }
}
```

---

## 🔄 Workflow Data Flow

- Each node’s **output = input** for the next node.
- Data is passed as **Array of Objects** with `json` key.

Example:

```json
[
  {
    "json": {
      "firstName": "Junaid",
      "lastName": "Shoukat",
      "age": 24
    }
  }
]
```

---

## 🔐 Extra Tricks

### Gmail Sub-Addressing (Unlimited Free Trials)

- Format: `yourname+tag@gmail.com`
- All mails go to the same inbox, but treated as unique by N8N.

---

## ⚡ Quick Summary

- **No-Code** = Drag & Drop only.
- **Low-Code** = Drag & Drop + Custom Code.
- **N8N Expressions** = Use JavaScript/Python to extend automation.
- **Supabase** = Database + Auth (Postgres + Vectors).
- **MCP** = Connects all tools.
- **Exams** = 2 types (Prompt Engineering + Full Stack Low-Code).
- **Certification** = Optional for learning, required for recognition.
