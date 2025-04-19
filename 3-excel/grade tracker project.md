# ✅ Project: **Student Grade Tracker with Smart Highlights**

🎯 Here's a practical **Excel project** focused on **Conditional Formatting with Formulas** — one of the most powerful tools in Excel for visualizing data dynamically.

------

## 

### 📌 Goal:

Track students' scores and highlight:

- ✅ Passed students (green)
- ❌ Failed students (red)
- 🟡 Borderline students (yellow)
- 🔄 Missing scores (gray or warning)

------

## 🧱 Step 1: Set Up Your Table



| Name   | Assignment | Midterm | Final | Average | Status |
| ------ | ---------- | ------- | ----- | ------- | ------ |
| John   | 85         | 78      | 90    |         |        |
| Sarah  | 40         | 60      |       |         |        |
| Ali    | 70         | 72      | 75    |         |        |
| Lila   | 55         | 59      | 60    |         |        |
| Daniel | 30         | 20      | 35    |         |        |

------

## 🧮 Step 2: Add Formulas

### 💡 Calculate average:

In the **Average** column (E2):

```
=AVERAGE(B2:D2)
```

Copy down for all students.

### 🧮 Determine Pass/Fail Status:

In the **Status** column (F2):

```
=IF(COUNTA(B2:D2)<3, "Incomplete", IF(E2>=60, "Pass", IF(E2>=50, "Borderline", "Fail")))
```

------

## 🎨 Step 3: Apply Conditional Formatting

### ✅ Highlight Passed Students (Green):

1. Select the whole row (e.g., `A2:F6`)
2. Go to **Home → Conditional Formatting → New Rule**
3. Choose **“Use a formula to determine which cells to format”**
4. Use:

```
=$F2="Pass"
```

1. Set Fill color to green

------

### ❌ Highlight Failed Students (Red):

Same steps, formula:

```
=$F2="Fail"
```

Color: Red fill, white bold text

------

### 🟡 Highlight Borderline (Yellow):

Formula:

```
=$F2="Borderline"
```

------

### ⚠️ Highlight Missing Scores:

Let’s gray out rows with missing grades: Formula:

```
=COUNTA(B2:D2)<3
```

Format: Light gray fill, italic text

------

## 🧪 Bonus Challenges (Optional):

- Add icon sets (✅ ❌ ⚠️) in the **Status** column
- Create a dropdown for grading status using **Data Validation**
- Make the grading scale adjustable with named ranges (e.g. `_passMark`, `_borderlineMark`)