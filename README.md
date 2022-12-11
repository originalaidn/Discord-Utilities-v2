# [Join the DU discord server for latest binary and support](https://discord.gg/WCNjEDPD2v)

## Requirements to run these plugin(s)
**-** [**New Discord API Plugin**](https://github.com/Cruze03/discord-api/blob/main/discord_api.smx) (Remove the [old one](https://github.com/Cruze03/sourcemod-discord/blob/master/discord_api.smx) to avoid conflicts) (**Please restart server when first added / when new version added**)

## Main Module
- This is needed for all the other modules.
- Consists how to retrieve and store data to config.

## Server Details Module
- Open `addons/sourcemod/configs/DiscordUtilitiesv2.txt`
- Fill up the `key` in `BOT_TOKEN` section with your **BOT's Token Key**.
- Fill up the `map_thumnail` in `WEBHOOK_SETTINGS` section with your **Custom Map Thumbnail URL**.
- Fill `map` in `CHANNEL_IDS` section with your server details **Channel ID**.
- Fill up the `server_dns_name` in `WEBHOOK_SETTINGS` section with your **Custom DNS** or leave it empty to use regular public IP.
- Add `addons/sourcemod/translations/du_serverdetails.phrases.txt` in your server.
- Type `sm_du_refresh` in your in-game client console.

![Server Details](https://cdn.discordapp.com/attachments/756189500828549271/1051479840194314322/ServerDetails.png)

## Chat Relay Module
- Open `addons/sourcemod/configs/DiscordUtilitiesv2.txt`
- Fill up the `key` in `BOT_TOKEN` section with your **BOT's Token Key**.
- Fill up the `key` in `API_KEY` section with your [Steam API Key](https://steamcommunity.com/dev/apikey).
- Fill `chat` in `CHANNEL_IDS` section with your chat relay **Channel ID**.
- Fill `chat` in `WEBHOOKS` section with your chat relay **Webhook URL**.
- Type `sm_du_refresh` in your in-game client console.

![Chat Relay](https://cdn.discordapp.com/attachments/756189500828549271/1010851311358586931/chat_relay1.png)
![Chat Relay](https://cdn.discordapp.com/attachments/756189500828549271/1010851312038072400/chat_relay2.png)

## Verification Module
- Open `addons/sourcemod/configs/DiscordUtilitiesv2.txt`
- Fill up the `key` in `BOT_TOKEN` section with your **BOT's Token Key**.
- Fill `verification` in `CHANNEL_IDS` section with your verification **Channel ID**.
- Fill `primary` in `VERIFICATION_SETTINGS` section with '1' if it's your primary server else '0'. **(Keep this '1' only in one server)**
- Fill `serverid` in `VERIFICATION_SETTINGS` section with a **unique value**.
- Fill `guildid` in `VERIFICATION_SETTINGS` section with your **Discord Server ID**.
- Fill `roleid` in `VERIFICATION_SETTINGS` section with your verification **Role ID**.
- Fill `invite_link` in `VERIFICATION_SETTINGS` section with your discord server **Invite Link**.
- Fill `command` in `VERIFICATION_SETTINGS` section with the command(s) players need to type in **Discord** to link their discord. (Split multiple commands with **',{space}'**)**(Max 5)**
- Fill `command_ingame` in `VERIFICATION_SETTINGS` section with the command(s) players need to type **In-Game** to get their verification code. (Split multiple commands with **',{space}'**)**(Max 5)**
- Fill `blocked_commands` in `VERIFICATION_SETTINGS` section with the command(s) players cannot access without verifying their discord. (Split multiple commands with **',{space}'**)**(Max 64)**
- Change `use_swgm_for_blocked_commands` in `VERIFICATION_SETTINGS` section to '1' if you want to use  commands from **SWGM config file** as well.
- Fill `database_name` in `VERIFICATION_SETTINGS` section with database entry name in `configs/database.cfg`
- Fill `table_name` in `VERIFICATION_SETTINGS` section with your desired table name in the database.
- Add `addons/sourcemod/translations/du_verification.phrases.txt` in your server.
- Type `sm_du_refresh` in your in-game client console.

![Verification](https://cdn.discordapp.com/attachments/756189500828549271/1010850115101147156/verification.png)

## Bug Report Module
- Open `addons/sourcemod/configs/DiscordUtilitiesv2.txt`
- Fill up the `key` in `BOT_TOKEN` section with your **BOT's Token Key**.
- Fill `bugreport` in `WEBHOOKS` section with your bug report **Webhook URL**.
- Fill up the `server_dns_name` in `WEBHOOK_SETTINGS` section with your custom dns or leave it empty.
- Add `addons/sourcemod/translations/du_bugreport.phrases.txt` in your server.
- Type `sm_du_refresh` in your in-game client console.

![Bug Report](https://cdn.discordapp.com/attachments/756189500828549271/1051478038409383977/Bugreport.png)

## Call Admin Module
- Open `addons/sourcemod/configs/DiscordUtilitiesv2.txt`
- Fill up the `key` in `BOT_TOKEN` section with your **BOT's Token Key**.
- Fill `calladmin` in `WEBHOOKS` section with your calladmin **Webhook URL**.
- Fill up the `server_dns_name` in `WEBHOOK_SETTINGS` section with your custom dns or leave it empty.
- Add `addons/sourcemod/translations/du_calladmin.phrases.txt` in your server.
- Type `sm_du_refresh` in your in-game client console.

![Bug Report](https://cdn.discordapp.com/attachments/756189500828549271/1051478038119981127/Calladmin.png)

## Sourcebans / MaterialAdmin Module
- Open `addons/sourcemod/configs/DiscordUtilitiesv2.txt`
- Fill up the `key` in `BOT_TOKEN` section with your **BOT's Token Key**.
- Fill `bans` in `WEBHOOKS` section with your bans **Webhook URL**.
- Fill `comms` in `WEBHOOKS` section with your comms **Webhook URL**.
- Fill `reportplayer` in `WEBHOOKS` section with your sourcebans/materialadmin report **Webhook URL**.
- Fill up the `server_dns_name` in `WEBHOOK_SETTINGS` section with your custom dns or leave it empty.
- Add `addons/sourcemod/translations/du_sourcebans.phrases.txt` in your server.
- Type `sm_du_refresh` in your in-game client console.

![Sourcebans or MaterialAdmin](https://cdn.discordapp.com/attachments/756189500828549271/1051478037734113320/Sourcebans.png)

## Server Tracker Module
- This module is used for your convenience only. It helps you know which of your server is using which `serverid` & which server is `primary`.
- Fill up the `servers_table_name` in `VERIFICATION_SETTINGS` section with your desired table name for this module. (Table will be created under `database_name` database)

![Server Tracker](https://cdn.discordapp.com/attachments/756189500828549271/1051483671657455677/ServerTracker.png)

**[Recommended]** Create a password protected, less slots server (1-5) and mark that as the "primary" server. Keep these convars values to avoid map change in that server: `sv_hibernate_when_empty 0;mp_maxrounds 99999;mp_roundtime 60;mp_roundtime_defuse 60`. This is to avoid bot missing a message to delete when primary server is between changing maps.

### NOTE:
1) `map` & `verification` keys in `MESSAGE_IDS` section are automatically added with **message id** by the respective plugins. If you want to add a new message in your respective channel, just remove the id from `map` or `verification` keys in `MESSAGE_IDS` section and reload the current map.
2) Why is this not compilable in SM 1.12? [It is because of this :(](https://github.com/alliedmodders/sourcepawn/issues/671). I personally use SM 1.10 compiler
