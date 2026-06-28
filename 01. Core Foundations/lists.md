# The Index

## רשימות (Lists / Arrays)

> מבנה נתונים שמאחסן אוסף של ערכים תחת שם אחד, מסודרים לפי מיקום (אינדקס), שניתן לגשת אליהם, לערוך ולהרחיב.

### 🎭 אפשרויות לאנלוגיה (לבחירה ידנית)

* **אפשרות א' (מגירת סכו"ם):** במקום משתנה לכל מזלג (fork1, fork2...), יש לך מגירה אחת שנקראת "כלים". כל מיקום קבוע: מזלגות בתא הראשון, סכינים בשני. רוצה להוסיף כף? פשוט דוחף אותה פנימה.
* **אפשרות ב' (פס ייצור ממוספר):** דמיינו פס ייצור עם תאים ממוספרים. בכל תא יש מוצר. ניתן לשלוף תא מסוים לפי מספרו, להחליף את התוכן, או לדחוף מוצר חדש לסוף הפס.

### 💻 קוד תמציתי (Python)

```python
shopping_cart = ["Apples", "Milk", "Bread"]  # A list of items

print(shopping_cart[0])   # Apples  – indexing starts at 0
print(shopping_cart[-1])  # Bread   – negative index counts from the end

shopping_cart.append("Eggs")       # Adding an item to the end
shopping_cart.remove("Milk")       # Removing a specific item by value
print(len(shopping_cart))          # 3 – current number of items

for item in shopping_cart:         # Looping through every item
    print(f"- {item}")
```

> **לשים לב:** אינדקסים בפייתון (ובכמעט כל שפה) מתחילים מ-`0`, לא מ-`1`. הפריט הראשון הוא `list[0]`, השני הוא `list[1]` וכן הלאה. זו מוסכמה אוניברסלית שמגיעה מהיסטוריה של שפת C.

### 🛠️ יישום בפרויקט

בבניית **אפליקציית TODO**: הרשימה היא "הזיכרון" של כל המשימות. כל משימה שהמשתמש מוסיף נדחפת לסוף הרשימה (`append`). כשמציגים את המסך – עוברים על כל הרשימה ומציגים כל פריט.

---

*· The Index by LiveCode*
