Here’s a set of **practical exercises** to sharpen your skills with **Excel formulas and functions**. These will go from beginner to intermediate level — great for real-world practice!

------

## 📘 **Exercise Set: Excel Formulas & Functions**

------

### ✅ **1. Basic Arithmetic & Cell References**

📋 Data:



| A       | B     | C        |
| ------- | ----- | -------- |
| Product | Price | Quantity |
| Apple   | 2     | 4        |
| Banana  | 3     | 2        |
| Orange  | 1.5   | 5        |

🔧 **Tasks:**

- In **D2**, calculate total for each product: `=B2*C2`
- Use **AutoFill** to apply to all rows

------

### ✅ **2. Use `IF()` Function**

📋 Add a column `E` for "Is Expensive?"

> If price is more than 2, show **"Yes"**, else **"No"**

🔧 Formula in E2:

```excel

=IF(B2>2, "Yes", "No")
=IF(ISBLANK(A7), "Blank", "Not Blank")
=IF(AND(A1>10, A3="Yes"), "Valid", "Invalid")
=IF(A3="Yes", "Confirmed", "Pending")
=IF(A1>90, "A", IF(A1>80, "B", IF(A1>70, "C", "Fail")))
```

------

### ✅ **3. Use `SUM`, `AVERAGE`, `MAX`, `MIN`**

Below your table (Row 6), calculate:

- Total quantity: `=SUM(C2:C4)`
- Average price: `=AVERAGE(B2:B4)`
- Max price: `=MAX(B2:B4)`
- Min quantity: `=MIN(C2:C4)`

------

### ✅ **4. Use `LOOKUP()`**

Search for a product name and return its price.

📋 Example:



| G      | H                   |
| ------ | ------------------- |
| Search | Banana              |
| Price  | (your formula here) |

🔧 Formula in H2:

```excel

=VLOOKUP(H1, A2:C4, 2, FALSE)
```

------

### ✅ **5. Use `COUNTIF()`**

Count how many products have quantity more than 3.

```excel

=COUNTIF(C2:C4, ">3")
```

------

### ✅ **6. Use `INDEX` + `MATCH`**

Get the quantity of “Orange”:

```excel
=INDEX(C2:C4, MATCH("Orange", A2:A4, 0))
```

------

## ⭐ Bonus Challenge:

Build a small invoice system:

- Enter item names, prices, and quantities
- Use formulas to:
  - Calculate totals
  - Apply tax (`Total * 1.09`)
  - Apply discount if total > 100