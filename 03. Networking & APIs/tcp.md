# The Index

## TCP (Transmission Control Protocol)

> פרוטוקול תקשורת שמבסס חיבור מאובטח לפני שליחת נתונים, ומוודא שכל חבילה הגיעה ליעדה בשלמות ובסדר הנכון.

### 🎭 אפשרויות לאנלוגיה (לבחירה ידנית)

* **אפשרות א' (דואר רשום עם אישור מסירה):** שולחים מסמך חשוב. הנמען חייב לחתום שקיבל. אם חלק הלך לאיבוד – שולחים שוב. רק אחרי אישור על *הכל*, הסיפור נגמר. TCP עובד בדיוק ככה: לא עוברים הלאה עד שהמידע הגיע.
* **אפשרות ב' (שיחת קשר צבאית – "עבור"):** "קיבלת פקודה? עבור." "קיבלתי, עבור." שני הצדדים מאשרים כל שלב לפני שממשיכים. אין השמטות. אין השערות.

### 💻 קוד תמציתי (Python)

```python
import socket

HOST = "livecode.org"
PORT = 80

# TCP requires a connection handshake before data is sent
with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.connect((HOST, PORT))              # 3-way handshake: SYN → SYN-ACK → ACK
    s.sendall(b"GET / HTTP/1.0\r\n\r\n") # Send request after connection is confirmed
    data = s.recv(1024)                  # TCP guarantees this data arrived in full

print(f"Received {len(data)} bytes")
```

> **לשים לב:** TCP מעט איטי יותר מ-UDP כי הוא מוודא כל חבילה – אבל לרוב הפיתוח שלנו (אתרים, APIs, בסיסי נתונים) זה בדיוק מה שרוצים: ודאות מלאה שהמידע הגיע.

### 🛠️ יישום בפרויקט

HTTP ו-HTTPS (כלומר כל אתר אינטרנט), בסיסי נתונים, העברת קבצים – כולם רצים על TCP. כשמפתחים שרת ומקבלים timeout, כנראה מדובר בבעיית חיבור ה-TCP.

---

*· The Index by LiveCode*
