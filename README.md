<p align="center">
  <img src="https://imghosting.in/host/7i64il" width="80" height="80" style="border-radius:50%;border:2px solid #00d4ff;box-shadow:0 0 30px rgba(0,212,255,.3)">
</p>

<h1 align="center">⚡ TechyRender</h1>

<p align="center">
  <b>Plug it into your bot. Control it from the web.</b><br>
  One Python file that give your render hosted bots a REST API, live status page, and remote management directly from the web. No complex setup, no cron-job/uptime-monitor, manage everything from one place !!!
</p>


---

## <span class="tricon">🌐</span> Introduction to TechyRender

**TechyRender** is a lightweight Python engine you drop into your bot projects. Once running, it:

- Serves a **live status page** at your bot's URL
- Exposes a **REST API** that the TechyRender website talks to
- Keeps your bot **alive** with heartbeat pings
- Auto-**restarts** your bot if it crashes
- Lets you **link your bot** to your TechyRender account and control all render functions 


---

## <span class="tricon">✨</span> What You Get

| Feature | What it does |
|---------|--------------|
| <span class="tbl-icon">🌐</span> **Live Web UI** | A dark-themed status page at your bot's URL showing all the necessary infos |
| <span class="tbl-icon">🔌</span> **REST API** | `/getstatus`, `/connectweb`, `/unlink`, `/update` — called by the website automatically |
| <span class="tbl-icon">❤️</span> **Heartbeat** | Pings your bot's URL every 60 seconds (default/changeable) and keep Render from spinning down |
| <span class="tbl-icon">🔄</span> **Auto-Restart** | If your bot script crashes, it restarts automatically in 5 seconds |
| <span class="tbl-icon">☁️</span> **MongoDB Sync** | Persists your bot's state (interval, connection) across restarts |
| <span class="tbl-icon">🛑</span> **Full Control** | Fully control all render actions through the website, via Render's Official API |
| <span class="tbl-icon">🔗</span> **One-Click Link** | Connect to the TechyRender website with a single click |

---

## <span class="tricon">📥</span> Quick Setup Tutorial

### <span class="tricon">🔌</span> Adding TechyRender in your Projects
1. Download the **[TechyRender.zip](https://github.com/SuryaXCristiano-Official/TechyRender/releases/download/Zip/TechyRender.zip)** and extract it. You will find 3 files there - `TechyRender.py`, `requirements.txt`, `.env` and a Setup Guide.
2. Place the `TechyRender.py` in your github bot repo folder
3. Also add `requirements.txt` on the same folder 
4. Add .env on the repo, or add them later as render secret variables
5. Repo setup is done ✅ 


### <span class="tricon">🧩</span> Setup Render Environment
1. Go to render.com , create new web service. 
2. Select your github repo, select hosting plan 
3. Keep everything default, but **you must add this as the start command**
```bash
python TechyRender.py
```
4. If your main bot logic is fine, your bot will be live ✅


## <span class="tricon">🔗</span> Connecting to the Website

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


## <span class="tricon">⁉️</span> Tamper Warning ( Vital )

**The `TechyRender.py` is a encrypted python file. Please do not change filename, remove or add any code in the file, or else the file won't work. Though the project is free and open source, the file is kept encrypted to prevent misuse / use without credits


---


## <span class="tricon">📥</span> Additional Guides

### <span class="tricon">⬛</span> Setting up MondoDB

For a detailed guide on **MondoDB** setup please visit **[here](https://techyrender.page.gd/Mongodb)**

### <span class="tricon">📝</span> Api Docs

**[TechyRender API Docs](https://techyrender.page.gd/ApiDocs)**

**[Render API Docs](https://api-docs.render.com/reference/introduction)**


---


## <span class="tricon">❗</span> Important Points ( Must Read )

1. You must add the `BOT_FILENAME` as a env variable. If it's not added, TechyRender **can't detect** your main bot file. 
2. The TechyRender.py is optimized to support all type of telegram bot methods, and supports both `Polling` & `Webhook`.
3. To use Mongodb, you must add `MONGO_URI` env variable, and Uncomment `pymongo` in the `requirements.txt`. 
4. `BOT_NAME` & `BOT_DEV` env variables are optional. But the website needs the BOT_NAME variable to auto detect the bot's name
5. You can add any other variables such as Bot Token, Admin Id or API keys in the same `.env` file. Same criteria goes for `requirements.txt` also.
6. Make sure you always have the access of your mail, in order to Login into the website. **It's not recommended to use Temp Mails**
7. If your bot is linked to a TR id and you lost the access of your TR account, **adding another TR id isn't possible**. You must need to use API endpoint to **unlink the existing TR id first**. 
8. **Don't ever share** your TR ID, Render API key etc. with anyone. On the other hand, Render URL can be shared.
9. The Project is open source and free, please share and give it a star if you like to 🙏

---


## <span class="tricon">🔴</span> Legal Notice ( Vital ) 

𝗧𝗵𝗶𝘀 𝗣𝗿𝗼𝗷𝗲𝗰𝘁 𝗶𝘀 𝗺𝗮𝗱𝗲 𝗳𝗼𝗿 𝗲𝗱𝘂𝗰𝗮𝘁𝗶𝗼𝗻𝗮𝗹 𝗽𝘂𝗿𝗽𝗼𝘀𝗲𝘀, 𝗯𝘂𝘁 𝗻𝗼𝘁𝗵𝗶𝗻𝗴 𝘂𝗻𝗲𝘁𝗵𝗶𝗰𝗮𝗹 𝗶𝘀 𝘂𝘀𝗲𝗱 𝗵𝗲𝗿𝗲. 𝗔𝗹𝗹 𝘁𝗵𝗲 𝗔𝗣𝗜 𝗳𝗲𝗮𝘁𝘂𝗿𝗲𝘀 𝗮𝗿𝗲 𝗮𝗹𝗿𝗲𝗮𝗱𝘆 𝗶𝗻 𝗥𝗲𝗻𝗱𝗲𝗿'𝘀 𝗔𝗣𝗜 𝗱𝗼𝗰𝘀. 𝗧𝗵𝗲 𝗢𝗻𝗹𝘆 𝗚𝗼𝗮𝗹 𝗼𝗳 𝘁𝗵𝗶𝘀 𝗣𝗿𝗼𝗷𝗲𝗰𝘁 𝗶𝘀 𝘁𝗼 𝗵𝗲𝗹𝗽 𝗽𝗲𝗼𝗽𝗹𝗲 𝗺𝗮𝗻𝗮𝗴𝗲 𝘁𝗵𝗲𝗶𝗿 𝗽𝗿𝗼𝗷𝗲𝗰𝘁𝘀 𝗲𝗮𝘀𝗶𝗹𝘆 𝗶𝗻 𝗼𝗻𝗲 𝗽𝗹𝗮𝗰𝗲, 𝗮𝗻𝗱 𝘀𝗽𝗲𝗰𝗶𝗮𝗹𝗹𝘆 𝗳𝗼𝗿 𝝉𝗵𝗼𝘀𝗲 𝘄𝗵𝗼 𝗰𝗮𝗻𝘁 𝗮𝗳𝗳𝗼𝗿𝗱 𝗮 𝗽𝗮𝗶𝗱 𝗽𝗹𝗮𝗻 𝗼𝗳 𝗿𝗲𝗻𝗱𝗲𝗿. 𝗣𝗹𝗲𝗮𝘀𝗲 𝗱𝗼𝗻𝘁 𝗺𝗶𝘀𝘂𝘀𝗲, 𝗼𝗿 𝗠𝗶𝘀𝘂𝗻𝗱𝗲𝗿𝘀𝘁𝗮𝗻𝗱 𝘁𝗵𝗲 𝗰𝗼𝗻𝗰𝗲𝗽𝘁. 𝗧𝗵𝗮𝗻𝗸𝘀 🙏

---

<p align="center">
  <sub>Built with ❤️ by</sub><br>
  <strong><a href="https://t.me/SuryaXCristiano" target="_blank">@SuryaXCristiano</a></strong>
</p>

<p align="center">
  <sub>© 2026 Copyright Reserved @SuryaXCristiano </sub>
</p>
