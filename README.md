# Aternos AFKBot ✨  

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](/LICENSE)  

### This AFK Bot will keep your Aternos server alive 24/7.

#### If you're having any problems or errors with this, please let me know by creating an Issue.  
<br/>

# Let's Get Started!

# Requirements 🎒
What You'll need

1. A Render.com account. (It's free and simple)  
   Sign up at: https://render.com

2. An UptimeRobot account. (It's also free and simple)  
   Sign up at: https://uptimerobot.com/signUp

3. An Aternos server or any Minecraft server you own.  
   Make sure your server settings have `online-mode` set to `false`.

4. A GitHub account.

# Setup ⚙
1. Fork this repository, and edit the `config.json` file (add your server IP, port, bot username, and version if needed — e.g., "1.21").

2. Go to https://dashboard.render.com and click **New** > **Web Service**.

3. Connect your GitHub account (if not already), then select the forked repository.

4. Configure the service:  
   - **Name**: e.g., "Aternos-AFK-Bot"  
   - **Runtime**: Node  
   - **Build Command**: `npm install`  
   - **Start Command**: `node index.js` (or check your repo's `package.json` for the correct start script, often `node bot.js` or `npm start`)  
   - **Plan Type**: Free  

5. Click **Create Web Service**. Render will automatically build and deploy it.  
   Watch the **Logs** tab — it should show the bot connecting to your server.

6. Once deployed and running, copy the service URL from the top of the Render dashboard (it looks like `https://your-bot-name.onrender.com`).

7. Go to https://uptimerobot.com/dashboard.  
   Click **Add New Monitor** and set:  
   - **Monitor Type**: HTTP(s)  
   - **Friendly Name**: e.g., "Aternos Bot Keeper"  
   - **URL (or IP)**: Paste your Render service URL  
   - **Monitoring Interval**: Every 5 minutes (or 10 minutes to be safe)  
   Click **Create Monitor**.

8. Finally... DONE! Enjoy your free 24/7 Aternos server.

   (Tip: In-game, build a small enclosed bedrock room for the bot to stand in safely. Optionally OP it and run commands like `/effect give YourBotName minecraft:resistance infinite 255 true` to keep it alive.)

# CAUTION ⚠
### Aternos might detect your suspicious actions and delete your server or account!  
**By doing this, you acknowledge that you are responsible for any problems that arise.**  
**I DO NOT RECOMMEND DOING THIS ON YOUR MAIN ATERNOS SERVER!**  

**Extra notes on Render free tier**:  
- Free Web Services spin down after ~15 minutes of no inbound HTTP traffic (your bot might disconnect temporarily).  
- UptimeRobot pings keep it awake by sending regular requests.  
- You get 750 instance hours/month — plenty for one bot, but spun-down time doesn't count.  

If the bot disconnects often (e.g., on Minecraft 1.21+), check for an updated Mineflayer fork or repo that supports the latest protocol. Test on a backup world first! 🚀