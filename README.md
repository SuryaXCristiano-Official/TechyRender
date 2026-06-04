<p align="center">
  <img src="https://iili.io/C2nKZan.jpg" width="80" height="80" style="border-radius:50%;border:2px solid #00d4ff;box-shadow:0 0 30px rgba(0,212,255,.3)">
</p>

<h1 align="center">⚡ TechyRender</h1>

<p align="center">
  <b>Plug it into your bot. Control it from the web.</b><br>
  One Python file that give your render hosted bots a REST API, live status page, and remote management directly from the web. No complex setup, no cron-job/uptime-monitor, manage everything from one place !!!
</p>


---

## 🌐 Introduction to TechyRender

**TechyRender** is a lightweight Python engine you drop into your bot projects. Once running, it:

- Serves a **live status page** at your bot's URL
- Exposes a **REST API** that the TechyRender website talks to
- Keeps your bot **alive** with heartbeat pings
- Auto-**restarts** your bot if it crashes
- Lets you **link your bot** to your TechyRender account and control all render functions 


---

## ✨ What You Get

| Feature | What it does |
|---------|--------------|
| 🌐 **Live Web UI** | A dark-themed status page at your bot's URL showing all the necessary infos |
| 🔌 **REST API** | `/getstatus`, `/connectweb`, `/unlink`, `/update` — called by the website automatically |
| ❤️ **Heartbeat** | Pings your bot's URL every 60 seconds (default/changeable) and keep Render from spinning down |
| 🔄 **Auto-Restart** | If your bot script crashes, it restarts automatically in 5 seconds |
| ☁️ **MongoDB Sync** | Persists your bot's state (interval, connection) across restarts |
| 🛑 **Full Control** | Fully control all render actions through the website, via Render's Official API |
| 🔗 **One-Click Link** | Connect to the TechyRender website with a single click |

---

## 📥 Quick Setup Tutorial

### 🔌 Adding TechyRender in your Projects
1. Download the **[TechyRender.zip](https://github.com/SuryaXCristiano-Official/TechyRender/releases/download/Zip/TechyRender.zip)** and extract it. You will find 3 files there - `TechyRender.py`, `requirements.txt`, `.env` and a Setup Guide.
2. Place the `TechyRender.py` in your github bot repo folder
3. Also add `requirements.txt` on the same folder 
4. Add .env on the repo, or add them later as render secret variables
5. Repo setup is done ✅ 

### 🧩 Setup Render Environment
1. Go to render.com , create new web service. 
2. Select your github repo, select hosting plan 
3. Keep everything default, but **you must add this as the start command**
```bash
python TechyRender.py
```
4. If your main bot logic is fine, your bot will be live ✅

---

## 🔗 Connecting to the Website

1. Go to **[TechyRender Website](https://techyrender.page.gd)** and signup/login
2. Click **"+ ADD BOT"** and enter:
   - Your **Render API Key** 
   - Your **Render Service ID** 
   - Your bot's **Public URL**
3. The bot will be added successfully 
4. Select your bot from the list
5. Click **"Link TR ID"**
6. ✅ Done — you can now control your bot from the dashboard
7. You can add as many bots as you want, control them all from one place.

---

## 📥 Additional Guides

### ⬛ Setting up MondoDB

For a detailed guide on **MondoDB** setup please visit **[here](https://techyrender.page.gd/Mongodb)**

### 📝 Api Docs

**[TechyRender API Docs](https://techyrender.page.gd/ApiDocs)**
**[Render API Docs](https://api-docs.render.com/reference/introduction)**
---

### 🔴 Legal Notice ( Important ) 

𝗧𝗵𝗶𝘀 𝗣𝗿𝗼𝗷𝗲𝗰𝘁 𝗶𝘀 𝗺𝗮𝗱𝗲 𝗳𝗼𝗿 𝗲𝗱𝘂𝗰𝗮𝘁𝗶𝗼𝗻𝗮𝗹 𝗽𝘂𝗿𝗽𝗼𝘀𝗲𝘀, 𝗯𝘂𝘁 𝗻𝗼𝘁𝗵𝗶𝗻𝗴 𝘂𝗻𝗲𝘁𝗵𝗶𝗰𝗮𝗹 𝗶𝘀 𝘂𝘀𝗲𝗱 𝗵𝗲𝗿𝗲. 𝗔𝗹𝗹 𝘁𝗵𝗲 𝗔𝗣𝗜 𝗳𝗲𝗮𝘁𝘂𝗿𝗲𝘀 𝗮𝗿𝗲 𝗮𝗹𝗿𝗲𝗱𝘆 𝗶𝗻 𝗥𝗲𝗻𝗱𝗲𝗿'𝘀 𝗔𝗣𝗜 𝗱𝗼𝗰𝘀. 𝗧𝗵𝗲 𝗢𝗻𝗹𝘆 𝗚𝗼𝗮𝗹 𝗼𝗳 𝘁𝗵𝗶𝘀 𝗣𝗿𝗼𝗷𝗲𝗰𝘁 𝗶𝘀 𝘁𝗼 𝗵𝗲𝗹𝗽 𝗽𝗲𝗼𝗽𝗹𝗲 𝗺𝗮𝗻𝗮𝗴𝗲 𝘁𝗵𝗲𝗶𝗿 𝗽𝗿𝗼𝗷𝗲𝗰𝘁𝘀 𝗲𝗮𝘀𝗶𝗹𝘆 𝗶𝗻 𝗼𝗻𝗲 𝗽𝗹𝗮𝗰𝗲, 𝗮𝗻𝗱 𝘀𝗽𝗲𝗰𝗶𝗮𝗹𝗹𝘆 𝗳𝗼𝗿 𝘁𝗵𝗼𝘀𝗲 𝘄𝗵𝗼 𝗰𝗮𝗻𝘁 𝗮𝗳𝗳𝗼𝗿𝗱 𝗮 𝗽𝗮𝗶𝗱 𝗽𝗹𝗮𝗻 𝗼𝗳 𝗿𝗲𝗻𝗱𝗲𝗿. 𝗣𝗹𝗲𝗮𝘀𝗲 𝗱𝗼𝗻𝘁 𝗺𝗶𝘀𝘂𝘀𝗲, 𝗼𝗿 𝗠𝗶𝘀𝘂𝗻𝗱𝗲𝗿𝘀𝘁𝗮𝗻𝗱 𝘁𝗵𝗲 𝗰𝗼𝗻𝗰𝗲𝗽𝘁. 𝗧𝗵𝗮𝗻𝗸𝘀 🙏

---

<p align="center">
  <sub>Built with ❤️ by</sub><br>
  <strong>@SuryaXCristiano</strong>
</p>

<p align="center">
  <sub>© 2026 Copyright Reserved @SuryaXCristiano </sub>
</p>
