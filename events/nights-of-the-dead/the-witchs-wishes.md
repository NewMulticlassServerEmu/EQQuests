# The Witch's Wishes (EverQuest live, Nights of the Dead): research notes

Researched 2026-10-05. Web only, read-only.

## Sources and how reliable each one is

| Tag | URL | Access | Reliability |
|---|---|---|---|
| EQR-Q | https://special.eqresource.com/thewitchswishes.php | Raw HTML via curl, saved to `raw_witch/eqr.html` | Verbatim. Contains the step text and maps but no NPC dialogue. |
| EQR-I | https://items.eqresource.com/items.php?id=NNN | Raw HTML via curl, saved to `raw_witch/eqri_*.html` | Verbatim item blocks. The "Advanced Loot" line gives the real live item id. |
| EQR-A | https://achievements.eqresource.com/achievements.php?id=200115 | Raw HTML via curl | Verbatim |
| EQR-S | https://spells.eqresource.com/spells.php?id=7651 | Raw HTML via curl | Verbatim |
| ZAM-Q | https://everquest.allakhazam.com/db/quest.html?quest=9223 | curl gets **403**; read only through the WebFetch summariser | Quotes were requested one line at a time and re-checked. Treat them as near-verbatim, not guaranteed. Lines marked (S) could only be reached through the summariser and may be paraphrased. |
| ZAM-N | https://everquest.allakhazam.com/db/npc.html?id=47617 (Cikdew), ?id=755 (Mugu), ?id=47618 (Glinda), ?id=16389 (Bamrih Tyco) | Summariser | As above |
| ZAM-I | https://everquest.allakhazam.com/db/item.html?item=140855 ... 140861, 15026, 33678 | Summariser | Flags were cross-checked against EQR-I. Where they differ, EQR-I wins because it is raw. |
| EQ news | https://www.everquest.com/news/nights-of-the-dead-2021 | Summariser | Official |
| Bonzz | https://www.bonzz.com/nightsofthedead.htm | Summariser | Fan site |

Note: ZAM item ids (140854-140861, 15026, 33678) are **ZAM's own database ids**, not live ids. The live ids come from the EQR "Advanced Loot" lines and are listed in section 4.

## 0. History and context

- ZAM-Q: the quest was entered on ZAM "Sun Oct 14 10:13:57 2018" by Drewie, and its Era is shown as Ring of Scale. On the same page, hullan (Nov 2019) reports the step objective and description read only "Hi", which looks like an unfinished placeholder.
- Bonzz says the quest was broken for years and "eventually fixed in 2021". EQR lists it under the **2021** Nights of the Dead quests.
- EQ news 2021: the event ran **Oct 13 2021 12:00 a.m. PDT to Nov 9 2021 11:59 p.m. PDT**. It says: "It has been rumored that the Witch responsible for their furor has in fact found her voice. Cikdew has a new request for adventurous aides, who don't mind doing a little dirty work."
- Cikdew herself predates the quest. ZAM-N says her entry was added Oct 18 2014.

## 1. Dialogue

### Cikdew (quest giver)

ZAM-Q, from the GOMN comment, with each line quoted individually:

```
You say, 'Hail, Cikdew'
Cikdew says, 'Hello, my pretty! Have you come to [aid] this poor old woman? If not, then go away!'
You say, 'aid'
Cikdew says, 'Ah, good. You see, I am far too old and feeble to manage the difficult task at hand on my own. I need a strong young adventurer like you to help me. Surely this will be a [simple task] for one of your skills, no?'
You say, 'simple task'
Cikdew says, 'Well, you see, there are some things that can only be done during the Nights of the Dead. Some mystical items can only be gathered on these nights or they are not potent. Some magic will only work on these nights. I have need of some very special things that can only be gathered now so that I can make something of use with them. But this all must be done before the Nights of the Dead are over. I really can't explain what I seek until the time is proper, or that will break the magic. Will you [do this] for me?'
You say, 'do this'
Cikdew says, 'Very good, deary! Now, take this with you and I will be able to guide you through it.'
```

- EQR-Q gives the request phrase as `do this`.
- Assignment: the task is assigned and the player receives the **Dreadful Witch's Cauldron**. ZAM-N lists Cikdew as the source of the cauldron. The receive line was relayed as "You receive Dreadful Witch's Cauldron, a 4 slot container." (S, possibly paraphrased).
- Completion: after the brew and the mushroom are handed in, the line is:
  `Cikdew seemed pleased that you would take on a task to gather bad luck for her. You have her gratitude.`
  This reads like the task's completion text, not something Cikdew says aloud. **UNKNOWN: whether Cikdew says any line of her own on either turn-in.** No source quotes one.
- Ambient flavour line (ZAM-N and the GOMN comment). Cikdew occasionally turns Bamrih Tyco, the NPC next to her, into a frog and says: `Why are you hanging around here, fool? This is my bridge now! You and your important people. Well, those important people had better watch out for warts!` The exact trigger and timer are **UNKNOWN**.
- Other NPCs at the same spot (flavour only, no quest function):
  - **Glinda**: a cat, level 35, female per ZAM. Hail reply: `Merrrow!`
  - **Bamrih Tyco**: a stock South Karana NPC at /loc 2530, 910 (ZAM). When he is a frog his reply is `Ribbit`. His normal reply is `I'm afraid I can't speak right now, <name>. I'm waiting for someone very important to arrive.`
  - Name origins (ZAM-N): Cikdew is an anagram of "Wicked", and Glinda is the Good Witch from Oz.

### Mugu (Feerrott)

- This is the **stock** Feerrott smithing-supplies merchant. The task only adds a turn-in.
- Line, from the GOMN comment: `Mugu looks at the mirror, 'Ouch. You can have this back, I have no need for it.'` It is written as an emote, "Mugu looks at the mirror, ...". It was quoted twice the same way.
- She then gives the shattered mirror. The line was relayed as "You receive Pieces of a Shattered Mirror." (S). ZAM-N for Mugu lists "Items Given: Pieces of a Shattered Mirror".
- Mugu has no other quest dialogue or keywords in any source.

## 2. NPCs: location and appearance

**Coordinate convention.** Every coordinate below is in **/loc order (Y, X)**. GOMN labels some of his numbers "/way", but they are in /loc order. For example, his Mugu "/way 972, 1241" matches Mugu's ZAM spawn "+971, +1237" and a ZAM user's "LOC 972, 1246". For EQEmu, take x from the **second** number and y from the **first**.

| NPC | Zone | /loc (Y, X) | Level | Race / look | Gender | Screenshot |
|---|---|---|---|---|---|---|
| Cikdew | South Karana (southkarana) | +2544, +896, under the bridge to North Karana (ZAM-N) | 35 (ZAM-N) | Race id **UNKNOWN** (see below) | Female (ZAM-N) | https://zam.zamimg.com/images/6/5/656781f2b03a9a12ea111915b2a0ac26.jpg (saved as `raw_witch/cikdew_ss.jpg`) |
| Glinda (cat) | South Karana | Same spot as Cikdew (ZAM) | 35 | Cat | Female | ZAM npc 47618; screenshot URL not captured |
| Bamrih Tyco | South Karana | 2530, 910 | stock | stock | stock | ZAM npc 16389 |
| Mugu | The Feerrott | +971, +1237, just SW of the Oggok entrance by the stone huts at the river (ZAM-N, GOMN) | 5 | Ogre, smithing merchant | Female | https://zam.zamimg.com/images/8/d/8df9b3ce47a92c07b396d486c07dd733.jpg (saved as `raw_witch/mugu_ss.jpg`) |

**Cikdew's appearance**, judged from the screenshot only:
- a gaunt, pale-blue, ghostly old woman with long white hair and red eyes;
- a long dark-blue tattered gown with sleeves;
- a pentagram pendant on a chain.

It looks like a banshee or spectral-woman model, not a playable race. **No source states the race id, texture or helm.** Pick a client model that matches the screenshot.

EQR-Q map image of South Karana: https://special.eqresource.com/expacimages/thewitchswishes.jpg. It marks Cikdew at the top edge by the North Karana bridge, and marker "4" at the centaur village in the NE.

## 3. Task steps (live objective text verbatim from EQR-Q)

General task data (EQR-Q and ZAM-Q):
- Task name as shown in update messages: `Your task 'Witch's Wishes has been updated.` This is quoted by GOMN, apostrophe oddity included. The EQR title is "The Witch's Wishes", and the reward line is `You have successfully been granted your reward for: The Witch's Wishes`.
- Task Type: **Solo**
- Time Limit: **Unlimited**
- Repeatable: **Yes**
- Level range: ZAM says 1-130 ("1-125" in an older snapshot) for all classes and races. The rewards themselves need level 100 to use.
- Seasonal: Nights of the Dead only. The last step's wording, "before Nights of the Dead end", makes this explicit.
- GOMN tip: Rock Salt and Candied Spider can be made or bought beforehand, because the "Find" steps update on items you already hold.

| # | Objective (verbatim) | Zone | How it updates |
|---|---|---|---|
| 1 | Find a lost mirror near the entrance to the Erudin Palace 0/1 | Erudin | Location update that puts the **Lost Mirror on your cursor**, shown as "You have been given: Lost Mirror" (S). Spot: ZAM walkthrough and Lost Mirror item page say /loc **-700, -130**, on the grass near Demicla Tanner, the leather armor vendor. GOMN says "in the area of -718 -115, near the NPC Vynon Estaliun". EQR map: https://special.eqresource.com/expacimages/thewitchswishes1.jpg (marker 1). Shuraz: the mirror "is no rent. do that step right away"; if you lose it, restarting the task will not make it appear again. |
| 2 | Deliver the lost mirror to Mugu outside of Oggok 0/1 | The Feerrott | Hand the Lost Mirror to Mugu. You get the emote above plus **Pieces of a Shattered Mirror**. EQR: "note the mirror is Temporary". EQR map: https://special.eqresource.com/expacimages/thewitchswishes2.jpg (marker 2). |
| 3 | Find Rock Salt for the brew 0/1 | ALL | Possession check. EQR: buy from **Scholar Klaz** in the Plane of Knowledge. A ZAM comment also names Research Merchant Eric Rasumus in PoK "near small bank". Map: https://special.eqresource.com/expacimages/thewitchswishes3.jpg (marker 3). |
| 4 | Find a Candied Spider for the brew 0/1 | ALL | Possession check. Recipe: **Baking, Oven, Spices + Spider Legs + Frosting, trivial 88, makes 8** (ZAM recipe 943 and ZAM-Q). Spider Legs drop from newbie-area spiders. Frosting and Spices come from Chef Denrun in PoK (EQR). GOMN: a line "was Spammed 8 times to the chat window, probably because the combine makes (8) of the items". **UNKNOWN:** the summariser could not settle whether the repeated line was the task-update line or the combine-success line. |
| 5 | Find a broken horseshoe in the South Karana Centaur Village 0/1 | South Karana | Location update that gives the **Broken Horseshoe** ("You have been given: Broken Horseshoe", S). ZAM walkthrough: /loc **256, -2337**. GOMN: "in the area of 298 -2346, inside the Northern Hut of the Centaur Village". EQR map marker 4. A 2023 EQR comment advises getting the horseshoe before leaving South Karana the first time. |
| 6 | Brew the dreadful witch's potion 0/1 | ALL | Combine **Broken Horseshoe + Candied Spider + Pieces of a Shattered Mirror + Rock Salt** inside the Dreadful Witch's Cauldron. Result: "You have fashioned the items together to create something new: Dreadful Witch's Brew." (S). ZAM calls it a "Non-Tradeskill recipe" that yields 1x brew. Trivial, skill check and fail chance are **UNKNOWN**; as a non-tradeskill recipe it presumably cannot fail, but no source says so. |
| 7 | Travel to an infamous graveyard to perform the ceremony 0/1 | Shadowrest | Location update. Get there via **Devin Traical** in PoK: say "travel" to him (GOMN). GOMN: "I did not get the Update after I zoned in. I got it at the 3rd headstone to the SE (area of -59, -159), that has the dirt covered grave." ZAM walkthrough: /loc **-59, -170**. EQR map: https://special.eqresource.com/expacimages/thewitchswishes4.jpg (marker 6). |
| 8 | Pour the potion out onto the grave 0/1 | Shadowrest | **Right-click the Dreadful Witch's Brew** while standing on that grave. Output: `I'm pouring the brew over the grave.` then `Your task 'Witch's Wishes has been updated.` The sources do not say who says the first line (a say, an emote or a task message). The brew is **not consumed**, because step 10 delivers "the remaining dreadful brew". |
| 9 | Harvest the dreadful mushroom 0/1 | Shadowrest | A **ground spawn appears** on the dirt of that grave after the pour. ZAM gives the mushroom pickup at /loc **-59, -166**. Picking it up updates the task. The ground-spawn model in the EQR screenshot is a small round **red** ball: https://special.eqresource.com/expacimages/thewitchswishes5.jpg. **UNKNOWN:** whether the spawn is per-player or shared, its despawn time, and whether it can be picked up without having poured. |
| 10 | Deliver the remaining dreadful brew to Cikdew 0/1 | South Karana | Hand the Dreadful Witch's Brew to Cikdew. Output: `Your task 'Witch's Wishes has been updated.` |
| 11 | Deliver a dreadful mushroom, before Nights of the Dead end 0/1 | South Karana | Hand the Dreadful Mushroom to Cikdew. The task completes with the gratitude text, then the reward window opens. |

Step order: ZAM lists ten walkthrough items and EQR lists eleven steps. No source says whether the steps are sequential or partly parallel. The tips (prep salt and spider early; grab the horseshoe on the first pass through South Karana) imply that **steps 3, 4 and 5 can be done in any order, or before they become active**. **UNKNOWN:** the exact live step gating. A plausible reading is that steps 1-2 and 3-5 are open together, with 6 onward sequential.

## 4. Items (flags from EQR-I raw item blocks; live id = EQR "Advanced Loot" id)

| Item | Live id | Icon | Flags (EQR) | Type / size / weight | Stack | Lore text / notes |
|---|---|---|---|---|---|---|
| Lost Mirror | 106387 | 8111 | **No Trade, Quest, Temporary** (not Lore) | TINY, 0.2, usable in tradeskills | 1 | "a lost mirror". Class None, Race None. |
| Dreadful Witch's Cauldron | 106388 | 1017 | **Magic, Lore, No Trade, Quest** | Container, **4 slots**, size capacity **SMALL**, weight reduction 1%, own size SMALL, weight 0.4 | 1 | "a dreadful witch's cauldron". Class All, **Race: All Except Froglok** (that oddity is in the raw data). Usable in tradeskills. The client combine-container type id is **UNKNOWN**: no source states it, and ZAM only says "Non-Tradeskill recipe". |
| Pieces of a Shattered Mirror | 106389 | 1031 | **Lore, No Trade, Quest** | TINY, 0.2 | 1 | Lore name "pieces of a shattered mirror". ZAM description: "All that remains of this precious mirror are thirteen broken shards. They are sharp and gleam as if begging to be touched." |
| Broken Horseshoe | 106390 | 2904 | **No Trade, Quest** (not Lore) | TINY, 0.1 | 1 | "a broken horseshoe" |
| Dreadful Witch's Brew | 106391 | 705 | **Magic, Lore, No Trade, Quest** | SMALL, 0.2, Class All, Race All | 1 | Click: **"Pour the dreadful witch's brew" - Any Slot, Casting Time: Instant, Recast Delay: 10s**. ZAM adds "Unlimited charges". Description: "This brew bubbles and swirls in its jar, seeming to project a sorrowful longing to join the freshly tilled grave. Pouring the brew out poisons the ground at your feet." Click spell is live spell **7651 "Use Ability"** (EQR-S): no mana, instant, self, recast 12s, "Not a player spell", shared by hundreds of wands and clickies. So the item's display name carries the label and the task does the work. RoF2's spell 7651 may be something else, so check it before reusing the id. |
| Dreadful Mushroom | 106392 | 4296 | **Magic, No Trade, Quest** (not Lore) | SMALL, 0.2 | 1 | Description: "This fungus that sprung forth from the grave smells of earth and rot. You feel a little nauseous holding onto it." |
| Rock Salt | 75856 | 1075 | none (plain tradeskill item) | TINY, 0.1 | 1000 | Vendor item, sells for 0.210p. EQR's vendor list is truncated; Scholar Klaz in PoK is per EQR-Q. |
| Candied Spider | 13497 | 926 | **Quest** | SMALL, 0.1, food "This is a snack. (3)" | 20 | Classic baking item. Recipe ZAM 943 (see step 4). |
| Spices / Spider Legs / Frosting | stock | | | | | Classic baking components; not re-checked. |

## 5. Rewards

- EQR-Q: "Your choice of the following: 5x Ominous Orangeade; 5x Ghastly Gummy Bears".
- GOMN: the choice is made in a **reward selection window** ("The reward window offers five Ghastly Gummy Bears or five Ominous Orangeade"). Completion line: `You have successfully been granted your reward for: The Witch's Wishes`.
- **Experience, faction, coin: none listed** in any source. That does not prove there are none; **UNKNOWN** whether live gives XP.

| Item | Live id | Icon | Flags | Stats | Other |
|---|---|---|---|---|---|
| Ominous Orangeade | 94097 | 3064 | none shown in EQR | Drink, "This is a miraculous drink! (90)". **AC 155, HP 1200, Mana 1200, End 400**. Req level 100. | SMALL, 0.5. Stack 20. Tribute 240. Sells 0.001p. Also a reward from Carving Pumpkins and Squashing Pumpkins. |
| Ghastly Gummy Bears | 94095 | 1690 | none shown in EQR (ZAM's "LORE" claim is not in EQR's raw data, so ignore it) | Food, "This is a miraculous meal! (90)". **AC 155, HP 1200, Mana 950, End 600**. Req level 100. | SMALL, 0.5. Stack 20. Tribute 600. Also a reward from Missing Pumpkins and Squashing Pumpkins. |

- The "(90)" is the food or drink duration value, not a click spell. There is **no click effect**. ZAM renders it as "Miraculous Drink(90)" / "Miraculous Meal(90)", which is the duration label, not a spell.
- Both items have no click. **UNKNOWN:** how live applies the AC/HP/Mana/End (the stat-food mechanic). No source used here explains it.

### Achievement

- **Nights of the Dead: Garden Variety Ghouls**: 10 points, no reward, Events > Holiday (EQR-A).
- It has **4 objectives**:
  - Rongol in The Western Plains of Karana: Carry the Torch
  - Rongol in The Western Plains of Karana: Scarecrow Roundup
  - Leavalin Mossbite in The Greater Faydark: Necromancer's Garden
  - Cikdew in the Southern Plains of Karana: **The Witch's Wishes**
- So The Witch's Wishes is **one of four** objectives and does not award the achievement alone.

## 6. Repeatable / lockout / level / group

- Repeatable: **Yes** (EQR-Q, ZAM-Q).
- Lockout or replay timer: **none stated** in any source. **UNKNOWN** whether live has a request timer.
- Level: ZAM gives 1-130 (older text 1-125), all classes and races.
- Solo task (EQR-Q "Task Type: Solo", ZAM "Solo").
- Time limit: Unlimited, but only while Nights of the Dead is running.

## 7. Explicit UNKNOWNS (not found in any reachable source)

1. Cikdew's **race id / model / texture**. Only a screenshot exists, and it shows a ghostly banshee-like old woman.
2. Any **spoken Cikdew line on the brew or mushroom turn-in**. Only the task completion text is known.
3. **Who emits "I'm pouring the brew over the grave."** (player say, emote or task text), and the exact click radius around the grave.
4. Exact **auto-update radii** and the precise centre points. The sources disagree by about 20-40 units: Erudin -700,-130 vs -718,-115; centaur hut 256,-2337 vs 298,-2346; Shadowrest grave -59,-170 vs -59,-159, with the mushroom at -59,-166.
5. The **cauldron's combine container type id**, and whether the brew combine can fail or has a trivial.
6. **Step gating**: which steps are open at the same time.
7. **Mushroom ground spawn**: per-player or shared, respawn or despawn time, model id. It is a red ball in the screenshot.
8. Whether **experience** is awarded, and whether there is any request lockout.
9. How live applies the reward food's stats.
10. The Lost Mirror's exact rent behaviour beyond "Temporary / no rent", and whether the Erudin spot re-gives it. Shuraz says restarting the task does not.
11. Glinda's model and screenshot URL (cat; not captured).
12. ZAM's raw HTML (403) and the Wayback Machine (offline or 429) could not be read directly. Every ZAM quote came through a summariser, and lines marked (S) may be paraphrased.

## Local raw files

All are under `scratchpad/notd/raw_witch/`:
- `eqr.html`
- `eqri_*.html` (items)
- `eqr_ach.html`
- `sp_7651.html`
- maps `thewitchswishes*.jpg`
- `cikdew_ss.jpg`, `mugu_ss.jpg`
