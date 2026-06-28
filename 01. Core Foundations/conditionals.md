# The Index

## תנאים (Conditionals – if / elif / else)

> צומת החלטה בקוד: המחשב בודק אם תנאי מסוים מתקיים, ולפי התשובה בוחר באיזה נתיב להמשיך.

### 🎭 אפשרויות לאנלוגיה (לבחירה ידנית)

* **אפשרות א' (כניסה למועדון):** המאבטח (הקוד) בודק: "האם יש לך כרטיס? האם אתה מעל גיל 18?" – אם שניהם `True`, אתה נכנס. יש לך VIP? נכנס גם בלי תור. בכל מקרה אחר (`else`) – נשאר בחוץ.
* **אפשרות ב' (מזג האוויר בבוקר):** אתה מסתכל בחוץ: "האם גשום?" – מביא מטריה. "האם חם?" – לובש חולצה קצרה. "בסדר?" – לובש ג'קט קל. כל יום, אותה רשימת תנאים, תשובות שונות.

### 💻 קוד תמציתי (Python)

```python
age        = 20
has_ticket = True
is_vip     = False

if age >= 18 and has_ticket:   # Both conditions must be True
    print("Welcome in!")
elif is_vip:                   # If the first block was False, check this
    print("VIP entrance!")
else:                          # If nothing above matched
    print("Sorry, not tonight.")

# Shorthand: ternary expression (one-liner for simple conditions)
status = "Adult" if age >= 18 else "Minor"
print(status)                  # Adult
```

> **לשים לב:** `elif` הוא קיצור של "else if". אפשר לשרשר כמה `elif` שרוצים – פייתון יבדוק אותם אחד אחרי השני ויבצע רק את הראשון שיתקיים.

### 🛠️ יישום בפרויקט

בבניית **מערכת Login**: אם האימייל והסיסמה תואמים – מעביר את המשתמש לדשבורד. אם הסיסמה שגויה – מציג "נסה שוב". אם המייל לא קיים – מציג "האם תרצה להירשם?". כל תרחיש מטופל בנתיב נפרד.

---

*· The Index by LiveCode*
