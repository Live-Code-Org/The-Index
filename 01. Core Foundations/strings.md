# The Index

## מחרוזות טקסט (Strings)

> כל טקסט בקוד – בין שמדובר בשם משתמש, הודעה, כתובת URL או מיילה – מיוצג כ-String: רצף של תווים שנשמר כיחידה אחת.

### 🎭 אפשרויות לאנלוגיה (לבחירה ידנית)

* **אפשרות א' (שרשרת פנינים):** כל פנינה היא תו בודד (אות, ספרה, רווח). String הוא השרשרת השלמה. ניתן לגשת לכל פנינה לפי מיקומה, לחתוך חלק מהשרשרת, או לשלב שרשראות יחד.
* **אפשרות ב' (שלט מתחלף במגרש כדורגל):** כל שלט מציג מחרוזת אחרת ("GOAL!", "Half Time", שם השחקן). זה טקסט שניתן להחליף, לשרשר ולעצב בכל רגע נתון.

### 💻 קוד תמציתי (Python)

```python
name    = "Gal"
message = "Hello, " + name + "!"  # String concatenation (joining)
print(message)                     # Hello, Gal!

greeting = f"Welcome to Live Code, {name}!"  # f-string: cleaner way to embed variables
print(greeting)                               # Welcome to Live Code, Gal!

print(name[0])    # G     – accessing a single character by index
print(name[::-1]) # laG   – reversing the string with slice notation
print(len(name))  # 3     – number of characters in the string
```

> **לשים לב:** `"3"` ו-`3` הם שני דברים שונים לחלוטין – אחד הוא String והשני הוא מספר (int). ניתן לבדוק בקלות עם `type()`: `type("3")` יחזיר `<class 'str'>`.

### 🛠️ יישום בפרויקט

בבניית **מערכת משתמשים**: שם הפרופיל, כתובת המייל, ביוגרפיה – כולם Strings. בכל פעם שמציגים "שלום, גל!" בראש הדף, עושים שרשור של String קבוע + ה-String שהגיע מבסיס הנתונים.

---

*· The Index by LiveCode*
