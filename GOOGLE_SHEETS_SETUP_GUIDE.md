# Annual Budget & Finance Tracker - Google Sheets Setup Guide

## Quick Start

To create this spreadsheet in Google Sheets, follow these steps:

### Step 1: Create a New Google Sheet
1. Go to [Google Sheets](https://sheets.google.com)
2. Click **"+ New"** → **"Blank spreadsheet"**
3. Name it: **"Annual Budget & Finance Tracker 2027"**

### Step 2: Copy Each Tab Below

For each section below, create a new tab with the exact name and copy-paste the structure and data.

---

## TAB 1: START HERE

**Instructions to display on first tab:**

```
╔════════════════════════════════════════════════════════════╗
║      🎯 ANNUAL BUDGET & FINANCE TRACKER 2027              ║
║          Welcome! Let's organize your finances.            ║
╠════════════════════════════════════════════════════════════╣

📋 QUICK START GUIDE

Step 1: Go to SETTINGS tab
  ✓ Set your budget year
  ✓ Choose your currency  
  ✓ Set your monthly income

Step 2: Set monthly BUDGET per category
  ✓ In JANUARY tab, set your spending limits
  ✓ Same amounts copy to other months

Step 3: Log your TRANSACTIONS
  ✓ In TRANSACTIONS tab, enter each expense
  ✓ Choose category from dropdown

Step 4: Check your DASHBOARD
  ✓ See your annual progress
  ✓ Track spending vs budget

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

📊 WHAT'S INCLUDED

✅ Annual Dashboard with charts
✅ 12 Monthly Budget Trackers
✅ Transaction Journal
✅ Budget vs Actual Comparison
✅ Savings Goals Tracker
✅ Debt Tracker
✅ Bills Tracker
✅ Subscriptions Tracker
✅ Net Worth Calculator
✅ Annual Overview
✅ Automatic calculations & formulas
✅ All data updates in real-time

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

❓ NEED HELP?

• All formulas are pre-built — just enter your numbers
• No complex Excel knowledge needed
• Works in Google Sheets AND Excel
• Fully customizable
• Currency auto-formats to USD

Next Step → Go to SETTINGS tab →
```

---

## TAB 2: SETTINGS

**Layout:**

| | A | B | C | D | E | F | G | H |
|---|---|---|---|---|---|---|---|---|
| **1** | **BUDGET CONFIGURATION** | | | | | | | |
| **2** | Budget Year | 2027 | | | | | | |
| **3** | Currency | USD | | | | | | |
| **4** | Currency Symbol | $ | | | | | | |
| **6** | **INCOME CATEGORIES** | | | | | | | |
| **7** | Salary | Freelance | Side Hustle | Bonus | Other | | | |
| **8** | $4,000 | $500 | $200 | $0 | $0 | | | |
| **9** | **TOTAL MONTHLY INCOME** | | =SUM(B8:F8) | | | | | |
| **11** | **EXPENSE CATEGORIES** | | | | | | | |
| **12** | Housing | Utilities | Groceries | Transport | Insurance | Healthcare | Dining | Entertainment |
| **13** | $1,200 | $200 | $400 | $250 | $150 | $100 | $150 | $200 |
| **14** | Shopping | Education | Travel | Personal | Other | | | |
| **15** | $100 | $50 | $100 | $80 | $120 | | | |
| **16** | **TOTAL BUDGET** | | | | | | | |
| **17** | =SUM(B13:B15,D13:E14) | | | | | | | |
| **19** | **SAVINGS CATEGORIES** | | | | | | | |
| **20** | Emergency Fund | Vacation | Investing | Home | Car | Other | | |
| **21** | $300 | $200 | $500 | $100 | $150 | $80 | | |
| **22** | **TOTAL SAVINGS** | | | | | | | |
| **23** | =SUM(B21:G21) | | | | | | | |
| **25** | **DEBT CATEGORIES** | | | | | | | |
| **26** | Credit Card | Student Loan | Auto Loan | Medical | Other | | | |

---

## TAB 3: TRANSACTIONS

**Headers:** Date | Type | Category | Description | Amount | Month | Account

**Sample Data:**

| Date | Type | Category | Description | Amount | Month | Account |
|------|------|----------|-------------|--------|-------|---------|
| 1/5/2027 | Expense | Groceries | Walmart | $85.50 | January | Checking |
| 1/8/2027 | Income | Salary | Monthly Salary | $4,000.00 | January | Checking |
| 1/10/2027 | Expense | Transportation | Gas Station | $50.00 | January | Checking |
| 1/15/2027 | Expense | Utilities | Electric Bill | $120.00 | January | Checking |
| 1/20/2027 | Expense | Housing | Rent Payment | $1,200.00 | January | Checking |
| 1/25/2027 | Expense | Dining Out | Restaurant | $45.99 | January | Checking |
| 2/3/2027 | Expense | Groceries | Target | $72.00 | February | Checking |
| 2/8/2027 | Income | Salary | Monthly Salary | $4,000.00 | February | Checking |
| 2/12/2027 | Expense | Transportation | Gas Station | $55.00 | February | Checking |
| 2/18/2027 | Expense | Utilities | Water Bill | $70.00 | February | Checking |

**Add Data Validation (Dropdowns):**

- **Column B (Type):** Dropdown = Income, Expense, Savings, Debt Payment
- **Column C (Category):** Dropdown = All expense categories from SETTINGS
- **Column G (Account):** Dropdown = Checking Account, Savings Account, Credit Card, Cash, Other

---

## TAB 4: DASHBOARD

**Annual Finance Dashboard 2027**

| | A | B | C |
|---|---|---|---|
| **1** | **ANNUAL FINANCE DASHBOARD** | | |
| **2** | | | |
| **3** | **ANNUAL TOTALS** | | |
| **4** | Total Income | =SUMIF(TRANSACTIONS!B:B,"Income",TRANSACTIONS!E:E) | |
| **5** | Total Expenses | =SUMIF(TRANSACTIONS!B:B,"Expense",TRANSACTIONS!E:E) | |
| **6** | Total Savings | =SUMIF(TRANSACTIONS!B:B,"Savings",TRANSACTIONS!E:E) | |
| **7** | Remaining Balance | =B4-B5-B6 | |
| **8** | | | |
| **9** | **KEY METRICS** | | |
| **10** | Savings Rate | =IFERROR(B6/B4*100,0)% | |
| **11** | Monthly Avg Expenses | =B5/12 | |
| **12** | Monthly Avg Savings | =B6/12 | |
| **13** | Monthly Avg Income | =B4/12 | |
| **14** | | | |
| **15** | **TOP EXPENSE CATEGORIES** | Category | Amount |
| **16** | 1. | Housing | $14,400 |
| **17** | 2. | Dining Out | $1,800 |
| **18** | 3. | Transportation | $3,000 | 
| **19** | 4. | Utilities | $2,400 |
| **20** | 5. | Other | $26,900 |

**Add Charts:**

1. **Chart 1: Income vs Expenses**
   - Type: Column Chart
   - Data: B4:B5 (Total Income, Total Expenses)
   - Title: "Income vs Expenses"

2. **Chart 2: Expense Breakdown**
   - Type: Pie Chart
   - Data: From expense categories
   - Title: "Where Your Money Goes"

3. **Chart 3: Monthly Trend**
   - Type: Line Chart
   - Data: From ANNUAL_OVERVIEW tab
   - Title: "Monthly Income & Expenses Trend"

---

## TAB 5: ANNUAL OVERVIEW

| Month | Income | Expenses | Savings | Remaining | Savings Rate |
|-------|--------|----------|---------|-----------|--------------|
| January | $4,700 | $2,500 | $1,000 | $1,200 | 21.3% |
| February | $4,700 | $2,450 | $1,050 | $1,200 | 22.3% |
| March | $4,700 | $2,400 | $1,100 | $1,200 | 23.4% |
| April | $4,700 | $2,300 | $1,200 | $1,200 | 25.5% |
| May | $4,700 | $2,350 | $1,150 | $1,200 | 24.5% |
| June | $4,700 | $2,400 | $1,100 | $1,200 | 23.4% |
| July | $4,700 | $2,500 | $900 | $1,300 | 19.1% |
| August | $4,700 | $2,600 | $1,000 | $1,100 | 21.3% |
| September | $4,700 | $2,450 | $1,100 | $1,150 | 23.4% |
| October | $4,700 | $2,350 | $1,200 | $1,150 | 25.5% |
| November | $4,700 | $2,450 | $1,150 | $1,100 | 24.5% |
| December | $4,700 | $2,550 | $1,000 | $1,150 | 21.3% |
| **TOTAL** | **$56,400** | **$30,400** | **$13,050** | **$12,950** | **23.1%** |

**Formulas for each month row:**
- Income: =SUMIF(TRANSACTIONS!F:F,"January",TRANSACTIONS!E:E) [change month for each row]
- Expenses: =SUMIF(TRANSACTIONS!F:F,"January",TRANSACTIONS!B:B,TRANSACTIONS!E:E) [where Type = Expense]
- Savings: =SUMIF(TRANSACTIONS!F:F,"January",TRANSACTIONS!B:B,TRANSACTIONS!E:E) [where Type = Savings]

---

## TAB 6-17: JANUARY through DECEMBER

**Each month has identical structure. Here's JANUARY:**

| Category | Budget | Actual | Difference | Status |
|----------|--------|--------|-----------|--------|
| **INCOME** | | | | |
| Salary | $4,000 | $4,000 | $0 | ✓ |
| Freelance | $500 | $520 | $20 | ✓ |
| Side Hustle | $200 | $180 | -$20 | |
| **TOTAL INCOME** | **$4,700** | **$4,700** | **$0** | |
| | | | | |
| **EXPENSES** | | | | |
| Housing | $1,200 | $1,200 | $0 | ✓ |
| Utilities | $200 | $185 | $15 | ✓ |
| Groceries | $400 | $475 | -$75 | ✗ |
| Transportation | $250 | $220 | $30 | ✓ |
| Insurance | $150 | $150 | $0 | ✓ |
| Healthcare | $100 | $90 | $10 | ✓ |
| Dining Out | $150 | $190 | -$40 | ✗ |
| Entertainment | $200 | $180 | $20 | ✓ |
| Shopping | $100 | $80 | $20 | ✓ |
| Education | $50 | $60 | -$10 | |
| Travel | $100 | $70 | $30 | ✓ |
| Personal | $80 | $90 | -$10 | |
| Other | $120 | $110 | $10 | ✓ |
| **TOTAL EXPENSES** | **$2,500** | **$2,600** | **-$100** | |
| | | | | |
| **SAVINGS** | | | | |
| Emergency Fund | $300 | $300 | $0 | ✓ |
| Vacation | $200 | $150 | $50 | |
| Investing | $500 | $550 | -$50 | |
| **TOTAL SAVINGS** | **$1,000** | **$1,000** | **$0** | |
| | | | | |
| **SUMMARY** | | | | |
| Income | | $4,700 | | |
| - Expenses | | $2,600 | | |
| - Savings | | $1,000 | | |
| = Remaining | | $1,100 | | |

**Formulas:**
- Difference = Actual - Budget
- Status: IF(Actual<=Budget,"✓","✗")

---

## TAB 18: SAVINGS GOALS

| Goal | Target | Saved | Remaining | Progress | Progress % |
|------|--------|-------|-----------|----------|-----------|
| Emergency Fund | $5,000 | $2,500 | $2,500 | 50% | =C2/B2 |
| Vacation 2027 | $2,000 | $800 | $1,200 | 40% | =C3/B3 |
| New Car | $10,000 | $3,000 | $7,000 | 30% | =C4/B4 |
| Home Down Payment | $50,000 | $15,000 | $35,000 | 30% | =C5/B5 |

**Conditional Formatting:**
- Progress bars: Green gradient from 0-100%
- Color scale: Red (0%) → Yellow (50%) → Green (100%)

---

## TAB 19: DEBT TRACKER

| Debt | Balance | APR | Min Payment | Extra Payment | Total Monthly | Months to Payoff |
|------|---------|-----|-------------|----------------|----------------|------------------|
| Credit Card | $3,500 | 22.9% | $100 | $50 | $150 | 22 |
| Student Loan | $12,000 | 5.5% | $200 | $50 | $250 | 64 |
| Auto Loan | $8,500 | 7.2% | $300 | $0 | $300 | 36 |
| **TOTALS** | **$24,000** | | **$600** | **$100** | **$700** | |

**Formulas:**
- Total Monthly = Min Payment + Extra Payment
- Months to Payoff = LOG((Min+Extra)/(Min+Extra-Balance*APR/12))/LOG(1+APR/12)

---

## TAB 20: BILLS

| Bill | Amount | Due Date | Frequency | Status | Next Due |
|------|--------|----------|-----------|--------|----------|
| Rent | $1,200 | 1 | Monthly | Paid | 2/1/2027 |
| Internet | $65 | 15 | Monthly | Paid | 2/15/2027 |
| Electric | $120 | 20 | Monthly | Due | 1/20/2027 |
| Insurance | $150 | 1 | Monthly | Paid | 2/1/2027 |
| Water | $60 | 11 | Monthly | Due | 2/11/2027 |
| Phone | $85 | 25 | Monthly | Upcoming | 2/25/2027 |

**Conditional Formatting:**
- Paid = Green background
- Due = Yellow background
- Overdue = Red background

**Formula for Status:**
```
=IF(TODAY()>Next_Due_Date,"Overdue",IF(TODAY()=Due_Date,"Due","Paid"))
```

---

## TAB 21: SUBSCRIPTIONS

| Subscription | Monthly Cost | Annual Cost | Renewal Frequency | Next Renewal |
|--------------|--------------|-------------|-------------------|--------------|
| Netflix | $15.99 | $191.88 | Monthly | 2/8/2027 |
| Spotify | $11.99 | $143.88 | Monthly | 2/1/2027 |
| Canva Pro | $15 | $180 | Monthly | 2/15/2027 |
| Adobe CC | $54.99 | $659.88 | Monthly | 2/5/2027 |
| Gym | $50 | $600 | Monthly | 2/1/2027 |
| Audible | $14.95 | $179.40 | Monthly | 2/20/2027 |
| **TOTAL** | **$162.92** | **$1,955.04** | | |

**Formulas:**
- Annual Cost = Monthly Cost × 12
- Total Monthly = SUM(all monthly costs)
- Total Annual = SUM(all annual costs)

---

## TAB 22: NET WORTH

### ASSETS

| Asset | Amount |
|-------|--------|
| Checking Account | $5,500 |
| Savings Account | $15,000 |
| Investment Account | $25,000 |
| Retirement (401k) | $45,000 |
| Primary Home | $350,000 |
| Vehicle | $25,000 |
| **TOTAL ASSETS** | **$465,500** |

### LIABILITIES

| Liability | Amount |
|-----------|--------|
| Credit Card Debt | $3,500 |
| Student Loans | $12,000 |
| Auto Loan | $8,500 |
| Mortgage | $280,000 |
| **TOTAL LIABILITIES** | **$304,000** |

### NET WORTH

| | Amount |
|---|--------|
| Total Assets | $465,500 |
| - Total Liabilities | $304,000 |
| = **NET WORTH** | **$161,500** |

**Formula:**
```
Net Worth = SUM(Assets) - SUM(Liabilities)
```

**Add Chart:**
- Donut chart showing Assets vs Liabilities

---

## 🎨 FORMATTING GUIDE

### Colors
- **Header Background:** Dark Gray (#2C3E50)
- **Header Text:** White
- **Section Headers:** Light Gray (#ECF0F1)
- **Positive Values:** Green (#27AE60)
- **Negative Values:** Red (#E74C3C)
- **Accent Color:** Blue (#3498DB)
- **Grid Lines:** Light Gray (#BDC3C7)

### Fonts
- **Headers:** Arial Bold, 12pt
- **Section Titles:** Arial Bold, 11pt
- **Data:** Arial, 10pt
- **Totals:** Arial Bold, 10pt

### Number Formatting
- Currency: $ #,##0.00
- Percentage: 0.0%
- Date: MM/DD/YYYY

### Cell Borders
- Thin borders around all data cells
- Bold borders around sections
- Double border around totals

---

## ✅ CONDITIONAL FORMATTING RULES

### Dashboard
- Income/Savings: Green if > 0
- Expenses: Red if > budget
- Remaining: Green if positive

### Monthly Budget Tabs
- Over budget: Red background
- On budget: Green background

### Debt Tracker
- High APR (>10%): Red background
- Medium APR (5-10%): Yellow background
- Low APR (<5%): Green background

### Bills
- Overdue: Red background + bold text
- Due: Yellow background
- Paid: Green background

### Savings Goals
- 0-25% complete: Red
- 25-50% complete: Yellow
- 50-75% complete: Light Green
- 75-100% complete: Dark Green

---

## 📊 CHARTS TO CREATE

### 1. Dashboard Charts

**Chart 1: Income vs Expenses (Column Chart)**
- X-axis: "Income" | "Expenses"
- Y-axis: Amount in USD
- Colors: Green for Income, Red for Expenses

**Chart 2: Expense Breakdown (Pie Chart)**
- Data: Categories and amounts from monthly budget
- Shows % breakdown

**Chart 3: Monthly Trend (Line Chart)**
- X-axis: Months (Jan-Dec)
- Y-axis: Amount in USD
- 3 lines: Income, Expenses, Savings

### 2. Savings Goals Chart (Progress Bars)
- Type: Horizontal bar chart
- Shows progress toward each goal
- Color gradient: Red → Green

### 3. Net Worth Chart (Donut Chart)
- Shows Assets vs Liabilities
- Color: Blue for Assets, Red for Liabilities

---

## 🔒 DATA VALIDATION & PROTECTION

### Data Validation (Dropdowns)

1. **TRANSACTIONS tab, Column B (Type):**
   - Options: Income | Expense | Savings | Debt Payment
   - Type: List

2. **TRANSACTIONS tab, Column C (Category):**
   - Options: Housing, Utilities, Groceries, Transportation, Insurance, Healthcare, Dining Out, Entertainment, Shopping, Education, Travel, Personal, Other
   - Type: List

3. **TRANSACTIONS tab, Column G (Account):**
   - Options: Checking Account | Savings Account | Credit Card | Cash | Other
   - Type: List

4. **BILLS tab, Column E (Status):**
   - Options: Paid | Due | Overdue
   - Type: List (or use formula)

5. **BILLS tab, Column D (Frequency):**
   - Options: Weekly | Bi-Weekly | Monthly | Quarterly | Annual
   - Type: List

### Sheet Protection
- Protect SETTINGS tab from accidental editing
- Allow editing only on: TRANSACTIONS, Monthly tabs, and Goal tabs
- Keep formulas read-only

---

## 💡 USAGE TIPS

1. **Update TRANSACTIONS regularly** - This is the main data entry point
2. **Budget amounts stay the same each month** - Copy January to other months
3. **Dashboard updates automatically** - No manual calculations needed
4. **All formulas use SUMIF** - They find data by month/category
5. **Currency auto-converts** - Change in SETTINGS, applies everywhere

---

## 🚀 NEXT STEPS

1. ✅ Create each tab with provided data
2. ✅ Add data validation (dropdowns)
3. ✅ Apply conditional formatting
4. ✅ Create charts
5. ✅ Format cells (colors, fonts, numbers)
6. ✅ Test all formulas
7. ✅ Export to Excel (.xlsx)
8. ✅ Create PDF guide
9. ✅ Upload to Etsy

