# The Index

## UDP (User Datagram Protocol)

> פרוטוקול תקשורת מהיר שמשגר חבילות מידע ישירות ליעד – ללא חיבור מוקדם וללא בדיקה אם הגיעו. המהירות חשובה יותר מהשלמות.

### 🎭 אפשרויות לאנלוגיה (לבחירה ידנית)

* **אפשרות א' (שידור רדיו חי):** תחנת הרדיו פולטת גלים לכל כיוון – לא יודעת מי מקשיב ולא מחכה לאישור. אם מישהו נכנס לרכב באמצע שיר, הוא שמע רק חצי. זה בסדר – השידור לא יתחיל מחדש בשבילו.
* **אפשרות ב' (פיצוץ פלייריים מהאוויר):** מטוס קטן מטיל אלף פלייריים. לא אכפת לו מי תפס, מי לא. מי שתפס – יש לו. מי שלא – חסר. המסר הגיע ממילא לרוב.

### 💻 קוד תמציתי (Python)

```python
import socket

HOST = "127.0.0.1"
PORT = 5005

# UDP: fire and forget – no connection established, no delivery guarantee
with socket.socket(socket.AF_INET, socket.SOCK_DGRAM) as s:
    message = b"Player moved to position (42, 17)"
    s.sendto(message, (HOST, PORT))  # Sent immediately, no handshake needed
    # If the packet is lost – we don't retry. The next position update will arrive soon.
    print("Position update sent")
```

> **לשים לב:** UDP לא "גרוע" – הוא *מתאים* למקרים שבהם עדיף לאבד מידע ישן ולהמשיך קדימה, מאשר לחכות. בסטרימינג של וידאו, עדיף לפסוח על פריים אחד מאשר לקפוא שנייה שלמה.

### 🛠️ יישום בפרויקט

משחקי מרובי משתתפים (Multiplayer), שיחות קוליות ווידאו (Zoom, WhatsApp), סטרימינג חי – כולם משתמשים ב-UDP. כשהתמונה ב-Zoom מתפשרת לרגע ומתאוששת – זה UDP בפעולה.

---

*· The Index by LiveCode*
