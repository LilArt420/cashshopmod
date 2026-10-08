Ragnarok Offline - Cash Shop Rewards
====================================

What this mod does
------------------
- Expands the Cash Shop with useful scrolls and convenience items.
- Awards account-wide Cash Points for time spent online.
- Awards account-wide Cash Points after a configurable number of monster kills.
- Shows reward notifications in chat without an overhead speech bubble.
- Adds a status NPC in Prontera at 158,190.

Default rewards
---------------
- 15 points for every 15 online minutes.
- 15 points for every 100 monster kills.
- No daily earning limit.

Configuration
-------------
Open npc/points.txt and edit the values directly below the OnInit label:

  .PlayTimeEnabled = 1;
  .PlayMinutesPerReward = 10;
  .PlayTimePoints = 15;

  .KillRewardEnabled = 1;
  .KillsPerReward = 100;
  .KillRewardPoints = 15;

  .DailyPointCap = 0;
  .ShowRewardMessages = 1;

Use 1 to enable a feature and 0 to disable it. DailyPointCap = 0 means
unlimited. Restart Ragnarok Offline after changing script settings.

Shop items and prices
---------------------
Open db/item_cash.yml. Each entry uses this format:

  - Item: Blessing_10_Scroll
    Price: 5

The item value must be a valid rAthena AegisName.

The client also needs to know the item's name, description and icon. Most
items are in the client's own item table, but some iRO-only ones are not in
kRO's, and show as "Unknown Item" there. System/itemInfo.lua supplies those.
If you add an item that shows as unknown on a kRO client, add its entry there
too, using the item's numeric ID (copy it from iRO's System/iteminfo.lub).

Progress and storage
--------------------
Cash points and reward progress are account-wide and persist in the database.
The play-time counter advances once per complete online minute; logging out
cancels the running partial minute. Monster-kill progress carries over between
characters on the same account.

rAthena AegisName lists
--------------------
Consumables: https://github.com/rathena/rathena/blob/master/db/re/item_db_usable.yml
Equipment: https://github.com/rathena/rathena/blob/master/db/re/item_db_equip.yml
Miscellaneous: https://github.com/rathena/rathena/blob/master/db/re/item_db_etc.yml 