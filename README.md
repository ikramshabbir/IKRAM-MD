<div align="center">🦅 X-ANSARI MD

⚡ Fast • Powerful • Modern WhatsApp Automation

A feature-rich WhatsApp bot built with Node.js & Baileys

<p>
  <img src="https://img.shields.io/badge/X--ANSARI-MD-black?style=for-the-badge" alt="X-ANSARI">
  <img src="https://img.shields.io/badge/Version-4.0.0-blue?style=for-the-badge" alt="Version 4.0.0">
  <img src="https://img.shields.io/badge/Node.js-20%2B-green?style=for-the-badge&logo=node.js" alt="Node.js">
  <img src="https://img.shields.io/badge/Baileys-6.7.24-purple?style=for-the-badge" alt="Baileys">
</p><p>
  <b>⚡ Built for speed.</b>
  &nbsp;•&nbsp;
  <b>🛡️ Built for stability.</b>
  &nbsp;•&nbsp;
  <b>🦅 Built for WhatsApp.</b>
</p></div>---

🌟 About X-ANSARI

X-ANSARI MD is a modern, modular and feature-rich WhatsApp bot designed to provide a fast and powerful WhatsApp automation experience.

Built with Node.js and Baileys, X-ANSARI combines media tools, group management, owner controls, utilities, automation and a modular plugin architecture into one powerful WhatsApp bot.

«🦅 X-ANSARI — More than a bot. A complete WhatsApp experience.»

---

✨ Features

⚡ Core

- 🚀 Fast command processing
- 🔄 Automatic reconnection
- 💾 SQLite database support
- 🧩 Modular plugin architecture
- 🛡️ Command access control
- 📊 Command logging & metrics
- 🌐 Public / private bot modes
- 🌍 Multi-language support
- 🎯 Prefix-based command system

👑 Owner & Administration

- 👑 Owner-only commands
- 🛡️ Group administration
- 🔗 Anti-link protection
- 🚫 Anti-spam controls
- ⚠️ Warning system
- 🔇 User mute management
- 👋 Welcome & goodbye messages
- ⚙️ Per-group settings

🎨 Media & Utilities

- 🖼️ Image tools
- 🎨 Sticker tools
- 🎵 Audio/media utilities
- 📝 Text-to-speech tools
- ✨ Fancy text generation
- 💬 Quote generation
- 🖌️ Image/text effects
- 🎬 Media conversion powered by FFmpeg

🤖 Automation

- 💬 Automatic reactions
- 🎯 Keyword-based reaction categories
- 🧠 Smart command handling
- ⚡ Fast response path for lightweight commands
- 🔧 Configurable automation features

---

📦 Requirements

Requirement| Version
Node.js| 20+
npm| Latest recommended
Git| Recommended
FFmpeg| Required for media features
SQLite| Included through Node package

«💡 Node.js 20+ is recommended for the current project.»

---

🚀 Installation

1️⃣ Clone the repository

git clone https://github.com/ikramshabbir/X-ANSARI.git

Enter the project:

cd X-ANSARI

---

2️⃣ Install dependencies

npm install

If your environment needs optional/native dependencies:

npm install --include=optional --foreground-scripts

---

3️⃣ Configure environment

If ".env.example" exists:

cp .env.example .env

Otherwise create:

nano .env

Example configuration:

BOT_MODE=public
BOT_LANG=en

PREFIX=.

SUDO=

STICKER_PACKNAME=X-ANSARI
STICKER_AUTHOR=X-ANSARI

---

⚙️ Configuration

Variable| Description
"BOT_MODE"| "public" or "private"
"BOT_LANG"| Bot language
"PREFIX"| Command prefix
"SUDO"| Additional privileged users
"STICKER_PACKNAME"| Sticker pack name
"STICKER_AUTHOR"| Sticker author

«⚠️ Never upload your real ".env" file or authentication credentials to GitHub.»

---

▶️ Start the Bot

Start X-ANSARI with:

npm start

The bot initializes its database, plugins and WhatsApp connection automatically.

---

📱 WhatsApp Pairing

On the first startup, follow the pairing/login instructions displayed by the bot.

Once authentication is completed, the session is stored locally so the bot can reconnect without requiring repeated pairing.

«🔐 Never share your WhatsApp authentication/session files.»

---

🧩 Commands

The default prefix is:

.

Examples:

.ping
.menu
.help

---

⚡ General

Command| Description
".ping"| Check bot response
".menu"| Display command menu
".help"| Show command help

---

👑 Owner

Examples:

.broadcast
.repeat
.exif

Owner commands are restricted to authorized users.

---

🛡️ Group Management

Depending on enabled plugins:

.warn
.mute
.kick
.promote
.demote

Group features can include:

- 🔗 Anti-link
- 🚫 Anti-spam
- 👋 Welcome messages
- 👋 Goodbye messages
- ⚠️ Warning system
- 🔇 User mute management
- ⚙️ Per-group settings

---

🎨 Media

Examples:

.sticker
.ttp
.attp
.tts
.quote
.fancy

Available commands depend on the installed plugins.

---

🤖 AutoReact

X-ANSARI includes a lightweight local keyword-based AutoReact system.

Control it with:

.autoreact on
.autoreact off
.autoreact status

AutoReact uses local keyword/category matching and does not require an external AI API for its reaction engine.

Possible categories include:

- ❤️ Love
- 😂 Funny
- 😍 Amazing
- 👍 Agree
- 🙏 Islamic / Dua
- 😢 Sad
- 😮 Surprise
- 🎉 Congratulations
- 👋 Greeting
- 🌅 Morning
- 🌙 Night
- 👋 Goodbye
- 🥺 Accident

---

🗂️ Project Structure

X-ANSARI/
│
├── index.js
├── package.json
├── package-lock.json
├── .env
├── .gitignore
│
├── src/
│   │
│   ├── config/
│   │
│   ├── database/
│   │
│   ├── enterprise/
│   │
│   ├── messages/
│   │   ├── handler.js
│   │   └── serialize.js
│   │
│   ├── plugins/
│   │
│   ├── socket/
│   │   └── connection.js
│   │
│   └── utils/
│       ├── message.js
│       ├── group.js
│       └── groupSettings.js
│
└── README.md

---

🧩 Plugin Architecture

X-ANSARI uses a modular command/plugin system.

Example:

command(
  {
    pattern: "example",
    fromMe: false,
    desc: "Example command",
    type: "misc",
  },
  async (message, conn) => {
    // Command logic
  }
);

This allows individual commands to be added, removed and maintained independently.

---

⚡ Performance

X-ANSARI is designed with lightweight command processing in mind.

Performance features

- ⚡ Fast command detection
- 🚀 Lightweight command execution
- 🧠 Command caching where appropriate
- 💾 Persistent settings
- 🔄 Automatic connection recovery
- 🧩 Modular processing
- ⚡ Optimized lightweight command paths

Example:

.ping
   │
   ▼
Command Detection
   │
   ▼
Fast Execution
   │
   ▼
Pong

---

🎬 FFmpeg

FFmpeg is required by several media commands.

Check installation:

ffmpeg -version

Find FFmpeg:

which ffmpeg

Termux

pkg install ffmpeg

---

📱 Termux Deployment

Clone:

git clone https://github.com/ikramshabbir/X-ANSARI.git

Enter:

cd X-ANSARI

Install:

npm install

Start:

npm start

PM2

Install PM2:

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

☁️ VPS / Linux Deployment

Clone:

git clone https://github.com/ikramshabbir/X-ANSARI.git
cd X-ANSARI

Install:

npm install

Start:

npm start

Production with PM2

pm2 start index.js --name X-ANSARI
pm2 save

Check:

pm2 status

---

🐳 Docker Deployment

Example "Dockerfile":

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

«⚠️ Configure persistent storage for authentication/session data when using containers.»

---

🔐 Security

Never expose:

.env
WhatsApp session files
Authentication credentials
Database credentials
API keys
Hosting credentials
GitHub tokens

Recommended ".gitignore":

.env
*.db
sessions/
auth/
node_modules/
logs/

---

🛠️ Troubleshooting

Bot doesn't start

Check Node:

node -v

Check npm:

npm -v

Reinstall dependencies:

rm -rf node_modules
npm install

---

FFmpeg isn't detected

Run:

which ffmpeg

Then:

ffmpeg -version

---

SQLite error

Install optional/native dependencies:

npm install --include=optional --foreground-scripts

Test SQLite:

node -e "const Database=require('better-sqlite3'); const db=new Database(':memory:'); console.log('SQLITE WORKING'); db.close()"

Expected:

SQLITE WORKING

---

🔄 Update X-ANSARI

Pull the latest changes:

git pull origin main

Install dependencies:

npm install

Restart:

npm start

---

👨‍💻 Development

Clone:

git clone https://github.com/ikramshabbir/X-ANSARI.git
cd X-ANSARI

Create a branch:

git checkout -b feature/my-feature

Check JavaScript syntax:

node --check index.js

Stage:

git add .

Commit:

git commit -m "Add new feature"

Push:

git push origin feature/my-feature

---

🤝 Contributing

Contributions, improvements and bug reports are welcome.

Contribution flow

Fork
  ↓
Create Branch
  ↓
Make Changes
  ↓
Test
  ↓
Commit
  ↓
Push
  ↓
Pull Request

Please keep contributions:

- 🧹 Clean
- 🧩 Modular
- 🧪 Tested
- 📚 Documented
- 🔒 Secure

---

🐛 Bug Reports

When reporting an issue, include:

- Node.js version
- npm version
- Operating system / hosting
- Error message
- Relevant logs
- Steps to reproduce

Never include:

- WhatsApp session credentials
- Authentication files
- Passwords
- API keys
- GitHub tokens

---

📜 License

Please review the repository's license before redistributing or publishing modified versions.

---

👑 Credits

<div align="center">🦅 X-ANSARI MD

Developed & Maintained By

IKRAM SHABBIR

<p>
  <b>⚡ Speed</b>
  &nbsp;•&nbsp;
  <b>🛡️ Stability</b>
  &nbsp;•&nbsp;
  <b>🧩 Modularity</b>
  &nbsp;•&nbsp;
  <b>🚀 Innovation</b>
</p>---

❤️ Special Thanks

To the open-source developers, contributors and projects that make WhatsApp automation possible.

Special thanks to the Baileys ecosystem and its contributors.

---

⭐ Support the Project

If you find X-ANSARI MD useful:

⭐ Star the repository

🍴 Fork the project

🐛 Report bugs

💡 Suggest improvements

---

<br>🦅 X-ANSARI

Built with passion. Powered by code.

</div>
