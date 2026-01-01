# 🎮 InversedChat

**The ultimate Minecraft chat plugin** with AI moderation, custom commands, friend system, interactive chat games, and advanced features!

## 🆕 Latest Features

### 🤖 AI Chat Moderation
- **Automatic content filtering** powered by OpenAI Moderations API
- **Smart detection** of inappropriate language, toxicity, hate speech, and harassment
- **Progressive punishment system**: warnings → kick → ban
- **Configurable thresholds** for each punishment level
- **Real-time moderation** with minimal performance impact
- **Zero false positives** with AI-powered analysis

### ⚡ Custom Commands System
- **Create unlimited custom commands** directly in config.yml
- **No coding required** - simple YAML configuration
- **Multiple action types**: messages, broadcasts, console commands, sounds, titles, actionbars
- **Full PlaceholderAPI support** for dynamic content
- **Permission system** with customizable permission messages
- **Command aliases** support for multiple command names
- **Argument placeholders**: `{player}`, `{arg_0}`, `{args}`, etc.
- **Pre-configured examples** ready to use out of the box

### 📢 Autobroadcast In-Game Manager
- **Manage broadcasts** directly from Minecraft without editing files
- **Full GUI-like experience** with intuitive commands
- **Live editing** - changes apply instantly without restart
- Commands:
  - `/finalchat broadcast list` - View all configured broadcasts
  - `/finalchat broadcast add <message>` - Add a new broadcast
  - `/finalchat broadcast remove <id>` - Remove a broadcast by ID
  - `/finalchat broadcast edit <id> <message>` - Edit existing broadcast
  - `/finalchat broadcast interval <seconds>` - Change broadcast interval
  - `/finalchat broadcast toggle` - Enable/disable entire system

## ✨ Core Features

### 🎯 Chat System
- **Advanced Chat System** with multiple channels (Global, Local, Staff, Trade)
- **Channel GUI** - View and switch channels with `/channel`
- **Anti-Spam Protection** - Cooldowns, caps detection, duplicate message blocking
- **Word Filter** - Customizable blocked words with smart regex generation
- **Player Mentions** - @mention players with sound notifications
- **Chat Invisibility** - Hide your ability to send messages
- **Multi-language Support** - English and Italian included

### 👥 Friend System
Comprehensive friend management with advanced features:
- **Friend Codes** - Unique codes for adding friends with rewards
- **Friend List** - View all your friends with `/friend list`
- **Remove Friends** - Remove friends with `/friend remove <player>`
- **Block System** - Block players from sending you friend requests
- **Blocked List** - View all blocked players with `/friend blocked`
- **Friend Tag** - See `[FRIEND]` tag in private messages
- **Statistics** - Track friend count and redeemed codes
- **Regenerate Code** - Get a new friend code (costs money via Vault)

### 💬 Private Messaging
- **Private messages** with `/msg` and `/reply`
- **Friend indicator** - Shows `[FRIEND]` tag when messaging friends
- **Message spy** - Admins can monitor all private messages with `/spymsg`
- **Ignore system** - Ignore specific players or all messages
- **Sound notifications** - Hear when you receive messages

### 🎲 Chat Games
Interactive games that players participate in through chat:
- **Math Games** - Solve arithmetic problems
- **Unscramble** - Unscramble random words
- **Trivia** - Answer trivia questions
- **Auto-start** - Games start automatically at intervals
- **Rewards** - Winners get configurable rewards
- **Manual control** - Staff can start/stop games anytime

### 🎩 Additional Features
- **Hat Command** - Wear any item as a hat with `/hat`
- **Staff Chat** - Private channel for staff communication
- **Clear Chat** - Clear chat for all players
- **Mute Chat** - Temporarily disable global chat
- **String Similarity Tool** - Check similarity between words (anti-filter tool)
- **Regex Generator** - Generate regex patterns for word filtering

## 🔌 Integrations

| Plugin | Status | Description |
|--------|--------|-------------|
| **Vault** | ✅ Working | Economy for friend code regeneration, prefix/suffix support |
| **PlaceholderAPI** | ✅ Working | Full placeholder support in all messages |
| **CoinsEngine** | ✅ Working | Alternative economy system integration |
| **Discord** | ✅ Working | Webhook for chat, joins, deaths, broadcasts |
| **Tebex** | ✅ Working | Webhook for purchase announcements |
| **CraftingStore** | ✅ Working | Webhook for purchase announcements |
| **ChatControl Red** | ✅ Working | Full compatibility layer |
| **InteractiveChat** | ✅ Working | Item hover, inventory display, `[inv]` support |
| **EnderContainers** | ⚠️ Planned | Quick commands (`!ec <number>`) |

## 📝 Commands

### Main Commands
| Command | Description | Permission |
|---------|-------------|------------|
| `/finalchat help` | Show help menu | - |
| `/finalchat reload` | Reload plugin & config | `finalchat.admin.reload` |
| `/finalchat version` | Show plugin version | - |
| `/finalchat similar <word1> <word2>` | Check word similarity % | `finalchat.admin` |
| `/finalchat regex <word>` | Generate regex pattern | `finalchat.admin` |
| `/finalchat broadcast` | Manage autobroadcasts | `finalchat.admin` |

### Broadcast Manager
| Command | Description |
|---------|-------------|
| `/finalchat broadcast list` | List all broadcasts with IDs |
| `/finalchat broadcast add <message>` | Add new broadcast |
| `/finalchat broadcast remove <id>` | Remove broadcast by ID |
| `/finalchat broadcast edit <id> <message>` | Edit existing broadcast |
| `/finalchat broadcast interval <seconds>` | Set broadcast interval |
| `/finalchat broadcast toggle` | Enable/disable broadcasts |

### Chat Commands
| Command | Aliases | Description | Permission |
|---------|---------|-------------|------------|
| `/msg <player> <message>` | /tell, /w | Send private message | - |
| `/reply <message>` | /r | Reply to last message | - |
| `/ignore <player>` | - | Ignore/unignore player | - |
| `/ignoreall` | - | Ignore all messages | `finalchat.ignoreall` |
| `/spymsg` | - | Toggle message spy mode | `finalchat.spymsg` |
| `/clearchat` | /cc | Clear chat for all | `finalchat.clearchat` |
| `/mutechat` | - | Mute/unmute global chat | `finalchat.mutechat` |
| `/broadcast <msg>` | /bc | Send broadcast | `finalchat.broadcast` |
| `/staffchat <msg>` | /sc | Staff chat message | `finalchat.staffchat` |
| `/channel [name]` | /ch | Switch/view channels | `finalchat.channel` |
| `/chatinv` | /ci | Toggle chat invisibility | - |

### Friend System
| Command | Description |
|---------|-------------|
| `/friend code` | Show your friend code |
| `/friend redeem <code>` | Redeem a friend code |
| `/friend stats` | Show friend statistics |
| `/friend list` | List all your friends |
| `/friend remove <player>` | Remove a friend |
| `/friend block <player>` | Block a player |
| `/friend unblock <player>` | Unblock a player |
| `/friend blocked` | Show blocked players list |
| `/friend regenerate` | Regenerate your friend code |

### Other Commands
| Command | Description | Permission |
|---------|-------------|------------|
| `/hat` | Wear item as hat | `finalchat.hat` |
| `/chatgame [start/stop]` | Manage chat games | `finalchat.chatgame` |

## 🤖 AI Moderation Setup

1. **Get OpenAI API Key**
   - Visit [OpenAI Platform](https://platform.openai.com/api-keys)
   - Create an account or sign in
   - Generate a new API key

2. **Configure in config.yml**
```yaml
ai-moderation:
  enabled: true
  api-key: "sk-proj-YOUR_API_KEY_HERE"
  warn-threshold: 1    # Violations before warning
  kick-threshold: 3    # Violations before kick
  ban-threshold: 5     # Violations before ban
```

3. **Restart** the plugin or use `/finalchat reload`

4. **Test it!** Try sending inappropriate messages - AI will detect and warn you

## ⚡ Custom Commands Setup

Create powerful custom commands without coding!

### Example: Rules Command
```yaml
custom-commands:
  rules:
    command: "rules"
    aliases:
      - "regole"
    permission: ""
    actions:
      - "[message] &8&m-----------------------------"
      - "[message] &6&lServer Rules"
      - "[message] &e1. &7Be respectful"
      - "[sound] ENTITY_PLAYER_LEVELUP 1.0 1.0"
```

### Action Types
- `[message]` - Send message
- `[broadcast]` - Broadcast
- `[console]` - Console command
- `[player]` - Player command
- `[sound]` - Play sound
- `[title]` - Send title
- `[actionbar]` - Actionbar

### Placeholders
- `{player}` - Player name
- `{arg_0}`, `{args}` - Arguments
- PlaceholderAPI supported

## 📦 Installation

1. Download FinalChat.jar
2. Place in `plugins` folder
3. Install optional: Vault, PlaceholderAPI
4. Start server
5. Configure `config.yml`
6. Reload with `/finalchat reload`

## 🔐 Key Permissions

- `finalchat.*` - All permissions
- `finalchat.admin` - Admin access
- `finalchat.spymsg` - Spy messages
- `finalchat.bypass.cooldown` - Bypass cooldowns

## 🛠️ Info

- **Author**: InversedDevelopement (crudochef)
- **Version**: 1.0.0
- **Minecraft**: 1.16+ (Paper/Spigot)
- **Java**: 21

---

**Enjoy FinalChat!** 🎉
