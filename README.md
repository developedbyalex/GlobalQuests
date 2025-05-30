# GlobalQuests

**Quests to be completed by everyone.**

## Overview

GlobalQuests is a Minecraft plugin that enables players to collaborate on server-wide challenges. Players contribute collectively to complete objectives such as:

- Mining a specific number of blocks  
- Collecting experience points (EXP)  
- Killing mobs  
- Farming specific items  
- Crafting x amount of items  
- Placing x amount of blocks  

All progress is tracked globally, and rewards are given when the quest is completed by the community. The plugin is fully configurable and supports custom quest types, dynamic reward distribution, and persistent data saving using simple JSON files.

---

## Quest Progress

Quest progress is **tracked globally**, meaning all players on the server contribute to the same active quest. Each player's contributions are individually tracked, which allows for features such as top contributors and leaderboard-style rewards.

---

## Reward System

You have control over how rewards are given when a quest is completed:

- **Top Contributors**: You can configure different rewards for the top 3 players based on their contributions.
- **All Participants**: You can optionally enable rewards for everyone who contributed, regardless of amount.
- **Configurable**: This logic is configurable in the plugin's settings so you can choose what fits your server best.

---

## Data Storage

Quest and player contribution data is **persisted using a local JSON file**, meaning all data survives server restarts without needing a database. The plugin saves:

- Current active quest
- Progress and total contribution amounts
- Time remaining on the quest
- Player contribution data

---

## Commands & Permissions

Main Command: `/gquest`  
Aliases: `/gq`, `/quests`

| Command                               | Permission            | Description                                                       |
|---------------------------------------|------------------------|-------------------------------------------------------------------|
| `/gquest forcestart [questName]`      | `gquest.forcestart`    | Force start a specific quest, bypassing the timer                |
| `/gquests progress`                   | `gquest.progress`      | View the current quest's progress (customizable in config)       |
| `/gquests forcecomplete [questName]`  | `gquest.forcecomplete` | Instantly complete a quest and run reward commands               |
| `/gquests cancel [questName]`         | `gquest.cancel`        | Cancel a quest without giving rewards                            |
| `/gquest reload`                      | `gquest.reload`        | Reload the plugin configuration                                  |

---

## Placeholders

These can be used in messages to display quest data:

| Placeholder                | Description                                  |
|---------------------------|----------------------------------------------|
| `%gquest_name%`           | The display name of the quest                |
| `%gquest_type%`           | The type of quest                            |
| `%gquest_amount_required%`| The amount required to complete the quest    |
| `%gquest_progress%`       | The quest progress bar                       |
| `%gquest_percent%`        | Completion percentage of the quest           |
| `%gquest_time_remaining%` | Time remaining on the quest                  |
| `%gquest_leader%`         | Player who contributed the most              |
| `%gquest_leader_amount%`  | Amount the leading player contributed        |

---

## Config Example

You can view a sample configuration file here:  
🔗 [GlobalQuests Config YAML](https://github.com/developedbyalex/GlobalQuests/blob/main/config.yml)

---

## Message Ideas
![image](https://github.com/user-attachments/assets/be7f6854-2265-4a94-98e1-9a87261c7cf7)
![image](https://github.com/user-attachments/assets/aabc4930-9c93-43f4-a790-29369cce5c1a)
![image](https://github.com/user-attachments/assets/410eac44-b1a1-4f06-9460-fc323736b4ef)
![image](https://github.com/user-attachments/assets/29aa2ba5-53d3-4628-abbe-8e2c642f5fb1)

_Note that centered messages are a must. If you don't know how to do this, please do not quote for the plugin._

---

## Miscellaneous

- All commands support tab completion for ease of use.
- Plugin includes **resell rights**.
- No external database needed — just drop it in and go!
