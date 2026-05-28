# 🤖 Telegram Bot — Telegraf + Vercel

Bot Telegram dengan fitur auto-reply, forward ke admin, dan inline keyboard.

---

## 📁 Struktur Folder

```
telegram-bot/
├── api/
│   └── webhook.js      ← Kode utama bot
├── .env.example        ← Contoh file env
├── .gitignore
├── package.json
├── vercel.json
└── README.md
```

---

## 🚀 Cara Deploy ke Vercel

### 1. Upload ke GitHub
- Buat repo baru di GitHub
- Upload semua file ini (jangan upload `.env`!)

### 2. Import ke Vercel
- Buka [vercel.com](https://vercel.com) → **Add New Project**
- Pilih repo GitHub kamu → klik **Deploy**

### 3. Set Environment Variables di Vercel
Buka **Project Settings → Environment Variables**, tambahkan:

| Key        | Value                        |
|------------|------------------------------|
| `BOT_TOKEN` | Token bot dari @BotFather   |
| `ADMIN_ID`  | ID Telegram admin           |

### 4. Set Webhook Telegram
Setelah deploy, buka URL ini di browser (ganti bagian yang perlu):

```
https://api.telegram.org/bot<BOT_TOKEN>/setWebhook?url=https://<DOMAIN_VERCEL>/api/webhook
```

Contoh:
```
https://api.telegram.org/bot7836434671:AAEV.../setWebhook?url=https://telegram-bot-mu.vercel.app/api/webhook
```

Jika berhasil, muncul pesan:
```json
{"ok":true,"result":true,"description":"Webhook was set"}
```

---

## ✅ Selesai!
Bot kamu sudah aktif dan siap digunakan 🎉
