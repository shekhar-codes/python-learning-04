# 🟢 WhatsApp Classroom – Python Conditional Statements Edition

👩🏫 **Teacher:** *Hey coder kid! Aaj hum "conditions" explore karne ja rahe hain. Ready?*

👧 **You:** *Sir, "condition" ka matlab?*

👩🏫 **Teacher:**  
**Condition** wo logical test hai jo decide karta hai ki program ka agla step chalega ya skip hoga — bilkul tum jaise lunch-box dekh kar decide karte ho ki khana khana hai ya nahi. Python har test ko **True** ya **False** mein badal deta hai. True माने "haan", False माने "nahin" — isse hi **Boolean** kehte hain.  

- Kuch values by default "sachche" hote hain (*truthy*)— jaise non-zero numbers, non-empty strings 📜.  
- Kuch "jhoothe" (*falsy*)— jaise `0`, empty list `[]`, empty string `""`, ya `None`.  

Try in shell:  

```python
bool(5)      # True
bool([])     # False
```

---

## 🪄 Naya Shabd Alert  
- **Boolean:** Do-value system — True ya False.  
- **Truthy/Falsy:** Non-Boolean object jo Boolean test mein True ya False behave kare.  

---

## 👩🏫 Teacher: Ab chalo **if** ko pakdo.

### 🌟 "if" – Sabse pehli chowki

```
if condition:
    # magic block
```

Agar *condition* True ho, andar wali indented lines chalti hain. Indentation matlab space se tab tak ka group banana— Python brackets ki jagah space se samajhta hai.  

Childish example:  

```python
chocolates = 3
if chocolates > 0:
    print("Yay! I eat chocolate.")
```

Yahaan `>` ek **comparison operator** hai — ye check karta hai ki kaun badi value hai.  

### Practice 1:  
1️⃣ `toys = 0` set karo. `if toys == 0:` print `"Let's buy toys!"`.  

---

## 🟢 "if-else" – Do raaste

Kabhi *condition* False ho sakti. Tab **else** wala block chalta hai.

```python
weather = "rain"
if weather == "sunny":
    print("Play outside")
else:
    print("Read comics indoors")
```

### Practice 2:  
Banayo: agar `age >= 18` ho toh `"vote karo"`, warna `"grow older first"`.

---

## 🟠 "elif" – Zyada raaste

`elif` = "else if" ladder:

```python
score = 85
if score >= 90:
    grade = "A"
elif score >= 80:
    grade = "B"
elif score >= 70:
    grade = "C"
else:
    grade = "D"
```

Har step serially check hota; pehle True milte hi ladder ruk jata.

### Practice 3:  
Traffic‐fine program banao: speed > 120⇒"Big fine", 80–120⇒"Small fine", else "Safe".

---

## 🧬 Nested if – Ghar ke andar ghar

Ek `if` block ke andar doosra `if` likh sakte ho. Dhyaan rahe indentation se pata chalta hai kaun kiska bachcha hai.

```python
if pocket_money > 0:
    if pocket_money > 100:
        print("Buy video game")
    else:
        print("Buy candy")
```

**Tip:** Zyada nesting se code confusing ho sakta; kabhi-kabhi **guard clauses** (`return` ya `continue` early) use karo readability ke liye.

---

## 🔗 Logical operators – **and** / **or** / **not**

- `and` — dono conditions True honi chahiye  
- `or` — koi ek True kaafi  
- `not` — value ko ulta karta  

Operators precedence: `not` > `and` > `or`.  

```python
age = 10
height = 120
if age >= 10 and height >= 110:
    print("Ride roller-coaster")
```

**Short-circuit:** `and` pehla False milte hi ruk jata; `or` pehla True milte hi. Yeh efficiency badhata hai.

### Practice 4:  
`if (coins > 0 and not piggy_bank_full):` likh kar print `"Add coin"`.

---

## ⚡ Ternary Operator – One-line chocobar

Syntax: `value_if_true if condition else value_if_false`.

```python
speed = 70
status = "Fast" if speed > 60 else "Slow"
```

Short but use wisely— readability pe dhyan.

### Practice 5:  
Ek line mein `adult = True if age >= 18 else False`.

---

## 🚦 `match-case` (Python 3.10 +) – Super Switch

Structured **pattern matching** switch-like statement.  

```python
signal = "yellow"
match signal:
    case "red":
        action = "STOP"
    case "yellow":
        action = "SLOW"
    case "green":
        action = "GO"
    case _:
        action = "UNKNOWN"
```

Specials: `case _` wildcard matches anything. Tuples, guards (`if`), and type-patterns bhi possible.

### Practice 6:  
`match` use karke dice value (1-6) se "snake eyes", "lucky six", ya "plain roll" label karo.

---

## 🪁 Comprehensions with conditions

List comprehension me trailing `if` filter karta hai; embedded `if-else` value set karta hai.

```python
nums = [1,2,3,4]
even_squares = [n*n for n in nums if n%2==0]        # filter
labels = ["even" if n%2==0 else "odd" for n in nums] # value choice
```

### Practice 7:  
`names` list se sirf woh names lo jinme `"a"` ho aur uppercase karo.

---

## 💡 Best Practices Recap

1. **Indentation** = 4 spaces; no tabs mix.  
2. Keep ladders max 3-4 levels; use guard returns.  
3. Prefer `match-case` for many discrete patterns for clarity.  
4. Use ternary only when expression simple.  
5. Remember truthy/falsy surprises like empty list, `0.0`, empty dict.

---

## 🏋️‍♀️ Grand Practice Set

1. Writing Prompt Generator: User type likhne pe if/elif decide kare "poem", "story", "joke".  
2. ATM cash withdrawal rules: balance check, min ₹100, else denial.  
3. Rock-Paper-Scissors with `match-case` deciding winner.  
4. Temperature converter menu: if choice == 1 Celsius→F, 2 F→C else error.  
5. Secret-Santa filter: comprehension se sirf unhi friends ko pick karo jinme first letter vowel.

---

## 📍 Quick Glossary

| Word | Baccha Friendly Matlab |
|---|---|
| **Condition** | Sawal jo program poochta |
| **Boolean** | Sirf True ya False ki duniya |
| **Truthy/Falsy** | Sachche/Jhoothe values |
| **Indentation** | Space se banne wali gully jisse Python blocks samajhta |
| **Short-circuit** | Jaldi decision; poori line nahi padhta |
| **Pattern Matching** | `match-case` ka gyaan; values ko patterns se jodna |

---

## 🎯 Additional Deep Concepts

### Comparison Operators Detail

```python
# Equality and Inequality
x == y    # Equal to
x != y    # Not equal to

# Relational Operators  
x > y     # Greater than
x < y     # Less than
x >= y    # Greater than or equal to
x <= y    # Less than or equal to

# Identity Operators
x is y        # Same object in memory
x is not y    # Different objects

# Membership Operators
x in y        # x exists in y
x not in y    # x doesn't exist in y
```

### Advanced Boolean Logic

```python
# Complex conditions
if (age >= 18 and citizenship == "Indian") or (age >= 21 and citizenship == "Foreign"):
    print("Can vote")

# Using parentheses for clarity
if ((income > 500000) and (not tax_paid)) or (audit_required):
    print("Tax notice")
```

### Error Handling with Conditions

```python
# Safe division
if denominator != 0:
    result = numerator / denominator
else:
    result = "Cannot divide by zero"

# Checking if variable exists
if 'variable_name' in locals():
    print("Variable exists")
```

### Real-world Examples

#### Bank ATM System
```python
balance = 5000
pin = 1234
entered_pin = int(input("Enter PIN: "))
amount = int(input("Enter amount: "))

if entered_pin != pin:
    print("Wrong PIN")
elif amount > balance:
    print("Insufficient funds")
elif amount <= 0:
    print("Invalid amount")
elif amount % 100 != 0:
    print("Amount should be multiple of 100")
else:
    balance -= amount
    print(f"Transaction successful! Balance: {balance}")
```

#### Grade Calculator
```python
marks = int(input("Enter marks: "))

if marks < 0 or marks > 100:
    print("Invalid marks")
elif marks >= 90:
    grade = "A+"
    print("Excellent!")
elif marks >= 80:
    grade = "A"
    print("Very Good!")
elif marks >= 70:
    grade = "B"
    print("Good!")
elif marks >= 60:
    grade = "C"
    print("Satisfactory")
elif marks >= 50:
    grade = "D"
    print("Pass")
else:
    grade = "F"
    print("Fail")
```

---

👩🏫 **Teacher:** *Bas itna gyaan! Ab laptop kholo, code likho, aur agar doubt aaye toh ping maaro. Happy coding!* 🤗

---

## 📚 Complete Reference

Ye complete guide hai Python Conditional Statements ka. Har concept ko example ke saath explain kiya gaya hai. Practice questions solve karo aur coding skills improve karo!

**Created with ❤️ for Python learners**