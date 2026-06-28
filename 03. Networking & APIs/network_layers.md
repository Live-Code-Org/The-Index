# The Index

## 5 השכבות ברשת (Network Layers / TCP-IP Model)

> מודל ארכיטקטוני שמחלק את תהליך התקשורת ברשת ל-5 שכבות נפרדות, כאשר כל שכבה מטפלת בהיבט אחד של העברת המידע ומסתמכת על השכבה שמתחתיה.

### 🎭 אפשרויות לאנלוגיה (לבחירה ידנית)

* **אפשרות א' (שליחת חבילה בדואר):** כשאתם שולחים חבילה: אתם כותבים את התוכן (שכבת אפליקציה), שמים במעטפה עם כתובת (שכבת תעבורה), הדוור בוחר את המסלול (שכבת רשת), הורכבת הולכת לרכב הנכון (שכבת קישור), והרכב נוסע פיזית בכביש (שכבה פיזית). כל שלב אחראי לחלקו בלבד.
* **אפשרות ב' (בניית בניין):** יסודות (שכבה פיזית) → שלד בטון (קישור) → צינורות וחשמל (רשת ותעבורה) → הדירה המרוהטת שבה אנחנו גרים ומשתמשים (אפליקציה). כל שכבה בנויה על זו שמתחתיה.

### 💻 קוד תמציתי (Python)

```python
import urllib.request

# As developers, we work only at the APPLICATION layer (layer 5)
# Python + the OS handle all the layers below automatically

url      = "https://api.livecode.org/ping"
response = urllib.request.urlopen(url)

# We send a request and get data back.
# Behind the scenes: DNS → IP routing → TCP handshake → HTTPS encryption
# We don't manage any of that manually – the stack handles it.
data = response.read().decode("utf-8")
print(data)
```

> **לשים לב:** כמפתחי אפליקציות אנחנו עובדים כמעט תמיד בשכבה ה-5 בלבד (האפליקציה). הבנת השכבות התחתונות מאוד שימושית לדיאגנוסטיקה: כשיש בעיית חיבור, היא יכולה להיות בשכבה 1 (כבל נותק), 3 (IP לא נגיש) או 4 (TCP timeout).

### 🛠️ יישום בפרויקט

בפיתוח שרתים ו-APIs: כל שיחה שאנחנו עושים ל-API עוברת אוטומטית דרך כל 5 השכבות – גם אם אנחנו רואים רק את ה-`response.json()` בסוף. הבנת המודל עוזרת לנו להסביר מדוע בקשה מסוימת נכשלת.

---

*· The Index by LiveCode*
