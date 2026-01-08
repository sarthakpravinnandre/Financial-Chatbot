# 📊 Financial Data Analysis Chatbot

A lightweight, rule-based chatbot designed to answer **financial and investment-related queries** strictly using **user-uploaded structured data files**. This project focuses on **accuracy, transparency, and zero hallucination**, making it suitable for finance-sensitive environments.

---

## 🎯 Project Objective

The goal of this chatbot is to:

1️⃣ Analyze financial portfolio data
2️⃣ Answer user questions only from uploaded files
3️⃣ Avoid assumptions, guesses, or external knowledge
4️⃣ Provide clear numeric and factual answers

If the data is missing or insufficient, the chatbot responds safely instead of guessing.

---

## 📂 Supported Data Scope

The chatbot works **only** with uploaded tabular data files containing:

1️⃣ Investment portfolios
2️⃣ Funds and holdings
3️⃣ Securities and instruments
4️⃣ Trades, quantities, and prices
5️⃣ Profit & Loss metrics

Each **row** in the dataset represents **one holding or trade**.

---

## 🧠 Strict Intelligence Rules

The chatbot follows **non-negotiable rules**:

1️⃣ Answers are generated **only** from uploaded data
2️⃣ No internet, no external databases, no assumptions
3️⃣ No fabricated numbers or explanations
4️⃣ Calculations are derived strictly from available columns
5️⃣ If data is missing, it clearly refuses to answer

🛑 **Fallback Response (Exact):**

```
Sorry can not find the answer
```

---

## 📌 Key Data Fields Used

The chatbot identifies and computes answers using:

### 🔹 Fund Identification

* `ShortName`
* `PortfolioName`

### 🔹 Security Identification

* `SecurityId`
* `SecName`
* `SecurityTypeName`

### 🔹 Profit & Loss Metrics

* `PL_DTD`  (Day-to-Date)
* `PL_MTD`  (Month-to-Date)
* `PL_QTD`  (Quarter-to-Date)
* `PL_YTD`  (Year-to-Date)

⚠️ Yearly performance comparisons are based **only on `PL_YTD`**.

---

## 📐 How Calculations Work

1️⃣ **Holdings Count** = Number of matching rows
2️⃣ **Fund Performance** = Comparison using `PL_YTD`
3️⃣ **Totals / Sums** = Aggregated strictly from numeric columns
4️⃣ **Date Handling** = Limited to provided `AsOfDate`

No inferred timelines or missing dates are assumed.

---

## 💬 Example Questions & Responses

### ❓ Total number of holdings for Garfield fund

✅ *Answer:* The total number of holdings for the Garfield fund is **X**.

### ❓ Which fund performed better yearly

✅ *Answer:* Based on `PL_YTD`, Fund A performed better than Fund B because its yearly P&L is higher.

### ❓ What is the NAV of the fund

❌ *Answer:*

```
Sorry can not find the answer
```

---

## 🚀 Use Cases

1️⃣ Financial data validation
2️⃣ Portfolio performance comparison
3️⃣ Internal fund analysis tools
4️⃣ Audit-safe AI applications
5️⃣ Academic or final-year engineering projects

---

## ✅ Project Highlights

✔️ Zero hallucination policy
✔️ Deterministic and explainable answers
✔️ Finance-safe chatbot behavior
✔️ Ideal for sensitive investment data
✔️ Clean, rule-driven architecture

---

## 🧩 Future Enhancements

1️⃣ Role-based access control
2️⃣ Natural language query refinement
3️⃣ Interactive dashboards
4️⃣ Multi-file portfolio comparison
5️⃣ Exportable analysis reports

---

📌 **Note:** This chatbot intentionally prioritizes correctness over creativity. If the data does not support an answer, it will always refuse safely.

---

👨‍💻 *Developed as a structured financial data analysis project using strict AI guardrails.*
