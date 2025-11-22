# 📈 Advanced Multi-SIP & SWP Calculator

A comprehensive investment calculator for Systematic Investment Plans (SIP), Systematic Withdrawal Plans (SWP), with support for multiple portfolios, step-up investments, and tax calculations.

## ✨ Features

### 💰 Investment Management
- **Multiple SIP Portfolios** - Create and manage multiple independent investment portfolios
- **Existing Investments** - Include current investments in calculations
- **Step-up SIP** - Automatic annual increases in SIP contributions
- **Flexible Returns** - Different return rates for each portfolio

### 📉 Withdrawal Planning
- **Systematic Withdrawal Plan (SWP)** - Monthly or yearly withdrawals
- **Inflation-Adjusted Withdrawals** - Annual increases in withdrawal amounts
- **Post-Investment Growth** - Continue growing after SIP contributions end

### 📊 Financial Calculations
- **Capital Gains Tax** - Automatic tax calculation on profits
- **Inflation Adjustment** - Real purchasing power calculations
- **Wealth Gained** - Total profit including withdrawals
- **Multiple Time Periods** - Active SIP period + post-investment growth period

## 🚀 Quick Start

### Using the Calculator

1. **Open `index.html`** in any web browser (double-click the file)
2. **Set your parameters:**
   - Monthly SIP amount
   - Expected annual return (%)
   - Investment duration
   - Optional: Existing investment, SWP, tax rate, inflation
3. **Results update automatically** as you change values
4. **Add more portfolios** with the "➕ Add another SIP portfolio" button

### Running Tests

1. **Open `integration_tests.html`** in a web browser
2. **Click "🚀 Run Tests"** button
3. **View results** - All 8 tests should pass ✅

## 📋 Example Scenarios

### Scenario 1: Basic SIP
```
Monthly SIP: ₹10,000
Annual Return: 12%
Duration: 10 years

Result: ₹23,23,391
Invested: ₹12,00,000
Profit: ₹11,23,391
```

### Scenario 2: Existing Investment + SIP
```
Existing Investment: ₹5,00,000
Monthly SIP: ₹10,000
Annual Return: 12%
Duration: 10 years

Result: ₹39,73,584
Total Invested: ₹17,00,000
```

### Scenario 3: Step-up SIP with Withdrawal
```
Monthly SIP: ₹10,000
Annual SIP Increase: 10%
Monthly SWP: ₹5,000
Annual Return: 12%
Duration: 10 years

Result: Balanced growth with regular income
```

### Scenario 4: Retirement Planning
```
Monthly SIP: ₹25,000
Duration: 20 years (active investment)
Post-Investment Growth: 15 years
Annual Return: 12%

Result: Long-term wealth accumulation
```

## 🎯 Use Cases

- **Retirement Planning** - Calculate corpus needed for retirement
- **Goal-Based Investing** - Plan for specific financial goals
- **Income Planning** - Model regular withdrawals from investments
- **Portfolio Diversification** - Multiple portfolios with different returns
- **Tax Planning** - Estimate post-tax returns
- **Real Value Assessment** - Inflation-adjusted wealth calculations

## 🧮 Calculation Methodology

### SIP Calculation
The calculator uses **beginning-of-period** methodology:
```
For each month:
  1. Add SIP contribution
  2. Apply monthly return (SIP earns interest in deposit month)
  3. Apply SWP withdrawal
  4. Apply annual increases at year-end
```

This matches industry-standard financial calculators and Excel's `FV()` function with type=1.

### Formula Reference
```
FV = P × [((1 + r)^n - 1) / r] × (1 + r)

Where:
  P = Monthly SIP amount
  r = Monthly return rate (annual return / 12)
  n = Number of months
  (1 + r) = Beginning-of-period adjustment
```

### Multi-Portfolio Returns
When multiple portfolios exist, growth is calculated as a weighted average of all portfolio returns.

## 🧪 Testing

### Integration Tests
The project includes comprehensive integration tests that verify:

1. ✅ Basic SIP calculations
2. ✅ Existing investment handling
3. ✅ Step-up SIP (annual increases)
4. ✅ Monthly SWP withdrawals
5. ✅ Post-investment growth periods
6. ✅ Tax calculations
7. ✅ Lump sum investments
8. ✅ Edge cases (zero returns)

**To run tests:** Open `integration_tests.html` and click "Run Tests"

### Test Results
All tests verified against:
- Excel's `FV()` function
- Standard financial formulas
- Manual calculations

## 📁 Project Structure

```
sipcalc/
├── index.html              # Main calculator application
├── integration_tests.html  # Automated test suite
└── README.md              # This file
```

## 🔧 Technical Details

### Technologies
- Pure HTML, CSS, JavaScript
- No external dependencies
- Works offline
- Mobile responsive

### Browser Support
- ✅ Chrome/Edge
- ✅ Safari
- ✅ Firefox
- ✅ Opera

### Key Features
- **Dynamic Portfolio Management** - Add/remove portfolios on the fly
- **Real-time Calculations** - Results update as you type
- **Indian Rupee Formatting** - Proper currency display
- **Responsive Design** - Works on desktop and mobile
- **No Server Required** - Runs entirely in the browser

## 💡 Tips for Using the Calculator

### Planning Retirement
1. Set investment period to years until retirement
2. Set post-investment growth to expected retirement duration
3. Add SWP for monthly retirement income
4. Include inflation to see real purchasing power

### Multiple Investment Types
1. Create separate portfolios for different asset classes
2. Equity: Higher return (e.g., 12-15%)
3. Debt: Lower return (e.g., 6-8%)
4. See combined portfolio performance

### Step-up SIP Strategy
1. Set annual SIP increase (typically 5-10%)
2. Matches income growth
3. Significantly improves long-term returns
4. Example: ₹10k growing at 10%/year = ₹73L invested over 30 years

### Tax Efficiency
1. Enter expected LTCG tax rate (typically 10%)
2. See post-tax returns
3. Plan for tax-efficient withdrawals
4. Consider tax-saving instruments

## 📊 Understanding the Results

### Key Metrics

**Total Amount Invested**
- Sum of all SIP contributions + existing investments
- Does not include returns

**Maturity Value**
- Final corpus value after all growth and withdrawals
- Pre-tax amount

**Total Amount Withdrawn**
- Sum of all SWP withdrawals over time
- Part of your returns

**Wealth Gained**
- Total profit = (Maturity Value - Invested) + Withdrawn
- Represents actual wealth creation

**Value After Tax**
- Maturity value minus capital gains tax
- More realistic final amount

**Inflation-Adjusted Value**
- Purchasing power in today's terms
- Shows real value of money

## 🐛 Bug Fixes & Improvements

This calculator has been thoroughly tested and debugged:

### Fixed Issues
- ✅ Removed double growth calculation bug
- ✅ Proper sequencing of SIP → Growth → SWP
- ✅ Accurate multi-portfolio weighted returns
- ✅ Correct beginning-of-period SIP calculations

### Verified Against
- ✅ Excel financial functions
- ✅ Standard SIP formulas
- ✅ Manual month-by-month calculations
- ✅ Real financial calculators

## 🤝 Contributing

Found a bug or have a suggestion? This is a standalone project, but improvements are welcome:

- Test with different scenarios
- Report calculation discrepancies
- Suggest new features
- Improve documentation

## 📜 License

Free to use for personal financial planning and educational purposes.

## ⚠️ Disclaimer

This calculator is for illustrative purposes only. Actual investment returns may vary based on:
- Market conditions
- Fund performance
- Expense ratios
- Tax regulations
- Inflation rates

Always consult with a qualified financial advisor before making investment decisions.

---

## 🎓 Learning Resources

### Understanding SIP
- **Systematic Investment Plan** - Regular monthly investments
- **Rupee Cost Averaging** - Buy more units when prices are low
- **Power of Compounding** - Returns generate returns over time

### Understanding SWP
- **Systematic Withdrawal Plan** - Regular income from investments
- **Capital Preservation** - Withdraw only growth, preserve capital
- **Tax Efficiency** - Spread capital gains over multiple years

### Financial Planning Basics
1. **Emergency Fund** - 6 months expenses (not for investment)
2. **Goal Setting** - Define specific financial goals
3. **Asset Allocation** - Diversify across equity/debt/gold
4. **Regular Review** - Rebalance portfolio annually
5. **Stay Disciplined** - Continue SIP through market ups and downs

---

**Made with ❤️ for better financial planning**

**Version:** 2.0 (Tested & Verified)

**Last Updated:** November 2025

