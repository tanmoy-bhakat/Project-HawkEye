The required Code is present in "Project HawkEye.pdf".

📜 Guide: How to Get the Necessary Credentials
1. 🔑 Obtain Your Telegram Bot Token
This token is the password that allows your ESP32 to send messages as your bot..
Action: Open Telegram and search for the official account: @BotFather.
Command: Send the command /token (if you already created the bot) or /newbot (if starting fresh).
Result: BotFather will provide a token that looks like: 1234567890:ABC-DEF1234567890_GHIJ-KLMNO.
Usage in Code: Replace the placeholder YOUR_BOT_TOKEN with this entire string.

2. 💬 Find Your Telegram Chat ID
The Chat ID tells the bot which user to send the message to. Since your bot is public, we'll use a simple method:
Action A (Start Chat): Search for your bot, @Your_bot, and send it any message (e.g., "Start").
Action B (Get Update URL): Open your web browser and navigate to the following URL, replacing the placeholder with your actual bot token:
https://api.telegram.org/bot<YOUR_BOT_TOKEN>/getUpdates
Result: The browser will display a large block of code (JSON). Look inside this code for the first instance of "chat":{"id":...
The long number next to "id" (e.g., 1175576925) is your Chat ID.
Usage in Code: Replace the placeholder YOUR_CHAT_ID_1 with this number. If you want to send alerts to multiple users, repeat this process for each user and add their IDs to the chatIDs[] array.

3. 🌐 Finalizing WiFi Credentials
Action: Replace YOUR_WIFI_SSID and YOUR_WIFI_PASSWORD with the exact name and password of the Wi-Fi network you are using (e.g., your mobile hotspot).



## 🙌 Acknowledgments

This project was a collaborative effort by our team, where everyone contributed to different aspects of design, coding, and testing.

- **Tanmoy** — Contributed to coding, debugging, ESP32–Telegram integration, and resolving technical issues during the development process.  
- **Tushar** — Contributed to circuit design, model implementation, and also assisted in setting up the Telegram-based SMS alert system.
- **Himanshi** — Contributed to model designing and solely created the **Project HawkEye ppt** presentation, ensuring a clear and well-documented visual representation of the project. 
- **Rohit** and **Sayantan** — Contributed to circuit design, component setup, and model fabrication.  

Together, we successfully developed **Project HawkEye**, a laser-based intrusion detection and alert system using ESP32 and Telegram integration.
