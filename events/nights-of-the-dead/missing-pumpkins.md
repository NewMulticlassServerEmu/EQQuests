# Missing Pumpkins (EverQuest live, Nights of the Dead 2021): research for an EQEmu rebuild

Researched 2026-10-05. Web research only. Raw page dumps and images are in `scratchpad/notd/raw/`.

## Sources
- **[ZAM-Q]** Allakhazam quest page: https://everquest.allakhazam.com/db/quest.html?quest=10492
  - Current version: modified 2026-05-27, "Revamped by iventheassassin".
  - 2024 Wayback copy: http://web.archive.org/web/20240521072010/https://everquest.allakhazam.com/db/quest.html?quest=10492
  - Submitted by Cylius & Laurana. Entered 2021-10-14.
- **[ZAM-NPC]** Allakhazam NPC pages:
  - Arlien Browch: https://everquest.allakhazam.com/db/npc.html?id=56789
  - Minda: https://everquest.allakhazam.com/db/npc.html?id=57247
  - Tukk: https://everquest.allakhazam.com/db/npc.html?id=57246 (2022 Wayback copy: http://web.archive.org/web/20220116200946/https://everquest.allakhazam.com/db/npc.html?id=57246)
- **[ZAM-I]** Allakhazam item pages, ids 153143-153149 (pumpkins and the Fabulous Stack) and 140854 (Ghastly Gummy Bears). These are ZAM's internal ids, not live item ids.
- **[EQR]** EQ Resource quest page: https://special.eqresource.com/missingpumpkins.php
  - Map and screenshot images: https://special.eqresource.com/expacimages/missingpumpkins.jpg and missingpumpkins1.jpg through missingpumpkins12.jpg.
- **[EQR-I]** EQ Resource item pages. These carry the LIVE item ids from the "Advanced Loot" line: https://items.eqresource.com/items.php?id=106473 through 106479, and 94095.
- **[EQR-A]** EQ Resource achievement page: https://achievements.eqresource.com/achievements.php?id=200130
- **[BONZZ]** https://www.bonzz.com/nightsofthedead.htm (section "MISSING PUMPKINS (2021 #1)").
- **[EQNEWS]** https://www.everquest.com/news/nights-of-the-dead-2021
- **[MAPS]** Local map files (read-only):
  - `C:\Git\test\EverQuest Clients\EverQuest - THJ Client - Untouched\thj-client\maps\*_1.txt`. This is a third-party map pack with labels for the live NotD 2021 objects.
  - `...\EverQuest - Live Client\maps\` and `...\EverQuest - RoF2 Client\maps\`. These hold the zone geometry used to check which zone version applies.

## 0. Coordinate convention (read this first)
- ZAM, EQR and BONZZ all write coordinates as "/waypoint A, B[, C]". **These numbers are in /loc order: A = Y, B = X, C = Z.**
- Proof 1: ZAM gives Tukk at "-3688.80, -7675.90, +3.10". The RoF2 and THJ map labels put Tukk at map point (7675.7, 3685.3). Map files store (-X, -Y), so the map gives X = -7675.7 and Y = -3685.3. That only matches if the ZAM numbers are (Y, X).
- Proof 2: I rendered each zone's live map geometry and plotted the pumpkin coordinates as (Y, X). Every point lands exactly where EQR's numbered map markers are. This held for all 7 locations (6 pumpkins plus Arlien).
- **For EQEmu (x, y, z): x = second number, y = first number.**

## 1. Dialogue (verbatim from [ZAM-Q])
- Text is kept exactly as the source has it, typos included ("fro", "prizing-winning").
- Keywords are shown with ZAM's 2024 bracket style `[harvest more]`. The 2026 ZAM page writes `[ harvest more ]` with spaces.

### Arlien Browch: hail chain and task assignment
```
You say 'Hail, Arlien Browch'
Arlien Browch says, 'Hello to you too. Um. You haven't seen [ any pumpkins ] around here, have you?
You say, 'Pumpkins? No, I haven't seen any pumpkins around here.'
Arlien Browch says, 'Yes, my pumpkins. I have been growing them all year fro the Nights of the Dead [ celebration ].'
You say, 'Oh? Where are you holding your celebration this year?'
Arlien Browch says, 'I have been invited out to Minda and Tukk's farm. Do you know them? They have a [ nice farm ] out in the Western Plains of Karana.'
You say, 'If they have a nice farm why the pumpkins?'
Arlien Browch says, 'Yes. My pumpkins. I love them and grow them all over. I have the best most perfect different types [ of pumpkins ].'
You say, 'Where are all your different types of pumpkins?'
Arlien Browch says, 'I don't Know! I woke up this morning, and they were all gone. It was like they grew legs and ran off. Why [ would they ] do that?'
You say, 'I don't know. How would they have done that?'
Arlien Browch says, 'I don't know. Could you do something for me? Could you go to my precious pumpkin patches and [ harvest more ] pumpkins?'
You say, 'I could go harvest more pumpkins for you.'
 You have been assigned the task 'Missing Pumpkins'.
Arlien Browch says, 'Great, you can go to my pumpkin patches, and I will keep looking for my missing pumpkins.'
```
How the chain works:
- Live uses the RoF+/modern "say-link" style. Clicking a bracketed keyword makes the player speak a full sentence; the "You say" lines above are those sentences.
- The trigger keyword is the text inside the brackets.
- [EQR] lists the "Request Phrase" as **harvest more**. BONZZ also says "just try saying, 'Harvest More,' to get this task".

Task description, as shown in the task window ([ZAM-Q]):
> Arlien Browch's prizing-winning pumpkins have gone missing. She is traveling to Minda and Tukk's farm, in the Western Plains of Karana, to help them celebrate their ancestors these Nights of the Dead.
> Arlien needs you to go to her special pumpkin patches and harvest replacement pumpkins, while she continues to look for her lost pumpkins.

### Arlien: each pumpkin hand-in (steps 7-12)
All six hand-ins give the same line:
```
Arlien Browch says, 'Wow. Well, it's not perfect, but it's nice.'
Your task 'Missing Pumpkins' has been updated.
```
- Each pumpkin is its own task step, so one or several can be handed in per trade.
- BONZZ says "give him the six (6) pumpkins". It calls Arlien "him", which is wrong; she is female.

### Arlien: [delivered pumpkins] (step 13; "a hail does not work")
```
You say, 'delivered pumpkins'
Arlien Browch says, 'My pumpkins? No, I am still looking. Hey, do you think you [could deliver] my replacement pumpkins to Tukk?'
You say, 'I could deliver the pumpkins.'
You have been given: Fabulous Stack of Pumpkins
Your task 'Missing Pumpkins' has been updated.
Arlien Browch says, 'Great, head to the Western Plains of Karana. The farm is along the river's edge.'
```
- ZAM 2024 lists "Your task ... has been updated" both after the item and after her last line.
- The 2026 page shows only " You receive Fabulous Stack of Pumpkins . ".
- Step 13 completes on saying "delivered pumpkins". Whether step 13 completes on that phrase or on "could deliver" is not stated separately: **UNKNOWN**. The item is given on "could deliver".

### Tukk: hand-in of the Fabulous Stack of Pumpkins (step 15)
```
Tukk says, 'Thank you for these pumpkins. I know right where they will go. You should talk with Minda and let her know that the pumpkins have been delivered.'
Your task 'Missing Pumpkins' has been updated.
```
Tukk's hail is his classic, non-event text ([ZAM-NPC] 2022 copy):
```
You say, 'Hail Tukk'
Tukk says 'Grand to meet you! I hope you have come to help out around here. Nah!! You don't have the look of a farmer.
You say, 'Are you a follower of Karana ?'
Tukk says 'Yes. I am a follower of Karana, the Rainkeeper. It is He who keeps the plains fertile.'
```
- Note: the ZAM page has a [Karana bandits] reply attributed to "Rongol", not Tukk. It is probably copied from another NPC.

### Minda: [delivered pumpkins] (step 16, the completion; "a hail does not work")
```
You say, 'delivered pumpkins'
Minda says, 'That is great news! Now maybe [Grandfather Hule] will stop bothering us.'
You say, 'Grandfather Hule?'
Your task 'Missing Pumpkins' has been updated.
 (completion text:) You helped harvest replacement pumpkins for Arlien and delivered them for her. Minda and Tukk were grateful that you gathered the pumpkins to help them celebrate their ancestors.
Minda says, 'Yes, my great-great-grandfather has been pestering us about the celebration. I have a great idea, why don't you [go speak] with him so we can get set up?'
You say, 'Sure, I can go speak with him.'
```
- ZAM: "(Note: this last line is likely just a lead-in line to direct you to the 'Carving pumpkins' task.)"
- The next task, Carving Pumpkins, is given by **Hule C. Zarschl** in West Karana. BONZZ puts him "near a hut in the area of /waypoint -3715, -7665 (he is on Find)", with request phrase "Few Tasks". [EQR-A] spells him "Hule C. Zarshcl".
- No reply to "go speak" is recorded anywhere: **UNKNOWN / probably none**.

### Not found (UNKNOWN)
- Minda's plain hail text, both event and classic.
- What Arlien says on hail while the task is already active or after it is finished.
- What Arlien says when given a wrong item.
- Any reply to "go speak".

## 2. NPCs
| NPC | Zone (live) | Location | Race / gender | Level | Notes |
|---|---|---|---|---|---|
| Arlien Browch (title "Nights of the Dead Quests") | **The Commonlands = merged zone `commonlands`** ([EQR] "The Commonlands"; ZAM zone "Commonlands") | No coordinates in any web source; ZAM says "/waypoint 000 in the Commonlands tunnel". THJ map label `commonlands_1.txt`: `P 2337.2061, 1664.7727, 28.6787 ... Arlien_Browch_(Nights_of_the_Dead_Quests)`, which is **/loc -1664.8, -2337.2, 28.7, so EQEmu x=-2337.2 y=-1664.8 z=28.7** | Gnome, female (screenshot; quest text says "her"/"she") | 30 (ZAM) | Not attackable, faction None, body type Humanoid. ZAM says added 2021-09-11, expansion icon "Original". |
| Minda (title "Nights of the Dead Quests") | West Karana (`qey2hh1`) | ZAM: "/waypoint 000" (none given). Map labels: RoF2 `qey2hh1_2.txt` `P 7697.3652, 3736.5310, -2.2520` and THJ `qey2hh1_1.txt` `P 7692.9727, 3735.7080, -2.2398`, which is **/loc ~-3736, -7693, -2.2 (EQEmu x=-7693 y=-3736 z=-2.2)** | Human, female (screenshot) | 6 | Not attackable. This is an existing classic WK farm NPC; the RoF2 map pack already labels her, and ZAM tags her expansion as CoV. |
| Tukk (title "Nights of the Dead Quests") | West Karana (`qey2hh1`) | ZAM: "-3688.80, -7675.90, +3.10 in front of a barn" (/loc order), so **EQEmu x=-7675.9 y=-3688.8 z=3.1**. Map labels: RoF2 `P 7667.0, 3680.3, -1.46`; THJ `P 7675.71, 3685.33, -1.53` | Human, male (screenshot: bald, black vest, red trousers, boots) | 7 | Not attackable. "Findable (via Ctrl-F): No". Existing classic NPC with classic hail text. |

Where exactly Arlien stands:
- She is in the **tunnel at the south-east of the merged Commonlands, the passage that leads to Nektulos Forest**. Her spot is where that tunnel opens into the small side chamber.
- BONZZ: "in the tunnels at the vendor / NPC area".
- The ZAM map screenshot (red dot) and EQR's map (missingpumpkins.jpg) both show the same spot. My plot of the THJ label on the live `commonlands.txt` geometry lands there too.
- The exact coordinate comes only from a third-party map label: **treat it as close, not authoritative**.

Screenshots (zam.zamimg.com):
- Arlien:
  - Model: https://zam.zamimg.com/images/4/7/47c75f81988711e99e5bd003bce98308.jpg (female gnome, dark-red hair, light tunic with brown vest, belt pouch, dark knee breeches, white socks, brown shoes; holds a small yellow item/wand)
  - Map: https://zam.zamimg.com/images/4/d/4d3e60b5140054765495a9971e769634.jpg (red dot in the Commonlands-to-Nektulos tunnel)
- Minda:
  - Model: https://zam.zamimg.com/images/8/e/8e9b347c2f7463ca9eb419be114c4131.jpg (white hair, blue top with white collar, brown knee breeches, black shoes)
  - Map: https://zam.zamimg.com/images/e/f/ef285a035e52513053e0abf9cbbb3cc8.jpg (WK map, red dot at the south river edge, middle of the zone)
- Tukk:
  - Model: https://zam.zamimg.com/images/9/8/989da04301aefbc5c1b18ae81c161ba0.jpg
  - Map: https://zam.zamimg.com/images/6/b/6bb0aa8c31f26bad998d8f70f4fc107f.jpg
- BONZZ also has NPC images at https://www.bonzz.com/graphics/npc/Arlien%20Browch.jpg, .../Tukk.jpg and .../Minda.jpg.

Not found (UNKNOWN):
- Exact race id, texture, face or hair values; equipment tints; heading; class.
- Live run speed or pathing. Nothing suggests any NPC moves.

## 3. Pumpkin ground spawns
All six are ground spawns ([ZAM-I]: "This item is a ground spawn."). The model is a small pumpkin; see the EQR close-ups missingpumpkins1/3/5/7/9/11.jpg (one per zone).

| Step | Item | Zone (live shortname / version) | Web coords (/loc order Y, X[, Z]) | Map-label exact point, converted to EQEmu x, y, z | Step text in the task window ([ZAM-Q]) |
|---|---|---|---|---|---|
| 1 | Dreadful Pumpkin | Nektulos Forest, `nektulos`, **the Depths of Darkhollow revamp** (ZAM "Nektulos Forest 3.0"). THJ label file is named `nektulos_1_dodh.txt`. The RoF2 client's nektulos map has the same geometry as the DoDH map, so RoF2 already has this version. | ZAM 900, -820; BONZZ 880, -820 | x=-819.4, y=889.6, z=12.1 | "In Nektulos Forest, under a tree toward the North East a dreadful pumpkin grows." |
| 2 | Haunted Pumpkin | Kithicor Forest, `kithicor`, **classic geometry**. The live `kithicor.txt` map matches EQR's map; the separate `oldkithicor` map does not apply. | ZAM 636, 2193; BONZZ 645, 2170 | No map label found. **x=2193, y=636, z UNKNOWN** | "In Kithicor Forest, under a large tree near a burned-out farm, a haunted pumpkin grows." BONZZ: "south of the road, mid-zone, by a tree". |
| 3 | Perfectly Ripe Pumpkin | Misty Thicket: **the REVAMPED Misty Thicket (`mistythicket` geometry; ZAM "Misty Thicket 2.0")**, not classic `misty`. EQR's map image matches `mistythicket.txt` exactly; plotted on classic `misty.txt` the point falls in the wrong place. | ZAM -310, -138; BONZZ -310, -145 | label in `mistythicket_1.txt`: x=-132.5, y=-309.4, z=1.6 | "In Misty Thicket, a perfectly ripe pumpkin grows under a large tree near a well-cared-for home." BONZZ: "behind the hut near the PoK Book". |
| 4 | Frozen Pumpkin | Everfrost Peaks, `everfrost`, classic | ZAM/EQR 1665, 240, -60 (an early comment wrongly gave "1665, -60") ; BONZZ 1670, 250 | x=248.2, y=1661.7, z=-62.3 | "In Everfrost Peaks, under a tree in a small hollow toward the northwest, a pumpkin has frozen on the vine." BONZZ: "south from Halas, first dead-end on the left, by a tree". |
| 5 | Overripe Pumpkin | West Karana, `qey2hh1`, classic | ZAM 1330, -2060; BONZZ 1335, -2035 | x=-2046.8, y=1337.4, z=81.7 | "In West Karana, behind the small village to the northwest and under a tree, an overripe pumpkin has been forgotten." |
| 6 | Rotten Pumpkin | The Feerrott, `feerrott`, **classic** (not `feerrott2`, "The Feerrott: The Dream"). EQR's map shows the classic Feerrott with Cazic Thule. | ZAM 1011.6, -1985, -29 (comment by Merf: 1013.53, -1987.75); BONZZ 1010, -1980 | x=-1985.2, y=1011.4, z=-33.5 | ZAM: "In the Feerrott, toward the northeast." Players said the 2021 in-game text read "southeast of the temple" and that this was wrong; the pumpkin is in the far NE. Which wording live uses now: **UNKNOWN**. |

RoF2 client check for a rebuild:
- The RoF2 client folder has `mistythicket.eqg` and **no `misty.s3d`** (only `misty_chr.s3d` and the sound files).
- Check which shortname or version your server uses for Misty Thicket before placing the spawn. The live point only makes sense on the revamped geometry.

Not found (UNKNOWN):
- Ground-spawn respawn timer.
- Whether the spawns are visible to everyone or only to people on the task (on live they are ordinary ground spawns; no source says they are task-gated).
- Max per spawn point.
- The Kithicor Z value.

## 4. Farm auto-update, the Fabulous Stack, and the Tukk turn-in
Step 14, "Travel to Minda and Tukk's farm in West Karana", is an explore/auto-update step:
- ZAM: "a location in the area of -3606, -7678 (the Barnes at mid-zone, near the water at the dead end road)". That is **EQEmu x=-7678, y=-3606**.
- BONZZ: "/waypoint -3605, -7680 (the barns at mid-zone, near the water at the dead end road), for a location update."
- Z, radius and box size: **UNKNOWN**. Ground near Tukk and Minda is z ≈ -2 to +3.
- EQR's map marker 7 on missingpumpkins9.jpg is at the south river edge, middle of the zone. That agrees with Arlien's line "The farm is along the river's edge."

The **Fabulous Stack of Pumpkins** is handed to the player by Arlien in step 13, right after "could deliver". ZAM lists it under "Items Given" on her NPC page and says "This item is obtained from NPCs."

Step 15: hand the Fabulous Stack to **Tukk**. His reply is in section 1.

Step order:
- The steps are listed in sequence (1-6 harvest, 7-12 deliver, 13 talk, 14 travel, 15 deliver, 16 talk).
- Whether steps 1-6 and 7-12 can be done in any order was not stated. Each hand-in is its own step, so they are probably unordered within each group (**UNKNOWN**).

## 5. Items
Flags come from [EQR-I]; ZAM agrees: "Lore Item Quest Item", WT 0.1, SMALL, Stackable: No, Item Type Misc, Class NONE / Race NONE.
- None of them carries NO TRADE, and none is listed as temporary (EQR shows only "Magic, Lore, Quest").
- Merchants won't buy or sell any of them ("Not Sellable / Not Buyable").
- Stack size is 1 for all.

| Live id | ZAM id | Name | Icon | Lore text (item info, verbatim) |
|---|---|---|---|---|
| 106473 | 153143 | Dreadful Pumpkin | 3246 | This dreadful pumpkin has grown extremely disagreeable in the wilds of the Nektulos Forest. Be careful, it may bite! |
| 106474 | 153144 | Haunted Pumpkin | 1481 | This haunted pumpkin sends chills down your spine, and an intense feeling of being watched invades your thoughts. Perhaps a salt circle would help? |
| 106475 | 153145 | Perfectly Ripe Pumpkin | 1696 | This pumpkin has grown ripe with a pleasing pumpkin color. The fields of Misty Thicket have been kind. It would be a shame if anything happened to this specimen. |
| 106476 | 153146 | Frozen Pumpkin | 3245 | This frozen pumpkin has a satisfying thunk when tapped. It should be fun to carve, but you are unsure how it grew in the snow-covered hills of Halas. |
| 106477 | 153147 | Overripe Pumpkin | 2029 | This soft pumpkin will not be long for this world. Perhaps a quickened paced to see it back to Arlien would be wise. |
| 106478 | 153148 | Rotten Pumpkin | 1698 | This pumpkin has rotted in the fetid swamp of the Feerrott. You are not sure what it could be used for, except to feed it to the Dreadful Pumpkin. |
| 106479 | 153149 | Fabulous Stack of Pumpkins | 1691 | Arlien has carefully packed her second-choice pumpkins to be presented to Minda and Tukk, and they are ready for delivery. This collection of pumpkins would make any collector proud. |
| 94095 | 140854 | Ghastly Gummy Bears (reward) | 1690 | see section 6 |

Note: icon numbers are EQR/ZAM icon file numbers (item_NNNN.png). The in-game icon id is assumed to be the same, but that is not verified.

Ground-spawn object model ids (for EQEmu `ground_spawns.name` like IT###): **UNKNOWN**. The screenshots show the small pumpkin model in every zone.

## 6. Rewards
**5x Ghastly Gummy Bears**, live id 94095 ([EQR], [ZAM-Q], [EQR-I], [ZAM-I]):
- Food, "This is a miraculous meal! (90)", so food duration 90.
- AC 155, HP +1200, Mana +950, End +600.
- Required level 100. Tribute 600. Size SMALL, weight 0.5. Stack 20.
- Merchant value 1 cp. Class ALL, Race ALL.
- No Lore, No NO TRADE, no Magic flag shown.
- **No click effect**: it is stat food, not a clicky.
- Also a reward from "The Witch's Wishes" and "Squashing Pumpkins".

Conflicting reports:
- BONZZ says the reward window offered a choice of Ghastly Gummy Bears **or** Ominous Orangeade. Ominous Orangeade is live id 94097: drink, AC 155, HP 1200, Mana 1200, End 400, req 100, tribute 240.
- EQR lists Ominous Orangeade as a reward of Carving Pumpkins and Squashing Pumpkins, **not** of Missing Pumpkins.
- ZAM and EQR list only 5x Gummy Bears for this quest. **Treat Gummy Bears as the reward**; the Orangeade choice is unconfirmed.

Progression (TLP) servers:
- A ZAM comment from 2022 says a character "in TBS expansion" got **5x Eerie Jelly Beans** instead.
- Eerie Jelly Beans are live id 94094: enduring meal (60), AC 10, HP 250, Mana 200, End 300, Rec level 90, Corruption 5.
- So live scales or swaps the food by server era.

Achievement: **Nights of the Dead: Magnificent Winter Squash** (EQR-A id 200130; ZAM quest 10521):
- 10 points. Category Events > Holiday. Not a world achievement.
- Achievement reward: "AA (Scales to Level)" and "Experience".
- Objectives: complete Missing Pumpkins (Arlien Browch), Carving Pumpkins (Hule C. Zarshcl, WK) and Squashing Pumpkins (Levy Cullpay, WK).
- Completing Missing Pumpkins alone only advances the achievement.

Experience from the task itself:
- ZAM 2026 tags the quest goal "Advancement / Loot" and the search index says "Advancement,Loot Quest".
- **No task XP amount is listed anywhere: UNKNOWN.** Advancement probably refers to the achievement.

## 7. Repeatable, lockout, level, group
| Property | Value | Source |
|---|---|---|
| Repeatable | **Yes**. A 2022 comment: "You can do this quest line multiple times". | ZAM-Q, EQR |
| Replay timer / lockout | None listed; EQR shows "Time Limit: Unlimited". A replay timer is **UNKNOWN**: not stated, none mentioned. | EQR |
| Task type | **Solo** (EQR "Task Type: Solo"; ZAM "Group Size: Solo") | EQR, ZAM-Q |
| Level | ZAM: Level 1, Maximum Level 125 (2024), raised to 130 (2026). The reward food requires level 100, so low-level characters get an item they cannot use yet (or the TLP swap). | ZAM-Q |
| Classes / races | All / All | ZAM-Q |
| Seasonal | Nights of the Dead only. 2021 event: Oct 13, 2021 12:00 a.m. PDT to Nov 9, 2021 11:59 p.m. PDT ([EQNEWS]). | ZAM-Q, EQNEWS |
| Lore context | [EQNEWS]: "Minda and Tukk of the Western Plains of Karana are hosting a celebration for their ancestors. They have hired pumpkin farmer Arlien Browch to deliver a large supply of pumpkins. She has been seen heading towards the Commonlands, on her journey towards Minda and Tukks farm." / "It seems that she has been a bit unlucky and has been having some trouble controlling her squashes." | EQNEWS |

## Task step list (exact live wording, from EQR)
1. Harvest a dreadful pumpkin from Nektulos Forest 0/1 (Nektulos Forest)
2. Harvest a haunted pumpkin from Kithicor Forest 0/1 (Kithicor Forest)
3. Harvest a perfectly ripe pumpkin from Misty Thicket 0/1 (Misty Thicket)
4. Harvest a frozen pumpkin from Everfrost Peaks 0/1 (Everfrost Peaks)
5. Harvest an overripe pumpkin from West Karana 0/1 (The Western Plains of Karana)
6. Harvest a rotten pumpkin from the Feerrott 0/1 (The Feerrott)
7. Deliver the dreadful pumpkin to Arlien 0/1 (The Commonlands)
8. Deliver the haunted pumpkin to Arlien 0/1 (The Commonlands)
9. Deliver the perfectly ripe pumpkin to Arlien 0/1 (The Commonlands)
10. Deliver the frozen pumpkin to Arlien 0/1 (The Commonlands)
11. Deliver the overripe pumpkin to Arlien 0/1 (The Commonlands)
12. Deliver the rotten pumpkin to Arlien 0/1 (The Commonlands) (ZAM's "Deliver the dreadful rotten to Arlien" is a ZAM typo)
13. Speak with Arlien about her [delivered pumpkins] 0/1 (The Commonlands)
14. Travel to Minda and Tukk's farm in West Karana 0/1 (The Western Plains of Karana)
15. Deliver the Fabulous Stack of Pumpkins to Tukk 0/1 (The Western Plains of Karana) (ZAM writes "Fabulous Stack of pumpkins")
16. Speak with Minda about [delivered pumpkins] 0/1 (The Western Plains of Karana)

## Consolidated UNKNOWNS (not found anywhere; do not guess)
- Arlien's exact live coordinates from a first-hand web source. The only exact point is the third-party THJ map label, which agrees with both screenshot maps.
- Minda's exact live coordinates from a web source. Only map-pack labels exist.
- Kithicor pumpkin Z.
- Farm auto-update Z and radius.
- Ground-spawn respawn time, model ids, and whether a task gate exists.
- Hail text for Minda, event or classic.
- Arlien's reply on hail when the task is active or finished, and her reply to wrong items.
- Any reply to "go speak".
- Whether the in-game Feerrott step text now says NE or still says SE.
- Task XP, if any.
- Replay timer (none is listed).
- Reward choice: Gummy Bears only (ZAM/EQR) vs Gummy Bears or Ominous Orangeade (BONZZ, unconfirmed).
- Exact NPC appearance values (race id, texture, helm, face, hair, tints) and the classes of Minda and Tukk.
