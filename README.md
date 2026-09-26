<div align="center">🦅 X-ANSARI MD

⚡ Advanced WhatsApp Multi-Device Bot

Powerful • Fast • Modular • Reliable

""X-ANSARI" (https://img.shields.io/badge/X--ANSARI-MD-black?style=for-the-badge&logo=whatsapp)" (https://github.com/ikramshabbir/X-ANSARI)
""Version" (https://img.shields.io/badge/Version-4.0.0-blue?style=for-the-badge)" (https://github.com/ikramshabbir/X-ANSARI)
""Node.js" (https://img.shields.io/badge/Node.js-20%2B-green?style=for-the-badge&logo=node.js)" (https://nodejs.org/)
""Baileys" (https://img.shields.io/badge/Baileys-6.7.24-purple?style=for-the-badge)" (https://github.com/WhiskeySockets/Baileys)

<br>X-ANSARI MD is a modern, modular and performance-focused WhatsApp bot built with Node.js and Baileys.

</div>---

✨ About X-ANSARI

X-ANSARI MD is designed for users who want a powerful WhatsApp automation bot without unnecessary complexity.

It provides a modular plugin system, media tools, group management, owner controls, automation features and a lightweight architecture suitable for Termux, VPS and Pterodactyl/Waifly hosting.

🚀 Why X-ANSARI?

- ⚡ Fast command processing
- 🧩 Modular plugin architecture
- 📱 WhatsApp Multi-Device support
- 🛡️ Owner & admin controls
- 🎵 Media utilities
- 🖼️ Image & sticker tools
- 🤖 Local AutoReact system
- 💾 SQLite-based authentication
- 🎬 FFmpeg support
- 📦 Easy deployment
- 🔧 Easy customization

---

🌟 Features

🧠 Core

- WhatsApp Multi-Device
- Public / Private mode
- Custom command prefix
- Session management
- SQLite authentication
- Automatic reconnect handling
- Modular command loader
- Lightweight message processing

👑 Owner & Admin

- Broadcast tools
- Group management
- User management
- Bot mode controls
- Restart / shutdown controls
- Owner-only commands
- Admin permissions
- Group settings

🎨 Media

- Sticker creation
- Image processing
- Video processing
- TTP
- ATTP
- Fancy text
- Quote generator
- TTS
- Media conversion
- FFmpeg-powered utilities

🤖 Automation

- Local keyword-based AutoReact
- Custom reaction categories
- Group-specific settings
- Message utilities
- Anti-delete tools
- Automatic message handling

«AutoReact is designed around local keyword matching and does not require an external AI/Gemini API.»

---

📋 Requirements

Requirement| Version
Node.js| 20+
npm| Latest recommended
Git| Latest
FFmpeg| Recommended
RAM| 300MB+
Storage| 1GB+

---

📥 Installation

1. Clone Repository

git clone https://github.com/ikramshabbir/X-ANSARI.git
cd X-ANSARI

2. Install Dependencies

npm install

3. Start Bot

npm start

---

📱 WhatsApp Pairing

Start the bot:

npm start

Follow the pairing instructions shown in the terminal.

Once the WhatsApp account is linked, the authentication session is stored locally.

⚠️ Important

Do not delete your session/authentication database unless you intentionally want to link WhatsApp again.

---

⚙️ Configuration

Create or edit your ".env" file:

PREFIX=.
MODE=public
LANGUAGE=en

ADMIN_HTTP_PORT=8787
ADMIN_HTTP_HOST=0.0.0.0

ADMIN_HTTP_TOKEN=your_secure_token
PORTAL_PIN=your_secure_pin

«Configuration names can vary depending on the current project version. Keep existing working environment variables when updating the bot.»

---

🎮 Commands

The default prefix is:

.

Examples:

.ping
.menu
.help
.sticker
.fancy
.tts
.ttp
.attp
.quote

Use:

.menu

inside WhatsApp to see the complete command list available in your current installation.

---

🤖 AutoReact

X-ANSARI includes a local keyword-based AutoReact system.

Enable

.autoreact on

Disable

.autoreact off

Check Status

.autoreact status

AutoReact can recognize categories such as:

- ❤️ Love
- 👋 Greeting
- 😂 Funny
- 😍 Amazing
- 👍 Agree
- 😢 Sad
- 😮 Surprise
- 🎉 Congratulations
- 🙏 Islamic / Dua
- 🌅 Morning
- 🌙 Night
- 👋 Goodbye
- 😬 Accident
- 🙏 Thanks

AutoReact is OFF by default and only activates when explicitly enabled.

---

🗂️ Project Structure

X-ANSARI/
│
├── src/
│   ├── database/
│   ├── messages/
│   ├── plugins/
│   ├── socket/
│   └── utils/
│
├── plugins/
│
├── sessions/
│
├── index.js
├── package.json
├── package-lock.json
├── .env
└── README.md

---

🧩 Plugin Architecture

Commands are implemented through a modular plugin system.

A typical plugin looks like:

import { command } from "../plugins.js";

command(
  {
    pattern: "example",
    fromMe: false,
    desc: "Example command",
    type: "misc",
  },
  async (message, conn) => {
    await message.reply("Hello from X-ANSARI!");
  }
);

This makes it easy to add, remove or customize commands without modifying the core bot.

---

⚡ Performance

X-ANSARI is designed to keep command processing lightweight.

Important performance features include:

- Non-blocking command handling
- Lightweight message serialization
- Duplicate-message protection
- Fast command paths
- Local database access
- Modular plugin loading
- Minimal external dependencies

The ".ping" command is intended as a quick response test:

.ping

Example:

Pong · 0ms

«The displayed milliseconds measure the bot's command/send operation, not necessarily the complete WhatsApp network delivery time.»

---

🎬 FFmpeg

FFmpeg is recommended for media commands.

Check FFmpeg:

ffmpeg -version

Check the executable:

which ffmpeg

If FFmpeg is available, media commands such as video/image conversion and text-to-media utilities can use it.

---

📱 Termux Deployment

Install Termux packages:

pkg update
pkg upgrade
pkg install git nodejs ffmpeg

Clone the project:

git clone https://github.com/ikramshabbir/X-ANSARI.git
cd X-ANSARI

Install dependencies:

npm install

Start:

npm start

For persistent execution, a process manager such as PM2 can be used:

npm install -g pm2

Start:

pm2 start index.js --name X-ANSARI

Save:

pm2 save

Check:

pm2 status

Logs:

pm2 logs X-ANSARI

---

🖥️ VPS / Linux Deployment

Clone:

git clone https://github.com/ikramshabbir/X-ANSARI.git
cd X-ANSARI

Install:

npm install

Start:

npm start

For PM2:

npm install -g pm2
pm2 start index.js --name X-ANSARI
pm2 save

---

🐳 Docker

Example Dockerfile:

FROM node:20

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

CMD ["npm", "start"]

Build:

docker build -t x-ansari .

Run:

docker run -d --name x-ansari x-ansari

---

🛡️ Security

Never publicly share:

- WhatsApp session files
- Authentication databases
- ".env"
- Admin tokens
- Portal PINs
- Private credentials

Recommended ".gitignore":

node_modules/
.env
sessions/
*.db
*.sqlite
*.sqlite3
logs/

---

🔧 Troubleshooting

Bot does not start

Check Node.js:

node -v

Check npm:

npm -v

Reinstall dependencies:

rm -rf node_modules
npm install

Then:

npm start

---

FFmpeg not found

Check:

which ffmpeg

Then:

ffmpeg -version

Make sure FFmpeg is installed and accessible from the system PATH.

---

SQLite Error

Test:

node -e "const Database=require('better-sqlite3'); const db=new Database(':memory:'); console.log('SQLITE WORKING'); db.close()"

Expected:

SQLITE WORKING

---

Bot disconnects

Check the terminal logs first.

Do not delete authentication/session data unless you intentionally want to pair WhatsApp again.

Restart the bot:

npm start

---

🔄 Update

Before updating, make sure your local changes are committed.

Pull the latest version:

git pull origin main

Install any new dependencies:

npm install

Start:

npm start

---

🧑‍💻 Development

Clone:

git clone https://github.com/ikramshabbir/X-ANSARI.git
cd X-ANSARI

Install dependencies:

npm install

Check JavaScript syntax:

node --check index.js

For a specific file:

node --check src/messages/handler.js

---

🤝 Contributing

Contributions, improvements and bug fixes are welcome.

Contribution flow

git clone https://github.com/ikramshabbir/X-ANSARI.git
cd X-ANSARI

git checkout -b feature/my-feature

Make your changes, test them, then:

git add .
git commit -m "Add my feature"
git push origin feature/my-feature

Open a Pull Request on GitHub.

---

🐛 Bug Reports

When reporting a bug, include:

- Node.js version
- npm version
- Operating system
- Bot version
- Command that caused the issue
- Relevant terminal logs
- Steps to reproduce

Never include your WhatsApp session or private credentials.

---

📜 License

This project is provided for personal and educational use.

Please respect:

- WhatsApp's Terms of Service
- Applicable laws
- User privacy
- Group rules
- Platform policies

The developers are not responsible for misuse of the software.

---

❤️ Credits

🦅 X-ANSARI MD

Developed and maintained by:

Ikram Shabbir

GitHub:

https://github.com/ikramshabbir

Project:

https://github.com/ikramshabbir/X-ANSARI

Built with:

- Node.js
- Baileys
- SQLite
- FFmpeg
- Sharp

---

<div align="center">⚡ X-ANSARI MD

Fast. Modular. Powerful.

⭐ If you find the project useful, consider giving the repository a star.

Made with ❤️ by Ikram Shabbir

</div>
