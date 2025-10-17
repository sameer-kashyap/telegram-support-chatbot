# 🤖 AI-Powered Telegram Support Chatbot (n8n + Gemini)

## 🧩 Problem Statement
Authors and customers often ask repetitive questions about publishing plans, pricing, royalties, and submission guidelines. Responding manually consumes support time and delays responses.

## ✅ Solution
A Telegram-based AI chatbot that automatically:
- Recognizes common FAQs (e.g., “How do I publish my book?”)
- Gives **instant, structured replies**
- Falls back to **AI-powered answers** when unsure

---

## 🧠 Tech Stack

| Tool / Service | Purpose |
|----------------|---------|
| n8n | Workflow automation |
| Telegram Bot API | Customer interaction |
| OpenAI GPT | Dynamic AI fallback replies |
| Switch Node | FAQ classification logic |

---

## 🔗 Workflow Structure
[Telegram Trigger]
↓
[Normalize Message]
↓
[Check FAQ Match (Switch)]
├── Match → [Predefined Answer] → [Send Reply]
└── No Match → [OpenAI AI Response] → [Send Reply]


---

## 📁 Repository Files

| File | Description |
|------|-------------|
| `workflow.json` | Exported n8n workflow for import |
| `screenshots/flow.png` | Visual workflow |
| `prompt.txt` | AI instruction prompt |

---

## 🛠 How It Works (Example Conversations)

| User Input | Bot Response |
|------------|--------------|
| "What’s your publishing fee?" | "Our publishing plans start from ₹X. You can submit your manuscript at bookleafpub.in" |
| "Do you offer royalties?" | "Yes, authors receive up to X% royalties per sale." |
| "What's the weather?" | "I can help only with publishing-related questions. How can I assist you further?" *(Only if fallback rule is used)* |

---

## 🚀 Benefits

| Benefit | Impact |
|---------|--------|
| 24/7 Instant Replies | Zero waiting time for basic queries |
| Reduces Support Load | Support agents handle only complex issues |
| Scalable | Can be deployed across WhatsApp / Web later |

---

## 📌 Future Enhancements

- Add **lead capture & CRM logging**
- Add **multi-language responses**
- Enable **human handover to support team**

