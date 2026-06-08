# SmartLens — DAX Measures

## Revenue & Expense Measures

```dax
Total Revenue = 
CALCULATE(SUM(Transactions[Amount (USD)]), Transactions[Type] = "Revenue")

Total Expenses = 
ABS(CALCULATE(SUM(Transactions[Amount (USD)]), Transactions[Type] = "Expense"))

Gross Profit = [Total Revenue] - [Total Expenses]

Profit Margin % = DIVIDE([Gross Profit], [Total Revenue], 0)
```

## Month-on-Month Measures

```dax
Revenue MoM % = 
VAR CurrentMonth = [Total Revenue]
VAR PrevMonth = CALCULATE([Total Revenue], DATEADD(DateTable[Date], -1, MONTH))
RETURN DIVIDE(CurrentMonth - PrevMonth, PrevMonth, 0)

Expenses MoM % = 
VAR CurrentMonth = [Total Expenses]
VAR PrevMonth = CALCULATE([Total Expenses], DATEADD(DateTable[Date], -1, MONTH))
RETURN DIVIDE(CurrentMonth - PrevMonth, PrevMonth, 0)
```

## Cash Flow Measures

```dax
Net Cash Flow = [Total Revenue] - [Total Expenses]

Closing Cash Balance = 
VAR OpeningBalance = 12500
VAR CumulativeCashFlow = CALCULATE(
    [Net Cash Flow],
    DATESYTD(DateTable[Date])
)
RETURN OpeningBalance + CumulativeCashFlow
```

## Anomaly Detection

```dax
Avg Monthly Expenses = 
AVERAGEX(
    VALUES(DateTable[Month]),
    CALCULATE([Total Expenses])
)

Expense Anomaly Flag = 
IF([Total Expenses] > [Avg Monthly Expenses] * 1.2, "⚠ High", "Normal")
```
