Financial Data Analysis Chatbot
Overview

This project is a data-grounded financial analysis chatbot designed to answer questions strictly from user-uploaded data files. The chatbot does not use the internet or external knowledge. If an answer cannot be derived from the provided data, it clearly responds with:

"Sorry can not find the answer"

This makes the system reliable, auditable, and suitable for financial and analytical use cases where hallucination is unacceptable.

Key Features

Answers questions only from uploaded structured data files

No external data access or assumptions

Deterministic and calculation-based responses

Explicit fallback when data is missing

Suitable for portfolio analysis, fund comparison, and P&L evaluation

Data Scope

The chatbot works with structured tabular financial data, including but not limited to:

Investment portfolios and funds

Holdings and trades

Securities (Equity, Bond, Asset-Backed, etc.)

Quantities, prices, and FX rates

Profit and Loss metrics

Each row in the dataset represents one holding or trade record.

Supported Data Fields

The chatbot understands and uses the following fields:

Fund Identification: ShortName, PortfolioName

Security Identification: SecurityId, SecName, SecurityTypeName

Dates: AsOfDate, OpenDate, CloseDate

Quantities & Prices: StartQty, Qty, StartPrice, Price

Valuation: MV_Local, MV_Base

Profit and Loss Metrics:

PL_DTD (Day-to-Date)

PL_MTD (Month-to-Date)

PL_QTD (Quarter-to-Date)

PL_YTD (Year-to-Date)

Only these fields are used for calculations and comparisons.

Core Rules (Strictly Enforced)

The chatbot answers only using the uploaded files.

External knowledge, web data, or assumptions are not allowed.

If the answer is not present or cannot be calculated from the data, the response is exactly:

"Sorry can not find the answer"

No hallucinated values, summaries, or explanations.

All calculations (counts, totals, comparisons) are derived strictly from the dataset.

Data Interpretation Rules

Each row = one holding or trade

Number of holdings or trades = number of matching rows

Fund performance comparison is based only on PL_YTD

Yearly performance does not assume dates beyond AsOfDate

If data is missing or incomplete, no inference is made

Example Questions Supported
Holdings & Trades

Total number of holdings for a given fund

Number of trades for a specific security

Performance Analysis

Which fund performed better based on yearly Profit and Loss

Compare PL_YTD between two or more funds

Valid Response Example

Q: Which fund performed better based on yearly Profit and Loss?

A: Based on PL_YTD, Fund A performed better than Fund B because its yearly profit/loss is higher.

Invalid / Unsupported Query Example

Q: What is the NAV of the fund?

A: Sorry can not find the answer

What This Chatbot Will NOT Do

Guess or estimate missing values

Use internet or real-time market data

Answer conceptual finance questions

Provide investment advice

Intended Use Cases

Financial data validation

Portfolio performance analysis

Fund comparison dashboards

Internal analytics tools

Academic or demo projects requiring zero hallucination

Deployment Notes

Designed to work with modern LLM frameworks (e.g., AI SDK, vo.dev, Flowise)

Web access must be disabled

A strict system prompt is required to enforce grounding

Disclaimer

This chatbot is an analytical tool and does not provide financial advice. All outputs are strictly derived from the uploaded data files.

Author

Project Type: Data-grounded AI chatbot for financial analysis

If the data does not contain the answer, the chatbot will always say:

"Sorry can not find the answer"
