![](https://img.shields.io/github/downloads/zakriamansoor47/SLAYER_Football/total?style=for-the-badge)

# Accepting Paid Request! Discord: Slayer47#7002
# Donation
<a href="https://www.buymeacoffee.com/slayer47" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a>

## Description:
This plugin allows you to play Football in CS2. Match can be started both manually and automatically. It is customizable and you can run it with your own Football maps too.

**Thanks to [Moooniz](https://github.com/MooonizYT), for making his custom plugin PUBLIC (without source code)  for CS2 Community**

## Gameplay:
https://www.youtube.com/watch?v=yfltZoMH2Ts

## Installation:
**1.** First download this map to your server: [CS2 Football Map](https://steamcommunity.com/sharedfiles/filedetails/?id=3238565662) 

**2.** Then download this plugin and add it to your server (don't replace **cfg** folder).
- **addons**

**3.** Change the Map **or** Restart the Server.

**4.** Now it's time to add some important ConVars to your **sever.cfg** file
```
//-------------------------------
// Need For CS2 Football Plugin
//-------------------------------
mp_autoteambalance 1
mp_limitteams 1
mp_startmoney 0
mp_buytime 0
mp_timelimit 0
mp_fraglimit 0
mp_freezetime 1
mp_maxrounds 500
mp_winlimit 0
mp_warmuptime 0
mp_forcecamera 0 
mp_solid_teammates 1

// Bot Stuff
bot_add
bot_quota 4
bot_quota_mode "fill" 
bot_allow_grenades 0
bot_auto_follow 0
bot_auto_vacate 1
bot_chatter "off"
bot_difficulty 3
bot_join_after_player 1
bot_join_team "any"
bot_walk 0
bot_knives_only 1
bot_defer_to_human_goals 1 // This command prevents bots from doing scenario tasks when it is set on
bot_defer_to_human_items 1 // This console command prevents bots from taking scenario items when it is set on.

```

**5.** Edit the JSON file to your own Settings. (Follow the guidelines given in the JSON file)


## Somethings you need to remember when creating Football maps for this Plugin:
Create these Entities for football maps by these names **ONLY**

```js
---------------------
Entity - Entity Name
---------------------
Football - 'BALL'
Terrorist Side Goal Post - 'CTGOAL'
C-Terrorist Side Goal Post - 'TGOAL'
```


## Commands:
`!startgame` - Start the Football game with Specific Goals Manually (For Admins with Specific Flag)

`!check` - Print the current Map and Position of the Player. Useful when you add configuration of new Map in JSON file. (For Admins with Specific Flag)

## Configuration:
```
// This configuration was automatically generated by CounterStrikeSharp for plugin 'SLAYER_Football', at 2024/06/22 08:37:27
{
  "FB_PluginEnabled": true,
  "FB_AutostartEnabled": true,            // Autostart Match Enabled in all maps? (true = Yes, false = No)
  "FB_AdminFlagToUseCMDs": "@css/root",   // Who has access to use commands?
  "FB_MapSettings": [
    {
      "MapName": "field",           // Enter the Map name for which these settings for
      "ScoreboardEnabled": true,    // Enable the Scoreboard in Map? (true = Yes, false = No)
      "MaxPlayersInEachTeam": 5,    // How many players are allowed in Each team in this Map?
      "PlayersNeedForAutoStart": 2, // How many players needed to auto-start the game?  (0 = Disable Autostart for this Map)
      "GoalsNeedToWin": 7,          // How many Goals are needed to Win the Game?
      "CT_Spawns":  [               // CT Spawn Points in this Map
        {
          "CT_SpawnPoint_1":  "30.00 -300.00 -185.48",    // Center (next to ball) | NOTE: Always set players spawn position from Center to Goal Position
          "CT_SpawnPoint_2":  "210.00 -470.00 -185.48",   // Mid-Forward-left
          "CT_SpawnPoint_3":  "210.00 -300.00 -185.48",   // Mid-Forward-Center
          "CT_SpawnPoint_4":  "210.00 -130.00 -185.48",   // Mid-Forward-Right
          "CT_SpawnPoint_5":  "450.00 -470.00 -185.48",   // Mid-Back-left
          "CT_SpawnPoint_6":  "450.00 -300.00 -185.48",   // Mid-Back-Center
          "CT_SpawnPoint_7":  "450.00 -130.00 -185.48",   // Mid-Back-Right
          "CT_SpawnPoint_8":  "650.00 -300.00 -185.48",   // Goal Position
          "CT_SpawnPoint_9":  "",
          "CT_SpawnPoint_10":  "",
          "CT_SpawnPoint_11":  ""
          // Add more Spawn Points if you need
        }
      ],
      "T_Spawns":  [
        {
          "T_SpawnPoint_1":  "-90.00 -300.00 -185.48",    // Center (next to ball) | NOTE: Always set players spawn position from Center to Goal Position
          "T_SpawnPoint_2":  "-270.00 -130.00 -185.48",   // Mid-Forward-left
          "T_SpawnPoint_3":  "-270.00 -300.00 -185.48",   // Mid-Forward-Center
          "T_SpawnPoint_4":  "-270.00 -470.00 -185.48",   // Mid-Forward-Right
          "T_SpawnPoint_5":  "-510.00 -130.00 -185.48",   // Mid-Back-left
          "T_SpawnPoint_6":  "-510.00 -300.00 -185.48",   // Mid-Back-Center
          "T_SpawnPoint_7":  "-510.00 -470.00 -185.48",   // Mid-Back-Right
          "T_SpawnPoint_8":  "-710.00 -300.00 -185.48",   // Goal Position
          "T_SpawnPoint_9":  "",
          "T_SpawnPoint_10":  "",
          "T_SpawnPoint_11":  ""
          // Add more Spawn Points if you need
        }
      ],
      // Configure Scoreboard according to the Map
      "Scoreboard_1": [
        {
          "MessageText":  "BEST OF\n{0:D2}",            // Text Message (Note: Just Change the 'Best of' text | '{0:D2}' represents total Goals Target)
          "FontName": "Arial",                          // Font of the Text
          "FontSize": 20,                               // Font Size of the Text
          "HexColor": "#FFFFFFFF",                      // Color of the Text
          "Position": "-41 -929 130",                   // Position of the Text
          "Rotation": "0 180 90"                        // Rotation of the Text
        }
      ],
      "Scoreboard_2": [
        {
          "MessageText":  "{0:D2}           {1:D2}",    // Note: Only Adjust Spaces between {0:D2} and {1:D2}
          "FontName": "Arial",
          "FontSize": 30,
          "HexColor": "#FF3CB371",
          "Position": "-39 -929 60",
          "Rotation": "0 180 90"
        }
      ]
      // Don't add any more Scoreboards, they won't work
    }
    // Add more Maps here
  ],
  "ConfigVersion": 1
}
```
