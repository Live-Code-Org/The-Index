# The Index

## לולאות (Loops – for / while)

> מנגנון שמריץ קטע קוד שוב ושוב – כדי שלא נצטרך לכתוב את אותה שורה מאה פעמים, ונוכל לעבד אוסף נתונים בצורה אוטומטית.

### 🎭 אפשרויות לאנלוגיה (לבחירה ידנית)

* **אפשרות א' (מכונת דפוס vs. חיישן אור):**
  * `for` = מכונת דפוס: אתה אומר "תוציאי 1,000 עותקים". המספר ידוע מראש, המכונה סופרת ועוצרת.
  * `while` = חיישן אור במרפסת: לא יודע כמה זמן יעבוד. רץ כל עוד חשוך. ברגע שהשמש זורחת – עוצר.
* **אפשרות ב' (עגלת קניות):** יש לך 50 פריטים בסל. `for` עובר על כולם אחד-אחד ומחשב מחיר. `while` יעצור את הקנייה כל עוד סך החשבון לא עבר את תקציב שנקבע.

### 💻 קוד תמציתי (Python)

```python
fruits = ["Apple", "Banana", "Mango"]

# for loop: known number of iterations – goes through each item
for fruit in fruits:
    print(f"Processing: {fruit}")  # Runs 3 times, once per item

# while loop: condition-based – runs as long as something is True
stock = 5
while stock > 0:
    print(f"Items left: {stock}")
    stock -= 1  # Decrease by 1 each iteration

# break: exit the loop immediately
for fruit in fruits:
    if fruit == "Banana":
        break               # Stops the entire loop
    print(fruit)            # Only prints Apple

# continue: skip this iteration, move to the next
for fruit in fruits:
    if fruit == "Banana":
        continue            # Skips Banana only
    print(fruit)            # Prints Apple and Mango
```

> **לשים לב:** `for` ו-`while` ניתנים לקינון (לולאה בתוך לולאה). זה שימושי מאוד – למשל, לעבור על כל שורות ועמודות של טבלה. רק חשוב לשמור על ההזחה (indent) כדי שפייתון יבין מה בתוך מה.

### 🛠️ יישום בפרויקט

בבניית **חנות אונליין**: `for` עובר על כל מוצרי הקטלוג ומציג אותם בדף. `while` שומר את עגלת הקניות פתוחה כל עוד המשתמש לא לחץ "סיום קנייה".

---

*· The Index by LiveCode*
