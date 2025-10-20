# JobPointsShop - Jobs Reborn Addon

A comprehensive **Job Points management system** for Minecraft servers. Create redeemable vouchers, manage sellable items, and provide players with an intuitive economy system integrated with Jobs Reborn.

---

## 📦 Dependencies

**REQUIRED:** [JobsReborn](https://www.spigotmc.org/resources/jobs-reborn.4216/)

This plugin is an addon for Jobs Reborn and will not work without it!

---

## 🌟 Features

### 💰 Job Points Vouchers
- **Create vouchers** that players can redeem for job points
- **Single-use system** - vouchers are consumed when used
- **Auto-redeem** if player's inventory is full
- **Bulk distribution** with `/jgiveall` + custom messages
- **Mob drop vouchers** for special rewards

### 🎁 Collectible Items
- **Event Vouchers** (`/jevent`) - Commemorative items for special events
- **Custom Collectibles** (`/jitem`) - Achievement rewards, rank-up items
- Cannot be redeemed - kept as memorabilia
- Shows event name and timestamp

### 🛒 Advanced SellAll System
- **Visual GUI** for selling items with prices
- **Item Configuration GUI** - Place items directly to set prices ⭐ NEW
- **Chat-based Q&A flow** - 3 simple questions to configure any item
- **Stack-only mode** - Require full stacks for selling
- **Per-block mode** - Sell any amount of items
- **Auto-sell system** with two modes:
  - `all` - Auto-sell all configured items when picked up
  - `hand` - Auto-sell only items matching hand

### 🎨 Polish & Quality of Life
- ✅ **Cooldown system** (1 second) to prevent spam
- ✅ **Visual effects** - titles, sounds, particles
- ✅ **Full color support** with Minecraft color codes
- ✅ **Smart validation** - prevents invalid configurations
- ✅ **Real-time updates** - changes take effect immediately

---

## 🎯 Item Configuration GUI (Best Feature!)

### How It Works
1. Type `/jobpointshop config` as admin
2. Place ANY item in the chest GUI
3. Answer 3 simple questions in chat:
   - **Q1:** How many items per stack? (16/32/64)
   - **Q2:** How much for 1 stack? (points)
   - **Q3:** Stack-only or per-block?

### Example
```
Admin places DIAMOND in GUI
Q1: 64          → Stack size is 64 items
Q2: 100         → 100 points for 1 full stack
Q3: block       → Players can sell any amount

Result: 100 ÷ 64 = 1.5625 points per diamond
- Sell 1 diamond = 1.56 points
- Sell 64 diamonds (1 stack) = 100 points
- Sell 640 diamonds (10 stacks) = 1000 points
```

**No more manual config.yml editing!** 🎉

---

## 📋 Commands

### Job Points Vouchers
| Command | Description | Permission |
|---------|-------------|------------|
| `/jgive <player> <points>` | Give a player a voucher | `jobpoints.admin` |
| `/jgiveme <points>` | Give yourself a voucher | `jobpoints.admin` |
| `/jmob <points>` | Create mob drop voucher | `jobpoints.admin` |
| `/jgiveall <points> [msg]` | Give all online players | `jobpoints.admin` |
| `/jevent <event name>` | Create event collectible | `jobpoints.admin` |
| `/jitem <title> <desc>` | Create custom collectible | `jobpoints.admin` |
| `/jcheck` | Check voucher details | `jobpoints.admin` |
| `/jhelp` | Show help menu | `jobpoints.admin` |

### Item Configuration
| Command | Description | Permission |
|---------|-------------|------------|
| `/jobpointshop config` | Open config GUI ⭐ | `jobpoints.admin` |
| `/sellallprice <item> <price>` | Set price (old method) | `sellall.admin` |
| `/sellallremove <item>` | Remove item | `sellall.admin` |
| `/sellallreload` | Reload config | `sellall.admin` |

### Player Commands
| Command | Description | Permission |
|---------|-------------|------------|
| `/sellall` or `/sall` | Open sell GUI | `sellall.use` |
| `/shand` | Sell all matching items | `sellall.use` |
| `/sauto [all\|hand]` | Toggle auto-sell | `sellall.use` |
| `/sellall prices` | View all prices | `sellall.use` |

---

## 🎮 Player Usage

### Redeeming Vouchers
1. **Right-click** any Job Points or Mob Drop voucher
2. Voucher is **consumed** and points are added
3. See **title notification** and hear sound effect
4. If inventory is full, points are auto-redeemed

### Selling Items
1. Use `/shand` to quickly sell all matching items
2. Use `/sauto hand` to auto-sell items matching your hand
3. Use `/sauto all` to auto-sell all configured items
4. Open `/sellall` GUI to see prices and sell manually

---

## ⚙️ Installation

1. **Install** [JobsReborn](https://www.spigotmc.org/resources/jobs-reborn.4216/) first (REQUIRED)
2. **Download** JobPointsShop-1.0.0.jar from Modrinth
3. **Place** in your server's `plugins/` folder
4. **Restart** your server
5. **Configure** permissions in your permission plugin
6. **Start** using `/jobpointshop config` to set up items!

---

## 🔧 Compatibility

- **Minecraft:** 1.21.x (Paper/Spigot)
- **Java:** 17+
- **Required:** Jobs Reborn (latest version)
- **Tested on:** Paper 1.21.1

---

## 🆕 What's New in v1.0.0

### Item Configuration GUI
✨ **Visual interface** for setting item prices - no more manual config editing!  
✨ **3-step chat flow**: Stack size → Price → Mode  
✨ **Place items directly** in GUI to configure  
✨ **Real-time validation** and confirmation  

### Enhanced SellAll
✨ `/shand` now sells ALL matching items in inventory  
✨ `/sall` added as quick alias  
✨ `/sauto hand` for item-specific auto-sell  
✨ `/sauto all` for full auto-sell  

### Bug Fixes
✅ Fixed price calculation for per-block mode  
✅ Corrected stack terminology  
✅ Improved configuration messages  

---

## 🎨 Screenshots

### Item Configuration GUI
![Admin places item in chest GUI to configure prices](https://via.placeholder.com/800x450/2C2F33/FFFFFF?text=Config+GUI+-+Place+Items+Here)

*Place any item in the chest, answer 3 questions, done!*

### SellAll GUI
![Players see prices and can sell items visually](https://via.placeholder.com/800x450/2C2F33/FFFFFF?text=SellAll+GUI+-+View+Prices)

*Players can view prices and sell items with a single click*

### Voucher System
![Job Points Vouchers with custom lore](https://via.placeholder.com/800x450/2C2F33/FFFFFF?text=Job+Points+Voucher)

*Beautiful vouchers with full color support*

---

## 🎯 Use Cases

### For Server Owners
- **Event rewards** - Give commemorative vouchers for participation
- **Rank rewards** - Custom collectibles for rank-ups
- **Economy control** - Fine-tune item values with stack/block modes
- **Player engagement** - Auto-sell reduces inventory management hassle

### For Players
- **Easy selling** - `/shand` to quickly sell items
- **Auto-sell** - Never worry about full inventories
- **Clear pricing** - GUI shows exactly what each item is worth
- **Collectibles** - Keep event vouchers as memorabilia

---

## 🚀 Coming Soon

### 🛍️ Shop System - Buy Items with Job Points
- **Browse items** in a GUI shop interface
- **Purchase items** using your earned job points
- **Admin configuration** for shop items and prices
- **Stock limits** and cooldowns support
- **Category organization** for easy navigation
- **Player-friendly** buy interface with confirmation

*Stay tuned for the next update!*

---

## ⚖️ License

**All Rights Reserved - Proprietary License**

See [LICENSE](LICENSE) for full terms.

This addon is proprietary software. **Do not redistribute, modify, or claim as your own.**

---

## 🐛 Bug Reports & Support

Found a bug? Have a suggestion?

- **GitHub Issues:** [Report Here](#) *(add your GitHub link)*
- **Discord:** dei2004 *(add your Discord)*
- **SpigotMC:** [Discussion Thread](#) *(add your Spigot link)*

---

## 👤 Credits

**Author:** dei2004  
**Based on:** Jobs Reborn by Zrips  
**Platform:** Paper/Spigot 1.21.x  

---

## 🔗 Links

- **Jobs Reborn:** [Spigot](https://www.spigotmc.org/resources/jobs-reborn.4216/)
- **Source Code:** *(Private/Available on request)*
- **Documentation:** See README.md

---

**Version:** 1.0.0  
**Last Updated:** October 20, 2025  
**Downloads:** [Modrinth](#) | [SpigotMC](#) | [Hangar](#)

---

*Made with ❤️ for the Minecraft community*
