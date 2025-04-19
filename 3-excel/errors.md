##  All Excel Error Types (with Examples)

------

### 1. `#DIV/0!` – **Division by Zero**

📌 **Meaning:** You tried to divide by 0 or a blank cell.

🧪 **Example:**

```

=10/0
```

💡 **Fix:** Make sure the denominator is not 0 or blank.

------

### 2. `#VALUE!` – **Wrong Data Type**

📌 **Meaning:** A function got the wrong type of value (like text instead of a number).

🧪 **Example:**

```

="apple" + 5
```

💡 **Fix:** Ensure all inputs are the right type (e.g., numbers with numbers).

------

### 3. `#NAME?` – **Unrecognized Text or Function**

📌 **Meaning:** Excel doesn't recognize something, like a misspelled function or undefined name.

🧪 **Example:**

```

=SUME(A1:A3)  ← typo
```

💡 **Fix:** Check your spelling or if you're referencing a defined name that doesn't exist.

------

### 4. `#REF!` – **Invalid Cell Reference**

📌 **Meaning:** You deleted a cell or range that a formula depends on.

🧪 **Example:**

- Type `=A1 + B1`
- Then delete **column B**

💡 **Fix:** Update the formula with a valid reference.

------

### 5. `#N/A` – **Value Not Available**

📌 **Meaning:** The value you're looking for isn’t found (common in lookups).

🧪 **Example:**

```

=VLOOKUP("pear", A1:B3, 2, FALSE)
```

(If "pear" doesn't exist)

💡 **Fix:** Ensure the lookup value exists in the range.

------

### 6. `#NUM!` – **Invalid Number**

📌 **Meaning:** A number is too large/small or math is invalid (like square root of a negative).

🧪 **Example:**

```

=SQRT(-1)
```

💡 **Fix:** Check if the calculation makes mathematical sense.

------

### 7. `#NULL!` – **Incorrect Range Intersect**

📌 **Meaning:** You used a space (intersection operator) between ranges that don’t intersect.

🧪 **Example:**

```

=SUM(A1:A2 C1:C2)
```

💡 **Fix:** Use correct separators like `,` or `:` unless you really mean to intersect two ranges.

------

### 8. `#SPILL!` – **Spill Error (New Excel)**

📌 **Meaning:** Excel tried to return multiple values (spill) but couldn’t due to something blocking the space.

🧪 **Example:**

```

=SEQUENCE(5)
```

(but there’s something in the cells below it)

💡 **Fix:** Clear the range where the formula wants to spill.

------

### 9. `#CALC!` – **Calculation Error (Dynamic Arrays)**

📌 **Meaning:** Excel's formula engine can’t resolve the calculation.

🧪 **Example:** Happens sometimes in complex `LET()` or `LAMBDA()` functions.

💡 **Fix:** Double-check your logic and variables.

------

### 10. `#FIELD!` – **Structured Reference Issue (Excel Tables)**

📌 **Meaning:** You tried to reference a field that doesn’t exist in a structured table.

🧪 **Example:**

```

=Table1[WrongField]
```

💡 **Fix:** Use the correct column name from the table.