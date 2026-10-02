# Annual Budget & Finance Tracker - Product Structure

## 🎯 Stratégie Commerciale

**Positionnement** : All-in-One Annual Budget & Finance Tracker
**Prix** : $14.99 (promotion lancement : $9.99)
**Format** : Google Sheets + Excel
**Public** : Tous (familles, étudiants, entrepreneurs, professionnels)
**Langue** : Anglais (US)
**Devise** : USD

---

## 📊 Architecture du Produit

### PHASE 1 : ONGLETS FONDAMENTAUX (7 onglets)

| # | Onglet | Fonction |
|---|--------|----------|
| 1 | **START HERE** | Guide d'introduction - PREMIER ONGLET |
| 2 | **SETTINGS** | Configuration année, devise, catégories |
| 3 | **TRANSACTIONS** | Journal de toutes les dépenses/revenus |
| 4 | **DASHBOARD** | Vue d'ensemble annuelle |
| 5 | **ANNUAL OVERVIEW** | Résumé 12 mois |
| 6-17 | **JAN → DEC** | Budget & suivi mensuel |

### PHASE 2 : ONGLETS SPÉCIALISÉS (5 onglets)

| # | Onglet | Fonction |
|---|--------|----------|
| 18 | **SAVINGS GOALS** | Objectifs d'épargne avec barres de progression |
| 19 | **DEBT TRACKER** | Suivi des dettes et intérêts |
| 20 | **BILLS** | Factures récurrentes |
| 21 | **SUBSCRIPTIONS** | Abonnements mensuels/annuels |
| 22 | **NET WORTH** | Patrimoine net (actifs - passifs) |

---

## 🟢 FEUILLE 1 : START HERE

**Fonction** : Premier onglet que le client voit

```
╔══════════════════════════════════════════════════════════════╗
║                                                              ║
║         🎯 ANNUAL BUDGET & FINANCE TRACKER 2027             ║
║                                                              ║
║        Welcome! Let's organize your finances.               ║
║                                                              ║
╠══════════════════════════════════════════════════════════════╣
║                                                              ║
║  📋 QUICK START GUIDE                                       ║
║                                                              ║
║  Step 1: Go to SETTINGS tab                                ║
║          ✓ Set your budget year                            ║
║          ✓ Choose your currency                            ║
║          ✓ Customize your categories (optional)            ║
║                                                              ║
║  Step 2: Enter your MONTHLY INCOME                         ║
║          ✓ In SETTINGS, enter your salary & other income  ║
║                                                              ║
║  Step 3: Set monthly BUDGET per category                  ║
║          ✓ In JANUARY tab, set your spending limits       ║
║          ✓ Same amounts copy to other months              ║
║                                                              ║
║  Step 4: Log your TRANSACTIONS                            ║
║          ✓ In TRANSACTIONS tab, enter each expense        ║
║          ✓ Categories auto-fill                           ║
║                                                              ║
║  Step 5: Check your DASHBOARD                             ║
║          ✓ See your annual progress                       ║
║          ✓ Track spending vs budget                       ║
║                                                              ║
╠══════════════════════════════════════════════════════════════╣
║                                                              ║
║  📊 WHAT'S INCLUDED                                         ║
║                                                              ║
║  ✅ Annual Dashboard                                        ║
║  ✅ 12 Monthly Budgets                                      ║
║  ✅ Transaction Tracker                                     ║
║  ✅ Budget vs Actual Comparison                            ║
║  ✅ Savings Goals                                           ║
║  ✅ Debt Tracker                                            ║
║  ✅ Bills & Subscriptions                                   ║
║  ✅ Net Worth Calculator                                    ║
║  ✅ Automatic Charts & Reports                             ║
║                                                              ║
╠══════════════════════════════════════════════════════════════╣
║                                                              ║
║  ❓ NEED HELP?                                             ║
║                                                              ║
║  • All formulas are pre-built — just enter your numbers   ║
║  • No complex Excel knowledge needed                      ║
║  • Works in Google Sheets AND Excel                       ║
║  • Fully customizable                                      ║
║                                                              ║
║  NEXT → Go to SETTINGS                                     ║
║                                                              ║
╚══════════════════════════════════════════════════════════════╝
```

**Contenu textuel simple** (pas de formules compliquées)

---

## 🟢 FEUILLE 2 : SETTINGS

**Fonction** : Centralise toute la configuration

### Section A : Budget Configuration

```
┌─────────────────────────────────────┐
│ BUDGET CONFIGURATION                │
├─────────────────────────────────────┤
│ Budget Year              │ 2027     │
│ Currency                 │ USD      │
│ Currency Symbol          │ $        │
└─────────────────────────────────────┘
```

**Cellules** :
- A1 = "Budget Year" | B1 = 2027 (modifiable)
- A2 = "Currency" | B2 = "USD" (dropdown)
- A3 = "Currency Symbol" | B3 = "$"

### Section B : Income Categories

```
┌──────────────────────────────────────────────────┐
│ INCOME CATEGORIES (Monthly)                      │
├──────────┬──────────┬──────────┬──────────┬──────┤
│ Salary   │ Freelance│ Side Gig │ Bonus   │ Other │
│ $4,000   │ $500     │ $200     │ $0      │ $0    │
└──────────┴──────────┴──────────┴──────────┴──────┘
```

**Ligne 5** :
- A5 à G5 = Catégories de revenus (modifiables)
- A6 à G6 = Montants mensuels (modifiables)

**Formule en A7** : `=SUM(A6:G6)` → Total Monthly Income

### Section C : Expense Categories

```
┌──────────────────────────────────────────────────────────────┐
│ EXPENSE CATEGORIES                                           │
├──────────┬──────────┬──────────┬──────────┬──────────┬──────┤
│ Housing  │Utilities │Groceries │Transport │Insurance │Other │
│ $1,200   │ $200     │ $400     │ $250     │ $150     │ $100  │
└──────────┴──────────┴──────────┴──────────┴──────────┴──────┘
```

**Ligne 9** :
- Catégories de dépenses (modifiables)

**Ligne 10** :
- Budgets par catégorie (modifiables)

### Section D : Savings Categories

```
┌──────────────────────────────────────┐
│ SAVINGS CATEGORIES                   │
├──────────┬──────────┬──────────┬──────┤
│Emergency │Vacation  │Investing │Other │
│ $300     │ $200     │ $500     │ $100 │
└──────────┴──────────┴──────────┴──────┘
```

### Section E : Debt Categories

```
┌──────────────────────────────────────┐
│ DEBT CATEGORIES                      │
├──────────┬──────────┬──────────┬──────┤
│ Credit   │ Student  │ Auto     │Other │
│ Card     │ Loan     │ Loan     │      │
└──────────┴──────────┴──────────┴──────┘
```

---

## 🟢 FEUILLE 3 : TRANSACTIONS

**Fonction** : Journal de toutes les dépenses/revenus

```
┌─────────┬────────┬──────────┬─────────────┬──────────┬────────┐
│ Date    │ Type   │ Category │ Description │ Amount   │ Month  │
├─────────┼────────┼──────────┼─────────────┼──────────┼────────┤
│ 1/5/27  │Expense │Groceries │Walmart      │ $85.50   │January │
│ 1/8/27  │ Income │Salary    │Monthly Pay  │ $4,000   │January │
│ 1/10/27 │Expense │Transport │Gas          │ $50.00   │January │
│ 1/15/27 │Expense │Utilities │Electric     │ $120     │January │
│ 1/20/27 │Expense │Housing   │Rent         │ $1,200   │January │
│ 1/25/27 │Expense │Dining    │Restaurant   │ $45.99   │January │
│ 2/3/27  │Expense │Groceries │Target       │ $72      │February│
│ 2/8/27  │ Income │Salary    │Monthly Pay  │ $4,000   │February│
└─────────┴────────┴──────────┴─────────────┴──────────┴────────┘
```

**Colonnes** :
- A = Date (MM/DD/YYYY)
- B = Type (Dropdown: Income / Expense / Savings)
- C = Category (Dropdown: utilise les catégories de SETTINGS)
- D = Description (texte libre)
- E = Amount (nombre)
- F = Month (auto-calcul ou dropdown)
- G = Account (Checking / Savings / Credit Card)

**Dropdowns** :
- B : Income | Expense | Savings | Debt Payment
- C : dynamique (utilise les listes de SETTINGS)
- G : Checking Account | Savings Account | Credit Card | Cash | Other

**Formule en F** : `=TEXT(A2,"MMMM")` → Auto-remplit le mois

---

## 🟢 FEUILLE 4 : DASHBOARD

**Fonction** : Vue d'ensemble annuelle en temps réel

```
╔══════════════════════════════════════════════════════════════╗
║                   2027 ANNUAL FINANCE DASHBOARD             ║
╠══════════════════════════════════════════════════════════════╣
║                                                              ║
║  ANNUAL TOTALS                                              ║
║  ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━  ║
║                                                              ║
║  Total Income              $72,000.00                        ║
║  Total Expenses            $48,500.00                        ║
║  Total Savings             $15,000.00                        ║
║  Remaining Balance          $8,500.00                        ║
║                                                              ║
║  ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━  ║
║                                                              ║
║  KEY METRICS                                                ║
║  ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━  ║
║                                                              ║
║  Savings Rate              20.8%      ████████░░░░░░░░░░░  ║
║  Monthly Average Expenses  $4,042     ████████░░░░░░░░░░░  ║
║  Monthly Average Savings   $1,250     ██░░░░░░░░░░░░░░░░░  ║
║                                                              ║
║  ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━  ║
║                                                              ║
║  TOP EXPENSE CATEGORIES                                     ║
║  ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━  ║
║                                                              ║
║  1. Housing        $14,400  (30%)     ███████░░░░░░░░░░░░  ║
║  2. Utilities       $2,400  (5%)      █░░░░░░░░░░░░░░░░░░  ║
║  3. Groceries       $5,400  (11%)     ██░░░░░░░░░░░░░░░░░  ║
║  4. Transportation  $3,000  (6%)      █░░░░░░░░░░░░░░░░░░  ║
║  5. Other          $23,300  (48%)     ███████████░░░░░░░░  ║
║                                                              ║
║  ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━  ║
║                                                              ║
║  CHARTS                                                     ║
║  ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━  ║
║                                                              ║
║  [INCOME VS EXPENSES CHART]                                 ║
║  [EXPENSE BREAKDOWN PIE CHART]                              ║
║  [MONTHLY TREND LINE CHART]                                 ║
║                                                              ║
╚══════════════════════════════════════════════════════════════╝
```

**Formules Dashboard** :

```
Total Income       = SUMIF(TRANSACTIONS!B:B,"Income",TRANSACTIONS!E:E)
Total Expenses     = SUMIF(TRANSACTIONS!B:B,"Expense",TRANSACTIONS!E:E)
Total Savings      = SUMIF(TRANSACTIONS!B:B,"Savings",TRANSACTIONS!E:E)
Remaining          = Total Income - Total Expenses - Total Savings
Savings Rate       = (Total Savings / Total Income) * 100
Monthly Avg Exp    = Total Expenses / 12
```

---

## 🟢 FEUILLE 5 : ANNUAL OVERVIEW

**Fonction** : Résumé 12 mois

```
┌──────────┬──────────┬──────────┬──────────┬──────────┬──────────┐
│ Month    │ Income   │ Expenses │ Savings  │ Actual   │ Diff     │
├──────────┼──────────┼──────────┼──────────┼──────────┼──────────┤
│ January  │ $4,700   │ $2,500   │ $1,000   │ $2,600   │ -$100    │
│ February │ $4,700   │ $2,450   │ $1,050   │ $2,550   │ +$50     │
│ March    │ $4,700   │ $2,400   │ $1,100   │ $2,500   │ +$100    │
│ April    │ $4,700   │ $2,300   │ $1,200   │ $2,400   │ +$200    │
│ May      │ $4,700   │ $2,350   │ $1,150   │ $2,450   │ +$150    │
│ June     │ $4,700   │ $2,400   │ $1,100   │ $2,500   │ +$100    │
│ TOTAL    │$28,200   │$14,400   │ $6,600   │$15,000   │ +$600    │
└──────────┴──────────┴──────────┴──────────┴──────────┴──────────┘
```

**Formules** :
- Income = SUM(JANUARY!A7, FEBRUARY!A7, etc.)
- Expenses = SUM(JANUARY!B7, FEBRUARY!B7, etc.)

---

## 🟢 FEUILLES 6-17 : JANUARY → DECEMBER

**Fonction** : Budget mensuel + suivi réel

**Structure identique pour chaque mois** :

```
╔════════════════════════════════════════════════════╗
║              JANUARY 2027 BUDGET                   ║
╠════════════════════════════════════════════════════╣
║                                                    ║
║  INCOME                                            ║
║  ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ ║
║  Salary              $4,000    (Budget) $4,000     ║
║  Freelance            $500     (Actual)  $520      ║
║  Side Gig             $200     (Actual)  $180      ║
║  ────────────────────────────────────────────────  ║
║  TOTAL INCOME        $4,700    (Actual) $4,700     ║
║                                                    ║
╠════════════════════════════════════════════════════╣
║  EXPENSES                                          ║
║  ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ ║
║  Housing    Budget: $1,200  Actual: $1,200  ✓     ║
║  Utilities  Budget: $200    Actual: $185    ✓     ║
║  Groceries  Budget: $400    Actual: $475    ✗     ║
║  Transport  Budget: $250    Actual: $220    ✓     ║
║  Insurance  Budget: $150    Actual: $150    ✓     ║
║  Dining     Budget: $150    Actual: $190    ✗     ║
║  Other      Budget: $100    Actual: $80     ✓     ║
║  ────────────────────────────────────────────────  ║
║  TOTAL EXP  Budget: $2,450   Actual: $2,500  -50   ║
║                                                    ║
╠════════════════════════════════════════════════════╣
║  SAVINGS                                           ║
║  ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ ║
║  Emergency Fund     Budget: $300   Actual: $300    ║
║  Vacation           Budget: $200   Actual: $150    ║
║  Investing          Budget: $500   Actual: $550    ║
║  ────────────────────────────────────────────────  ║
║  TOTAL SAVINGS      Budget: $1,000 Actual: $1,000  ║
║                                                    ║
╠════════════════════════════════════════════════════╣
║  SUMMARY                                           ║
║  ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ ║
║  Income              $4,700                        ║
║  - Expenses          $2,500                        ║
║  - Savings           $1,000                        ║
║  = Remaining         $1,200                        ║
║                                                    ║
╚════════════════════════════════════════════════════╝
```

**Colonnes** :

```
A        B              C          D         E
────────────────────────────────────────────────
Category  Description   Budget    Actual    Diff
Housing   Rent          1200      1200      0
Utilities Electric      200       185       +15
Groceries Walmart       400       475       -75
Transport Gas           250       220       +30
```

**Formules** :
```
E2 = D2 - C2                (Difference)
D2 = SUMIF(TRANSACTIONS, Month=January, Category=Housing)
C2 = from SETTINGS
```

---

## 🟢 FEUILLE 18 : SAVINGS GOALS

**Fonction** : Objectifs d'épargne avec barres de progression

```
┌───────────────────┬────────┬─────────┬─────────────┬──────────┐
│ Goal              │ Target │ Saved   │ Remaining   │ Progress │
├───────────────────┼────────┼─────────┼─────────────┼──────────┤
│ Emergency Fund    │ $5,000 │ $2,500  │ $2,500      │ 50% ████  │
│ Vacation 2027     │ $2,000 │ $800    │ $1,200      │ 40% ███░  │
│ New Car          │ $10,000│ $3,000  │ $7,000      │ 30% ██░░  │
│ Home Downpayment │ $50,000│ $15,000 │ $35,000     │ 30% ██░░  │
└───────────────────┴────────┴─────────┴─────────────┴──────────┘
```

**Formules** :
```
Remaining = Target - Saved
Progress  = (Saved / Target) * 100
Bar       = REPT("█",INT(Progress/10)) & REPT("░",10-INT(Progress/10))
```

---

## 🟢 FEUILLE 19 : DEBT TRACKER

**Fonction** : Suivi des dettes

```
┌─────────────────┬────────────┬────────┬──────────────┬────────┐
│ Debt            │ Balance    │ APR    │ Min Payment  │ Extra  │
├─────────────────┼────────────┼────────┼──────────────┼────────┤
│ Credit Card     │ $3,500     │ 22.9%  │ $100/month   │ $50    │
│ Student Loan    │ $12,000    │ 5.5%   │ $200/month   │ $50    │
│ Auto Loan       │ $8,500     │ 7.2%   │ $300/month   │ $0     │
├─────────────────┼────────────┼────────┼──────────────┼────────┤
│ TOTALS          │ $24,000    │ -      │ $600/month   │ $100   │
└─────────────────┴────────────┴────────┴──────────────┴────────┘
```

**Données clés** :
- Debt name
- Current balance
- Interest rate (APR)
- Minimum payment
- Extra payment
- Months to payoff

**Formule** : `Months to Payoff = LOG((Min + Extra)/(Min + Extra - Balance * APR/12)) / LOG(1 + APR/12)`

---

## 🟢 FEUILLE 20 : BILLS

**Fonction** : Factures récurrentes

```
┌─────────────────┬────────┬────────┬───────────┬──────────┐
│ Bill            │ Amount │ Due    │ Frequency │ Status   │
├─────────────────┼────────┼────────┼───────────┼──────────┤
│ Rent            │ $1,200 │ 1      │ Monthly   │ Paid     │
│ Internet        │ $65    │ 15     │ Monthly   │ Paid     │
│ Electric        │ $120   │ 20     │ Monthly   │ Due      │
│ Insurance       │ $150   │ 1      │ Monthly   │ Paid     │
│ Property Tax    │ $400   │ 25     │ Quarterly │ Due      │
└─────────────────┴────────┴────────┴───────────┴──────────┘
```

**Status** : Paid / Due / Overdue (conditional formatting)

---

## 🟢 FEUILLE 21 : SUBSCRIPTIONS

**Fonction** : Tous les abonnements en un seul endroit

```
┌─────────────────┬───────────────┬───────────────┬──────────┐
│ Subscription    │ Monthly Cost  │ Annual Cost   │ Renewal  │
├─────────────────┼───────────────┼───────────────┼──────────┤
│ Netflix         │ $15.99        │ $191.88       │ Monthly  │
│ Spotify         │ $11.99        │ $143.88       │ Monthly  │
│ Canva Pro       │ $15           │ $180          │ Monthly  │
│ Adobe CC        │ $54.99        │ $659.88       │ Monthly  │
│ Gym             │ $50           │ $600          │ Monthly  │
│ Audible         │ $14.95        │ $179.40       │ Monthly  │
├─────────────────┼───────────────┼───────────────┼──────────┤
│ TOTALS          │ $162.92/m     │ $1,955.04/y   │          │
└─────────────────┴───────────────┴───────────────┴──────────┘
```

**Formules** :
```
Annual Cost = Monthly Cost * 12
Total Annual = SUM(Annual Cost)
```

Cela permet à l'utilisateur de voir exactement combien il dépense en abonnements par an.

---

## 🟢 FEUILLE 22 : NET WORTH

**Fonction** : Patrimoine net (Actifs - Passifs)

```
╔══════════════════════════════════════════════════╗
║              NET WORTH STATEMENT                 ║
╠══════════════════════════════════════════════════╣
║                                                  ║
║  ASSETS                                          ║
║  ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━  ║
║  Checking Account        $5,500                  ║
║  Savings Account         $15,000                 ║
║  Investment Account      $25,000                 ║
║  Retirement (401k)       $45,000                 ║
║  Primary Home            $350,000                ║
║  Vehicle                 $25,000                 ║
║  ────────────────────────────────────────────   ║
║  TOTAL ASSETS            $465,500                ║
║                                                  ║
║  LIABILITIES                                     ║
║  ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━  ║
║  Credit Card Debt        $3,500                  ║
║  Student Loans           $12,000                 ║
║  Auto Loan               $8,500                  ║
║  Mortgage                $280,000                ║
║  ────────────────────────────────────────────   ║
║  TOTAL LIABILITIES       $304,000                ║
║                                                  ║
╠══════════════════════════════════════════════════╣
║  NET WORTH = ASSETS - LIABILITIES                ║
║  NET WORTH               $161,500                ║
╚══════════════════════════════════════════════════╝
```

**Formule** : `Net Worth = SUM(Assets) - SUM(Liabilities)`

---

## 🎨 DESIGN & FORMATTING

### Couleurs (Professional Finance Style)
- **Fond** : Blanc / Gris très clair (#F9F9F9)
- **En-têtes** : Gris foncé (#2C3E50)
- **Chiffres positifs** : Vert (#27AE60)
- **Chiffres négatifs** : Rouge (#E74C3C)
- **Accent** : Bleu professionnel (#3498DB)
- **Bordures** : Gris léger (#BDC3C7)

### Polices
- En-têtes : Bold, 14pt
- Titres de section : Bold, 12pt
- Données : Regular, 11pt

### Conditional Formatting
```
✓ Expenses Over Budget  → Rouge
✓ Savings on Track      → Vert
✓ Overdue Bills         → Rouge foncé
✓ Progress Bars         → Gradient vert
```

---

## 💾 FORMAT DE LIVRAISON

Le client recevra :

```
Annual_Budget_Finance_Tracker.xlsx
├── START HERE
├── SETTINGS
├── TRANSACTIONS
├── DASHBOARD
├── ANNUAL OVERVIEW
├── JANUARY → DECEMBER
├── SAVINGS GOALS
├── DEBT TRACKER
├── BILLS
├── SUBSCRIPTIONS
└── NET WORTH
```

Plus un fichier PDF :

```
START_HERE_GUIDE.pdf
├── How to download
├── How to open in Google Sheets
├── How to make a copy
├── Step-by-step tutorial
└── FAQ
```

---

## 💰 POSITIONNEMENT COMMERCIAL

**Vs Competitors** :
- Produit 1 (Etsy, $7.99) : Budget simple + 12 mois
- Produit 2 (Etsy, $14.99) : Budget + Debt + Bills
- **Notre produit ($14.99)** : Budget + Debt + Bills + Savings + Subscriptions + Net Worth + Dashboard + Annual Overview

**Avantage** :
"All-in-One Finance System - Everything You Need to Take Control of Your Money"

---

## 📈 STRATÉGIE ETSY

**Titre** :
"Annual Budget Spreadsheet | Finance Tracker | Google Sheets Budget | Monthly Budget Expenses | Savings Debt Bill Tracker"

**13 Tags** :
1. budget spreadsheet
2. finance tracker
3. budget planner
4. google sheets template
5. annual budget
6. expense tracker
7. budget template
8. money management
9. financial planning
10. debt tracker
11. bills tracker
12. savings goals
13. family budget

---

## ✅ PROCHAINES ÉTAPES

1. **Créer le fichier Excel** avec structure complète + données d'exemple
2. **Tester toutes les formules**
3. **Ajouter conditional formatting**
4. **Créer PDF guide**
5. **Créer images Canva** pour Etsy
6. **Publier sur Etsy**
7. **Tester le lien Google Sheets**

