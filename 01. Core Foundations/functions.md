# The Index

## פונקציות (Functions)

> בלוק קוד שמקובץ תחת שם, מקבל קלט (פרמטרים), מבצע פעולה ומחזיר תוצאה. מגדירים פעם אחת – קוראים לו כמה פעמים שרוצים.

### 🎭 אפשרויות לאנלוגיה (לבחירה ידנית)

* **אפשרות א' (בלנדר):** אתה לא בונה בלנדר מחדש בכל פעם שבא לך שייק. הבלנדר הוא מנגנון קבוע. זורקים פנימה פירות (קלט), לוחצים כפתור (קריאה לפונקציה), ומקבלים שייק (פלט).
* **אפשרות ב' (מתכון):** אתם כותבים מתכון לעוגת שוקולד פעם אחת – ואז כל פעם שרוצים עוגה, פשוט עוקבים אחריו. יכולים להכין עוגה לכל אחד בלי להמציא את ההוראות מחדש.

### 💻 קוד תמציתי (Python)

```python
def make_shake(fruit, size="medium"):  # "size" has a default value
    result = f"{fruit} Shake ({size})"
    return result                       # Returns the output

my_drink   = make_shake("Banana")         # Uses default size
your_drink = make_shake("Mango", "large") # Overrides the default

print(my_drink)    # Banana Shake (medium)
print(your_drink)  # Mango Shake (large)

# Functions can also return multiple values
def calculate_tax(price):
    tax    = price * 0.17
    total  = price + tax
    return total, tax   # Returns a tuple

final, vat = calculate_tax(100)
print(f"Total: {final}, VAT: {vat}")  # Total: 117.0, VAT: 17.0
```

> **לשים לב:** פונקציה שמחזירה ערך צריכה `return`. פונקציה שרק *עושה* משהו (כמו הדפסה) לא חייבת. אם לא תכתבו `return`, הפונקציה תחזיר `None` בשקט – וזה בסדר גמור כשרוצים פעולה ולא תוצאה.

### 🛠️ יישום בפרויקט

בבניית **חנות אונליין**: במקום לחשב מע"מ בכל מקום בנפרד, כותבים פונקציה `calculate_tax(price)` אחת. בכל פעם שצריך – קוראים לה. רוצים לשנות את אחוז המע"מ? משנים במקום אחד, ומשפיעים על כל הקוד.

---

*· The Index by LiveCode*
