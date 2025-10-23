# QuestKeeper Bot Dashboard Setup

## Prerequisites
1. XAMPP (Apache + MySQL + PHP)
2. Python 3.8+
3. Discord Bot Token

## Installation Steps

### 1. Database Setup
1. Start XAMPP (Apache + MySQL)
2. Go to http://localhost/phpmyadmin
3. Create a new database called `questkeeper_bot`
4. The tables will be created automatically when you first visit the dashboard

### 2. Python Dependencies
```bash
pip install discord.py mysql-connector-python
```

### 3. Discord Application Setup
1. Go to https://discord.com/developers/applications
2. Select your QuestKeeper application
3. In OAuth2 section, add redirect URI: `http://localhost/BotDashboard/dashboard.php`
4. Copy your Client Secret and update it in dashboard.php

### 4. Bot Configuration
1. Update bot.py with your bot token
2. Make sure bot_database.py is in the same directory as bot.py
3. Update database credentials in bot_database.py if needed

### 5. File Structure
```
BotDashboard/
├── homepage.html
├── dashboard.php
├── config.php
├── api.php
├── bot_database.py
├── bot.py
└── bot_commands.json (created automatically)
```

## Features Added

### Real Discord Integration
- ✅ Shows your actual Discord servers
- ✅ Identifies servers where the bot is present
- ✅ Real user statistics from database
- ✅ Real quest activity feed

### Bot Configuration
- ✅ Select server by clicking on it
- ✅ Configure quest channels through web interface
- ✅ Updates bot configuration in real-time
- ✅ Persistent storage in MySQL database

### Database Integration
- ✅ User quest statistics
- ✅ Quest activity logging
- ✅ Bot configuration per server
- ✅ Quest management

## Usage

1. Start XAMPP
2. Run your Discord bot: `python bot.py`
3. Visit http://localhost/BotDashboard/homepage.html
4. Click "Dashboard" and login with Discord
5. Click on a server to select it for configuration
6. Click "Configure Channels" to set up the bot

## Commands Available
- `!submitquest` - Create a new quest (works as before)
- `!queststats` - View quest statistics (now pulls from database)

The dashboard now shows real data and allows actual bot configuration!
