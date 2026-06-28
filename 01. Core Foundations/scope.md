# The Index

## טווח הכרה (Scope)

> הגבולות שבהם משתנה "נראה" וניתן לגישה בקוד. משתנה שהוגדר בתוך פונקציה קיים רק שם – ומחוצה לה, הוא פשוט לא קיים.

### 🎭 אפשרויות לאנלוגיה (לבחירה ידנית)

* **אפשרות א' (כינוי משפחתי vs. שם רשמי):** הכינוי "צ'וצ'ו" קיים רק בתוך הבית. אם מישהו יצעק "צ'וצ'ו" ברחוב – אף אחד לא יסתובב. אבל השם שלך בתעודת הזהות הוא גלובלי – כולם מכירים אותו, בבנק וגם בבית.
* **אפשרות ב' (חדר ישיבות סגור):** מה שנאמר בחדר הישיבות – נשאר שם. החלטות שהתקבלו בפנים לא "יוצאות" החוצה אוטומטית לשאר הארגון. רק מה שה"מנהל" (הפונקציה) מחליט להוציא – יוצא.

### 💻 קוד תמציתי (Python)

```python
global_name = "Michael"  # Global scope – visible everywhere

def home():
    nickname = "ChooChoo"      # Local scope – only inside this function
    print(global_name)         # Works! Global is accessible from anywhere
    print(nickname)            # Works! We are inside the function

home()

print(global_name)  # Works! Still global
print(nickname)     # NameError: name 'nickname' is not defined
                    # nickname doesn't exist outside the function
```

> **לשים לב:** בפייתון אפשר לקרוא משתנה גלובלי מתוך פונקציה, אבל כדי *לשנות* אותו מבפנים, צריך להצהיר `global variable_name`. בפועל, מומלץ להעביר ערכים דרך פרמטרים ו-`return` – זה קוד ברור ובטוח יותר.

### 🛠️ יישום בפרויקט

בבניית **מערכת תשלומים**: `user_name` יהיה גלובלי (נדרש בכל הדפים), אבל `temporary_discount` יוגדר רק בתוך פונקציית "חישוב מחיר בקופה". ככה חלקים אחרים ב-API לא יכולים לגשת אליו בטעות ולשנות את ההנחה.

---

*· The Index by LiveCode*
