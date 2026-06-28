# The Index

## HTTPS (Hypertext Transfer Protocol Secure)

> פרוטוקול גלישה מאובטח שמצפין את כל המידע שעובר בין הדפדפן לשרת, כך שאף צד שלישי לא יכול לקרוא או לשנות אותו בדרך.

### 🎭 אפשרויות לאנלוגיה (לבחירה ידנית)

* **אפשרות א' (רכב משוריין):** שליחת מידע ב-HTTP רגיל דומה להעברת כסף בשקית ניילון שקופה ברחוב הראשי. HTTPS זה כאילו שמתם את הכסף בתוך רכב ברינקס משוריין ונעול – גם אם מישהו יעצור אותו, לא יוכל לפתוח.
* **אפשרות ב' (מכתב בציפן סודי):** אתם ושגריר ידידותי החלטתם מראש על צופן סודי. שולחים מכתב בשוק הפתוח – כולם רואים את הדף, אבל רק השגריר יכול לפענח את הכתב.

### 💻 קוד תמציתי (Python)

```python
import requests

# HTTPS: all data is encrypted via SSL/TLS certificate
response = requests.get("https://api.livecode.org/secure-data")

# You can inspect the security certificate of the connection
cert_info = response.raw.connection.sock.getpeercert() if hasattr(response.raw.connection, 'sock') else "N/A"

print(f"Status:   {response.status_code}")   # 200 = OK
print(f"Protocol: {response.url[:5]}")        # https
print(f"Data is encrypted in transit: True")
```

> **לשים לב:** הדפדפן מציג סמל מנעול בכתובת כשהאתר משתמש ב-HTTPS. כשאתם בונים פרויקט ומעלים לאוויר, חשוב להשיג **SSL Certificate** – רבים מספקי הענן מספקים אותו חינם (Let's Encrypt).

### 🛠️ יישום בפרויקט

כל אתר מודרני שמטפל בפרטי משתמשים, תשלומים, או כל מידע אישי – חייב לעבוד על HTTPS. דפדפנים מסמנים אתרי HTTP כ"לא מאובטח" ואף חוסמים אותם. זה שיקול קריטי בשלב ה-Deploy.

---

*· The Index by LiveCode*
