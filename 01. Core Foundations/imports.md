# The Index

## ייבוא ספריות (import)

> הוספת קוד חיצוני – ספריות ומודולים שאחרים כתבו – לתוך הקוד שלנו, כדי שנוכל להשתמש ביכולות שכבר קיימות ולא לכתוב הכל מאפס.

### 🎭 אפשרויות לאנלוגיה (לבחירה ידנית)

* **אפשרות א' (ארגז כלים מוכן):** אתם בונים מדף. לא מייצרים בעצמכם את המקדחה, את הברגים ואת הסרגל – אתם פשוט לוקחים ארגז כלים מוכן מהמחסן ומשתמשים במה שצריך. `import` הוא הדרך לפתוח ארגז כלים שאחרים כבר הכינו.
* **אפשרות ב' (שכירת מומחה):** רוצים מנוע חיפוש? לא בונים גוגל מאפס. אתם "שוכרים" ספריית חיפוש קיימת (`import whoosh`), ומתחברים לכישורים שלה ישירות לתוך הפרויקט.

### 💻 קוד תמציתי (Python)

```python
import math                          # Importing the entire math module
import random                        # For generating random numbers
from datetime import datetime        # Importing only the datetime class

result = math.sqrt(144)              # Using math.sqrt – no need to write the algorithm
print(result)                        # 12.0

lucky_number = random.randint(1, 100)  # Random integer between 1 and 100
print(f"Lucky number: {lucky_number}")

now = datetime.now()
print(f"Current time: {now.strftime('%H:%M')}")  # e.g. 14:35
```

> **לשים לב:** יש הבדל בין `import math` (מייבאים את כל הספרייה) לבין `from math import sqrt` (מייבאים רק פונקציה אחת). כשהספרייה גדולה ואתם צריכים רק חלק ממנה – `from ... import ...` שומר על קוד נקי ויעיל יותר.

### 🛠️ יישום בפרויקט

בכל פרויקט Python: `import requests` לשיחות API, `import os` לעבודה עם קבצים, `import json` לעבודה עם נתוני JSON. ספריות חיצוניות (כמו `flask`, `pandas`, `fastapi`) מותקנות דרך `pip install` ומיובאות בדיוק אותו אופן.

---

*· The Index by LiveCode*
