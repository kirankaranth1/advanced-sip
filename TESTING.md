# 🧪 How to Run the Integration Tests

## Quick Start

### Open the Integration Tests:
```bash
cd /Users/kiran/Desktop/code/playground/sipcalc
open integration_tests.html
```

Or simply double-click `integration_tests.html` in Finder.

---

## What Are Integration Tests?

The **integration tests** actually test your real `index.html` calculator, unlike the previous unit tests which had their own separate calculation logic.

### How It Works:

1. **Loads Real Calculator**: Opens `index.html` in an invisible iframe
2. **Sets Input Values**: Programmatically fills in form fields
3. **Triggers Calculation**: Calls the actual `calculateSip()` function
4. **Reads Results**: Extracts values from the DOM
5. **Verifies**: Compares actual vs expected results

---

## Test Suite

The integration tests include 10 comprehensive test cases:

1. ✅ **Basic SIP** - Simple ₹10k/month for 10 years at 12%
2. ✅ **Existing Investment** - ₹5L existing + ₹10k/month SIP
3. ✅ **Step-up SIP** - 10% annual increase in SIP amount
4. ✅ **Monthly SWP** - ₹10k SIP with ₹5k monthly withdrawal
5. ✅ **Post-Investment Growth** - 10y SIP + 10y additional growth
6. ✅ **Tax Calculation** - 10% capital gains tax application
7. ✅ **Existing Only** - ₹10L lump sum, no SIP
8. ✅ **Yearly SWP** - Annual withdrawals instead of monthly
9. ✅ **Zero Return** - Edge case with 0% return rate
10. ✅ **Inflation** - 6% inflation adjustment over 10 years

---

## Understanding the Results

### Test Display:

**Green border = PASS ✅**
- Actual results match expected values (within tolerance)
- Calculator is working correctly for this scenario

**Red border = FAIL ❌**
- Results don't match expectations
- Indicates a bug in the calculator logic
- Shows the difference between expected and actual

### Tolerance:

Tests allow a tolerance of ₹5,000 (or specified amount) to account for:
- Floating-point precision differences
- Rounding variations
- Minor calculation variations

---

## Features

### Interactive Calculator View:
Click **"Show/Hide Calculator"** button to:
- See the actual calculator interface
- Manually verify results
- Understand what inputs the test is using

### Detailed Output:
Each test shows:
- Test name and description
- Input parameters used
- Expected vs actual values for each metric
- Exact difference amounts for failures

### Summary Statistics:
Top of page shows:
- Total tests run
- Number passed (green)
- Number failed (red)

---

## What to Check

### If All Tests Pass (Green):
✅ Your `index.html` calculator is working correctly!
✅ Calculations are accurate
✅ No bugs detected

### If Tests Fail (Red):
❌ There's a bug in the calculation logic
❌ Check the failed test details
❌ Compare expected vs actual values
❌ Look at the difference amounts

---

## Example Expected Results

### Test 1: ₹10k/month, 12% return, 10 years
- **Total Invested**: ₹12,00,000
- **Maturity Value**: ₹23,00,387
- **Wealth Gained**: ₹11,00,387

This is the standard SIP formula result:
```
FV = P × [((1 + r)^n - 1) / r] × (1 + r)
where P = 10,000, r = 0.01, n = 120
```

---

## Troubleshooting

### Calculator Not Loading:
- Make sure `index.html` is in the same folder
- Check browser console for errors (F12 → Console tab)

### Tests Not Running:
- Wait a few seconds for iframe to load
- Refresh the page
- Check that JavaScript is enabled

### All Tests Failing:
- There may be a critical bug in `index.html`
- Open browser console to see error messages
- Verify `calculateSip()` function exists

---

## Comparison: Unit Tests vs Integration Tests

### ❌ Old `tests.html` (Unit Tests):
- Tests its own `calculateSipCorrect()` function
- Does NOT test the real calculator
- Can pass even if `index.html` is broken

### ✅ New `integration_tests.html`:
- Tests the actual `index.html` calculator
- Loads the real calculator in an iframe
- Guarantees the live calculator works correctly

---

## Browser Compatibility

Works in all modern browsers:
- ✅ Chrome/Edge
- ✅ Safari
- ✅ Firefox
- ✅ Opera

---

## Files Overview

```
/sipcalc/
├── index.html                  → Main calculator (THIS IS WHAT'S TESTED)
├── integration_tests.html      → Real integration tests ⭐ USE THIS
├── tests.html                  → Old unit tests (not connected to index.html)
├── manual_verification.html    → Visual breakdown
├── BUG_REPORT.md              → Bug documentation
└── TESTING.md                 → This file
```

---

## Quick Commands

```bash
# Run integration tests
open integration_tests.html

# View calculator
open index.html

# See all files
ls -la

# Open all at once
open integration_tests.html index.html
```

---

**🎯 Bottom Line:** Use `integration_tests.html` to verify your calculator is working correctly. Green = good, red = bug!

