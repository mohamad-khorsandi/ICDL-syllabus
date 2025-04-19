💪 Here’s a fresh set of **math-focused Excel exercises**, designed to help you practice Excel as a **math tool** — useful for students, finance, engineering, and general problem-solving.

------

## 📘 **Math-Based Excel Exercises**

------

### 🔢 **1. Percentage Calculations**

📋 Data:



| A       | B      | C          |
| ------- | ------ | ---------- |
| Product | Price  | Discount % |
| Shirt   | 50000  | 10%        |
| Pants   | 80000  | 15%        |
| Jacket  | 120000 | 20%        |

🔧 **Tasks:**

- Calculate **discount amount**: `=B2*C2`
- Calculate **final price**: `=B2 - (B2*C2)`

------

### 📈 **2. Compound Interest**

📋 Given:



| A                | B      |
| ---------------- | ------ |
| Principal (P)    | 100000 |
| Rate (R, yearly) | 5%     |
| Time (T, years)  | 3      |

🔧 Calculate:

- Compound Interest:

  ```
  
  =B1 * (1 + B2)^B3
  ```

------

### 🧮 **3. Quadratic Formula Solver**

Equation: `ax² + bx + c = 0`

📋 Data:



| A    | B    |
| ---- | ---- |
| a    | 1    |
| b    | -5   |
| c    | 6    |

🔧 Roots:

```
=(-B2 + SQRT(B2^2 - 4*B1*B3)) / (2*B1)
=(-B2 - SQRT(B2^2 - 4*B1*B3)) / (2*B1)
```

------

### 🎲 **4. Random Numbers**

📋 Tasks:

- Generate 10 random numbers between 1 and 100:

```

=RANDBETWEEN(1, 100)
```

- Calculate their average, max, and min

------

### 📊 **5. Calculate Standard Deviation & Variance**

📋 Sample Data: `85, 90, 78, 88, 92`

🔧 Paste into `A1:A5`
 Then use:

```
=STDEV.S(A1:A5)
=VAR.S(A1:A5)
```

------

### ➗ **6. Rounding Exercises**

📋 Try:

```
=ROUND(3.14159, 2)
=ROUNDUP(2.3, 0)
=ROUNDDOWN(2.9, 0)
=INT(5.7)
```

------

### ⏱️ **7. Time Math**



| A     | B     |
| ----- | ----- |
| Start | 08:30 |
| End   | 12:45 |

🔧 Calculate duration:

```

=B2 - A2
```

Then format the result as **Time** (`hh:mm`)

------

### 🧩 **8. Array Math (Bonus)**



| A    | B    | C    |
| ---- | ---- | ---- |
| 2    | 3    | 4    |
| 5    | 6    | 7    |

🔧 Multiply each element in A1:C2 by 2 (use formula in D1, then autofill):

```

=A1*2
```