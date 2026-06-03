<p align="center">
  <img src="https://iili.io/C2nKZan.jpg" width="80" height="80" style="border-radius:50%;border:2px solid #00d4ff;box-shadow:0 0 30px rgba(0,212,255,.3)">
</p>

<h1 align="center">⚡ TechyRender.py</h1>

<p align="center">
  <b>Plug it into your bot. Control it from the web.</b><br>
  One Python file that gives your bot a REST API, live status page, and remote management.
</p>

<p align="center">
  <a href="https://techyrender.page.gd"><img src="https://img.shields.io/badge/Visit-Website-00d4ff?style=for-the-badge"></a>
  <img src="https://img.shields.io/badge/Python-3.8%2B-3776AB?style=flat&logo=python">
  <img src="https://img.shields.io/badge/MongoDB-ready-47A248?style=flat&logo=mongodb">
</p>

---

## 👋 What is This?

**TechyRender.py** is a lightweight Python engine you drop into your bot project. Once running, it:

- Serves a **live status page** at your bot's URL
- Exposes a **REST API** that the TechyRender website talks to
- Keeps your bot **alive** with heartbeat pings
- Auto-**restarts** your bot if it crashes
- Lets you **link your bot** to your TechyRender account for remote control

No frameworks. No complex setup. One file.

---

## ✨ What You Get

| Feature | What it does |
|---------|--------------|
| 🌐 **Live Web UI** | A dark-themed status page at your bot's URL showing name, version, MongoDB status, connection status |
| 🔌 **REST API** | `/getstatus`, `/connectweb`, `/unlink`, `/update` — called by the website automatically |
| ❤️ **Heartbeat** | Pings your bot's URL every N seconds to keep Render from spinning down |
| 🔄 **Auto-Restart** | If your bot script crashes, it restarts automatically in 5 seconds |
| ☁️ **MongoDB Sync** | Persists your bot's state (interval, connection) across restarts |
| 🛑 **Remote Kill** | Website can suspend your bot instantly |
| 🔗 **One-Click Link** | Connect to the TechyRender website with a single click |

---

## 📥 Quick Start

### 1. Install

```bash
pip install requests python-dotenv pymongo cryptography
```

### 2. Place the File

Put `TechyRender.py` in the **same folder** as your bot script.

### 3. Configure

Create a `.env` file in the same folder:

```env
BOT_NAME=MyBot
BOT_DEV=YourName
RENDER_EXTERNAL_URL=https://your-bot.onrender.com
BOT_FILENAME=my_bot.py
```

### 4. Run

```bash
python TechyRender.py
```

That's it. Your bot runs inside TechyRender, and the web UI + API goes live at `http://0.0.0.0:8080`.

---

## ⚙️ Environment Variables

| Variable | Required | Default | What it does |
|----------|----------|---------|--------------|
| `BOT_NAME` | ✅ | — | Your bot's display name on the status page |
| `BOT_DEV` | — | `Unknown` | Your name/credit on the status page |
| `RENDER_EXTERNAL_URL` | ✅ | — | Your bot's public URL (needed for heartbeat + website link) |
| `PORT` | — | `8080` | Port for the web UI |
| `BOT_FILENAME` | ✅ | `Test.py` | Your bot script filename |
| `MONGO_URI` | — | — | MongoDB connection string (enables state sync) |
| `RENDER_SERVICE_NAME` | — | falls back to `BOT_NAME` | Used as the MongoDB document key |

> 💡 On Render.com, `RENDER_EXTERNAL_URL` is set automatically. For other hosts, set it manually.

---

## 🔗 Connecting to the Website

1. Go to **[techyrender.page.gd](https://techyrender.page.gd)** and log in
2. Add your bot using your **Render API key**, **Service ID**, and **Bot URL**
3. Select your bot and click **"Link TR ID"**
4. ✅ Your bot is now linked — control it from the website

Once connected, you can:

- 📊 **View live status** — ping, version, uptime, connection state
- 🔄 **Restart / Suspend / Resume** your Render service
- 📦 **Force deploy** with or without cache
- 🔧 **Edit environment variables** remotely
- ⏱ **Change ping interval** anytime
- 👀 **Watch terminal output** in real time

---

## 🌐 Web UI (Built-in)

When `TechyRender.py` runs, it serves a status page at your bot's URL:

```
https://your-bot.onrender.com  →  TechyRender Status Page
```

The page shows:
- System status (optimization, MongoDB, account link, version)
- Bot info (name, developer)
- A **"View on Website"** button linking to the TechyRender dashboard

---

## 📡 API Endpoints

Your bot automatically gets these endpoints:

| Endpoint | What it's for |
|----------|---------------|
| `GET /getstatus` | Returns bot name, version, ping interval, connection status |
| `GET /connectweb/techyrender?id=XXX` | Links your bot to a TechyRender account |
| `GET /techyrender/unlink?id=XXX` | Disconnects from the website |
| `GET /techyrender/update?id=XXX&interval=N` | Changes the heartbeat ping interval |

These are used by the website — you don't need to call them manually.

---

## ☁️ MongoDB (Optional)

Set `MONGO_URI` in your `.env` to enable persistent state:

```env
MONGO_URI=mongodb+srv://user:pass@cluster.mongodb.net
```

Your bot's ping interval and TechyRender ID are saved to MongoDB, so they survive restarts.

---

## ❓ FAQ

**Q: Do I need the PHP files?**  
No. The website is already hosted. You only need `TechyRender.py`.

**Q: My bot crashed — what happens?**  
TechyRender auto-restarts it after 5 seconds. You'll see a warning in stderr.

**Q: Can I run multiple bots?**  
Yes. Each bot runs its own `TechyRender.py` and connects to the same website.

**Q: How do I stop my bot remotely?**  
Use the **Suspend** button on the website. TechyRender detects the suspension and shuts down.

**Q: Does it work without MongoDB?**  
Yes. State is saved locally to `techyrender_config.json`. MongoDB just adds persistence across servers.

---

<p align="center">
  <sub>Built with ❤️ by</sub><br>
  <strong>@SuryaXCristiano</strong>
</p>

<p align="center">
  <sub>MIT License · Free to use, modify, and share</sub>
</p>
