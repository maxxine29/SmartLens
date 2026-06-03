SmartLens — AI-Powered SME Financial Intelligence Dashboard

Transforming raw financial data into actionable intelligence for small businesses in Zimbabwe

Project Overview
SmartLens is a 4-week portfolio project that delivers an AI-powered Power BI dashboard for Zimbabwean SMEs. It analyses financial data, forecasts cash flow, detects spending anomalies, and generates plain-English insights using the Claude AI API — the kind of financial intelligence that previously required a dedicated analyst.
This project was built to demonstrate dual competency in data analytics and project management, following a full Agile/PM process from charter to retrospective.

🔍 Problem Statement
The majority of SMEs in Zimbabwe manage their finances using basic spreadsheets with no forecasting capability. This leaves business owners unable to anticipate cash flow shortfalls, identify spending anomalies, or make proactive financial decisions.
SmartLens bridges this gap by delivering actionable intelligence from raw transaction data — surfaced through an intuitive, four-page Power BI dashboard.

✨ Key Features

Financial Overview — Revenue vs expenses, gross profit, and profit margin trends across 12 months
Cash Flow Forecast — 3-month forward projection using Power BI's built-in forecasting engine
Expense Breakdown — Category-level drill-down with budget comparison and anomaly flagging
AI Insights — Claude AI generates 4 plain-English financial insights dynamically from live dashboard data


🛠️ Tech Stack
ToolPurposeMicrosoft ExcelData simulation and preparationPower BI DesktopData modelling, DAX measures, dashboard buildPower BI ServicePublishing and sharingPython (matplotlib, pandas)Python visual for AI insight renderingClaude API (Anthropic)AI-generated financial insight summariesDAXCalculated measures (revenue, profit, cash flow, MoM %)NotionProject documentation and portfolio case study

📁 Repository Structure
SmartLens/
│
├── data/
│   └── SmartLens_Financial_Dataset.xlsx   # Simulated SME dataset (583 transactions)
│
├── dax/
│   └── measures.md                        # All DAX measures used in the dashboard
│
├── python/
│   └── ai_insights.py                     # Python script for Claude AI visual
│
├── pm-artifacts/
│   ├── SmartLens_Project_Charter.docx     # Project charter
│   ├── scope_document.md                  # Scope document
│   ├── risk_register.md                   # Risk register
│   └── retrospective.md                   # Post-project retrospective
│
└── README.md

📐 Project Management Approach
This project was managed using a structured PM framework across 4 weeks:
WeekPhaseKey DeliverablesWeek 1PlanningProject charter, scope document, Gantt chart, risk register, stakeholder personasWeek 2Data PreparationSimulated SME dataset (583 transactions), data cleaning in ExcelWeek 3Dashboard BuildPower BI data model, DAX measures, 4 dashboard pagesWeek 4AI Layer & LaunchClaude AI integration, publishing, portfolio documentation
PM Artifacts

Project Charter
Scope Document
Risk Register
Retrospective


📊 Dashboard Pages
1. Financial Overview
KPI cards, revenue vs expenses trend, profit margin line chart, and expense breakdown by category. Includes a month slicer for cross-filtering.
2. Cash Flow Forecast
Closing cash balance trend with 3-month Power BI forecast, net cash flow by month, and key cash flow KPIs.
3. Expense Breakdown
Category-level bar chart, expense distribution donut chart, monthly expense trend, and a budget vs actual table with anomaly flagging.
4. AI Insights
Python visual calling the Claude AI API dynamically — generates 4 plain-English financial insights from live dashboard data including risk flags, recommendations, and growth opportunities.

🧮 DAX Measures
Key measures built for this dashboard:
daxTotal Revenue = 
CALCULATE(SUM(Transactions[Amount (USD)]), Transactions[Type] = "Revenue")

Gross Profit = [Total Revenue] - [Total Expenses]

Profit Margin % = DIVIDE([Gross Profit], [Total Revenue], 0)

Closing Cash Balance = 
VAR OpeningBalance = 12500
VAR CumulativeCashFlow = CALCULATE([Net Cash Flow], DATESYTD(DateTable[Date]))
RETURN OpeningBalance + CumulativeCashFlow

Expense Anomaly Flag = 
IF([Total Expenses] > [Avg Monthly Expenses] * 1.2, "⚠ High", "Normal")
See dax/measures.md for the full list.

🤖 AI Insights — How It Works
The AI Insights page uses a Python visual in Power BI that:

Receives financial KPIs from the Power BI data model
Sends them to the Claude AI API with a structured prompt
Receives 4 plain-English financial insights in response
Renders them as formatted insight cards using matplotlib

This means the insights update dynamically as the dashboard data changes — no manual refresh needed.

📂 Dataset
The dataset simulates 12 months of financial data for Tatenda Hardware (Pvt) Ltd, a fictional retail hardware SME in Harare, Zimbabwe.

583 transactions across revenue and 12 expense categories
Realistic seasonal patterns (Dec/Nov revenue peak)
Deliberate anomalies (35% winter electricity spike in Jun/Jul)
Opening cash balance: $12,500

All data is simulated and based on publicly available SME financial benchmarks.

🎯 Key Findings

Annual revenue of $253,100 with expenses of $265,542 — a -4.9% profit margin
Closing cash balance of $57.60 — critically low for business continuity
Cost of Goods Sold is the largest expense category at ~$175K annually
Revenue peaks in November and December — driven by Zimbabwe's year-end construction season
Electricity costs spike 35% in June–July due to ZESA winter tariffs


👩🏽‍💻 About the Author
Maxine Mutasa — Junior Software Engineer transitioning into Data Analytics and Project Management.
Currently enrolled in the Microsoft Power BI Data Analyst Professional Certificate (Coursera) and building portfolio projects that demonstrate end-to-end PM and BI competency.

📍 Harare, Zimbabwe
💼 BSc Honours in Software Engineering — Africa University
🔗 LinkedIn - https://www.linkedin.com/in/maxine-rumbidzayi-mutasa-6a5ba7206 


📄 Licence
This project is for portfolio and educational purposes. The dataset is entirely simulated.
