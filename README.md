````markdown
# Arithmetic Formatter

A Python project that vertically arranges arithmetic problems (addition and subtraction only) side-by-side, optionally showing the answers.

## 📋 Description

This project mimics how elementary students solve arithmetic problems on paper. It accepts a list of arithmetic problems and returns them formatted vertically and aligned properly. Optionally, the answers can be included.

## ✅ Features

- Accepts up to 5 problems
- Only supports `+` and `-` operators
- Validates operands (only digits, max 4 digits)
- Formats problems in vertical layout
- Optional: Displays results

---

## 🛠️ Requirements

- Python 3.x

No additional libraries are needed.

---

## 🚀 How to Run

Clone the repo or copy the script into your environment. Run using Python:

```bash
python arithmetic_formatter.py
```

---

## 📦 Example Usage

```python
from arithmetic_formatter import arithmetic_arranger

print(arithmetic_arranger(["32 + 698", "3801 - 2", "45 + 43", "123 + 49"]))
```

**Output:**

```
   32      3801      45      123
+ 698    -    2    + 43    +  49
-----    ------    ----    -----
```

With answers:

```python
print(arithmetic_arranger(["32 + 8", "1 - 3801", "9999 + 9999", "523 - 49"], True))
```

**Output:**

```
  32         1      9999      523
+  8    - 3801    + 9999    -  49
----    ------    ------    -----
  40     -3800     19998      474
```

---

## ❌ Error Handling

The function returns meaningful errors in the following cases:

| Condition                    | Error Message                                     |
| ---------------------------- | ------------------------------------------------- |
| More than 5 problems         | `Error: Too many problems.`                       |
| Invalid operator             | `Error: Operator must be '+' or '-'.`             |
| Non-digit characters         | `Error: Numbers must only contain digits.`        |
| Operand longer than 4 digits | `Error: Numbers cannot be more than four digits.` |

---

## 🧪 Sample Tests

```python
assert arithmetic_arranger(["3 / 855"]) == "Error: Operator must be '+' or '-'."
assert arithmetic_arranger(["24 + 85215"]) == "Error: Numbers cannot be more than four digits."
assert arithmetic_arranger(["98 + 3g5"]) == "Error: Numbers must only contain digits."
assert arithmetic_arranger(["44 + 815", "909 - 2", "45 + 43", "123 + 49", "888 + 40", "653 + 87"]) == "Error: Too many problems."
```

---

## 📁 File Structure

```
arithmetic_formatter/
├── arithmetic_formatter.py
├── README.md
```

---

## 🧑‍💻 Author

Jordan Leturgez
Fort Wayne, IN
Certified in Python, Copywriter, Data Analysis, and more.

---

## 📄 License

This project is open source and free to use.

```

