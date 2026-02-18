# Data Cleaning Log

Dataset: toSend.xlsx  
Time Period: Jan 2023 – Dec 2023  
Total Records: 9,498  

---

## 1. Initial Inspection

- Checked total row count and column consistency.
- Verified that each row represents one completed transaction.
- Scanned for blank rows and inconsistent formatting.

---

## 2. Handling Missing Values

### Categorical Columns
- Replaced blanks, “UNKNOWN”, and “ERROR” values with:
  → "Not Specified"
- Ensured consistent spelling and capitalization across:
  - Item
  - Payment Method
  - Location

### Numeric Columns
- Identified missing values in:
  - Quantity
  - Price Per Unit
  - Total Spent
- Instead of dropping rows, imputed values to preserve transaction count.
- Recalculated Total Spent where needed using:
  Quantity × Price Per Unit

---

## 3. Data Validation

- Verified that:
  Total Spent = Quantity × Price Per Unit
- Checked for unrealistic values:
  - No negative quantities
  - No zero-price transactions
  - No extreme outliers
- Confirmed item price ranges were consistent.

---

## 4. Date Formatting

- Converted Transaction Date to proper date format.
- Extracted:
  - Month (for trend analysis)
  - Day of Week (for pattern analysis)

---

## 5. Standardization

- Cleaned extra spaces and inconsistent casing.
- Ensured uniform naming for:
  - Payment Methods (Cash, Credit Card, Digital Wallet)
  - Locations (In-store, Takeaway, Not Specified)

---

## 6. Feature Preparation for Dashboard

Created derived metrics using pivots and formulas:

- Total Revenue
- Total Orders
- Total Items Sold
- Average Order Value (AOV)
- Revenue by Item
- Revenue by Payment Method
- Revenue by Location
- Monthly Revenue
- Day-of-Week Revenue

---

## Final Result

- Cleaned dataset with consistent formatting.
- No dropped transactions.
- Revenue calculations validated.
- Ready for KPI generation and dashboard analysis.

