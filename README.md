# 💰 AI-Powered Personal Finance Advisor

An intelligent personal finance Android application built with **Kotlin + Jetpack Compose**, designed to help users automatically track expenses, categorize spending, and receive personalized financial advice — all enhanced by AI.

## 🚀 Features

* 📸 **Receipt Scanning**
  Use ML Kit to extract text from scanned receipts and automatically record expenses.

* 📩 **M-Pesa SMS Integration**
  Read and parse M-Pesa SMS messages (with user permission) to auto-log mobile money transactions.

* 🧠 **Smart Categorization**
  Auto-categorize expenses using rule-based logic and Hugging Face NLP models. Prompt user when categorization is uncertain.

* 💬 **“Ask My Finances” AI Agent**
  Chat with your finances using natural language. Ask:

  * “How much did I spend last week?”
  * “Where can I cut down on spending?”
  * “Suggest a saving strategy based on my habits”

* 📊 **Expense Analytics**
  Visual breakdowns of expenses by category, time, and amount.

* 💾 **Offline Support**
  Local storage powered by Room Database.

---

## 🧰 Tech Stack

| Layer            | Technology                                                             |
| ---------------- | ---------------------------------------------------------------------- |
| Language         | Kotlin                                                                 |
| UI               | Jetpack Compose                                                        |
| Architecture     | MVVM + Clean Architecture                                              |
| ML/OCR           | [ML Kit](https://developers.google.com/ml-kit/vision/text-recognition) |
| AI/NLP           | [Hugging Face Inference API](https://huggingface.co/inference-api)     |
| SMS Parsing      | Android SMS Content Provider                                           |
| Database         | Room Persistence Library                                               |
| Background Tasks | WorkManager                                                            |
| Network          | Retrofit / OkHttp                                                      |
| Permissions      | AndroidX Activity/Permissions APIs                                     |

---

## 📷 Screenshots


---

## ⚒️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/vivian347/Jibudget.git
cd Jibudget
```

### 2. Add Your API Keys

Create a file in your project:

```
local.properties
```

And add:

```properties
HUGGINGFACE_API_KEY=your_key_here
```

For SMS parsing, make sure to declare:

```xml
<uses-permission android:name="android.permission.READ_SMS"/>
<uses-permission android:name="android.permission.RECEIVE_SMS"/>
```

### 3. Run the App

Open in Android Studio and click ▶️

---

## 🧪 Key Modules

| Module       | Description                                                 |
| ------------ | ----------------------------------------------------------- |
| `receipts/`  | ML Kit text recognition for scanned receipts                |
| `sms/`       | M-Pesa SMS parser and extractor                             |
| `chat/`      | Hugging Face API interface for finance chat agent           |
| `expenses/`  | Expense entry management, categorization, and Room DB setup |
| `analytics/` | Charts and graphs (PieChart, BarChart using Compose)        |

---

## 🤖 AI & ML Notes

| Feature             | Tool Used                                   | Local or API |
| ------------------- | ------------------------------------------- | ------------ |
| OCR for Receipts    | ML Kit                                      | On-device    |
| Categorization      | Hugging Face (or rule-based fallback)       | API          |
| GPT-like Chat Agent | Hugging Face                                | API          |

---

## 📜 License

This project is licensed under the MIT License.

---

## 💡 Inspiration

This project was inspired by the intersection of:

* 🇰🇪 Local financial behaviors (M-Pesa usage)
* 💸 Financial literacy gaps
* 🧠 AI-powered personal productivity

---

## 🙌 Contributions

PRs and ideas are welcome!
Let’s build AI tools that make local financial lives easier 🚀
