# Nights of the Dead 2006: Toadstool Surprise, Making Candy Apples, Find the Black Cat, Great Zombie Attack, Lycanthrope's Cure, Monster Mash

Gathered 2026-10-05. Read-only web research plus read-only reads of the local peq dump
(`scratchpad\notd_web\peq-dump\create_tables_content.sql`, parsed with `notd_web\pq.py`, `ta.py`, `se.py`) and the
ProjectEQ quest clone (`scratchpad\notd_web\peqquests`, HEAD 2124cc0, 2026-09-21). Nothing under C:\Git\test was changed.

## 0. Read this first

**Quote reliability.** Allakhazam returns 403 to curl, so every Allakhazam text came through WebFetch, which runs the
page through a summarizing model. I asked for exact quotes each time.
- **[V+]** = the same wording from two sources (for example Allakhazam and the ProjectEQ script, or two fetches).
- **[V]** = one verbatim-style transcript from one fetch (probably exact; punctuation may differ).
- **[P]** = paraphrase by the fetch model. Do not use as NPC text.
- EQ Resource item pages (items.eqresource.com) and Bonzz were read raw with curl and are exact.

**Coordinates.** Allakhazam NPC-page locations ("+A, +B") and Bonzz "/waypoint" values are in **/loc order (Y, X)**
(proved in 2006-2007-quests.md and 2008-quests.md; re-confirmed here: Laryen Allakhazam (-185, -260) = peq spawn2
x=-260, y=-185; Crazy Charlie Allakhazam (+1803, +3787) = peq x=3790, y=1815). peq spawn2 values below are given as
(x, y) and also converted to /loc (Y, X). Map-file "P" lines (Brewall format) store **(-X, -Y, Z)**.

**Item ids.** Allakhazam item ids for items added in 2006 or later are Allakhazam-internal (53536, 53664 ...). The **live
ids** below come from EQ Resource (items.eqresource.com, which uses live ids) and the peq dump (`13THFLOOR` live import);
both agree on every id listed. Flags are from EQ Resource (live), cross-checked against peq.

**Year.** All six are 2006. Allakhazam "Date added" is Oct 31 - Nov 7, 2006 for all six quest pages and NPC pages, and the
patch note of **Oct 30, 2006** says: "keep your eyes peeled for Haunted Jack and Spooky Sally with their fiendish holiday
treats in your local hometown. There have also been rumors of a strange zombie uprising, an increased bout of
lycanthropy, and other creepy encounters rising up within Kithicor Forest. Take care and watch your step! Folks in need
of assistance have been taking refuge within the Plane of Knowledge and Crescent Reach." (local patcheq copy
`notd\raw\patches\p-2006-2.txt:510-518`). The official 2008 and 2010 Halloween news names "Wicked Winnie and a wizened
hermit in the Plane of Knowledge" under "Candy and Costumes" (everquest.com/news/imported-eq-enus-51169 and -52055);
neither article names the four Kithicor/Rivervale tasks, but Allakhazam comments show them running in 2007, 2009, 2013,
2014, 2017, 2019 and 2022.

**Achievement.** All six count toward "Nights of the Dead: The Monster Mash" (Allakhazam 8832) together with Skeleton
Zapping, Aragol's Seance and Haunted Cave.

---

## 1. Nights of the Dead: Toadstool Surprise (Allakhazam quest 3802)

### Header (Allakhazam [V])
- Level 1, max 90. Solo (min 1 / max 1). Task. Era tag "Serpents Spine". Added Oct 31, 2006.
- Allakhazam header says "Repeatable: No". The peq task row (5652) is repeatable with no timer. **Live repeat/lockout:
  UNCONFIRMED** (no comment reports a timer or a second run).
- Time limit: none stated.

### Giver: a wizened hermit (Allakhazam npc 23815)
- Plane of Knowledge, Allakhazam **/loc +237, +415** "by a tree near the main bank". Bonzz: "near the main bank, by a
  tree on the hillside ( /waypoint 240, 400, -115 )". Inventory says "near main bank": agrees.
- Level: Allakhazam **30**; Bonzz "Level 50". Conflict; UNCONFIRMED which is current.
- Look (screenshot, my read): **Erudite female**, dark skin, purple head wrap, black robe with purple/pink panels and a
  gold sash, holding a staff with a glowing golden head. Allakhazam calls her "she". Suffix "(Nights of the Dead
  Quests)". Screenshot https://zam.zamimg.com/images/4/6/4664901bd71760f341ad65e2dd9a5fb2.jpg
- peq npc 202385 `a_wizened_hermit`, lastname 'Halloween Quests', level 50, race 3 (Erudite), class 2, gender 1 (female),
  texture 11, primary model 29. peq spawn2 137462 poknowledge x=336.5, y=219.3, z=-126.7 = /loc (219, 336). That is
  about 80-200 units off the live spot.

### Dialogue (Allakhazam [V])
```
You say, 'Hail, a wizened hermit'
a wizened hermit says 'I don't understand what all the fuss is about. This should be a day of [fear], not celebration!'
You say, 'Fear?'
a wizened hermit says 'Yes! All should be afraid! Er, well I can't think of anything in particular they should be scared of come to think of it. I just know that when the [masses] are fearful they stay home, and out of my hair!'
You say, 'Masses?'
a wizened hermit says 'Far too many people out and about today if you ask me. I have half a mind to turn them all into [toadstools].'
You say, 'Toadstools?'
a wizened hermit says 'It's a neat trick actually. Since it seems there won't be any peace for me today regardless, I suppose I could show it to you. Bring me back some toadstools from Toxxulia, if you dare!'
```
- The "Far too many people ..." line also appears on the NPC page ([V+]).
- Completion (Allakhazam walkthrough [V]): `The wizened hermit pulls out a strange earring as she tucks the toadstools
  into a fold of her robe. You gain experience!!`
- Bonzz shortcut keyword: "Toadstool?".

### Task steps (Allakhazam [V])
1. `Collect 10 Toxxulia Toadstools 0/10 (Toxxulia Forest)`
2. `Deliver 10 Toxxulia Toadstools 0/10 (Plane of Knowledge)`

peq's task 5652 differs: one loot step "a toxxulia mushroom" x10 (item 54725) plus "speak with a wizened hermit"; its
description reads "Loot 10 Toxxulia Toadstools from Toxxulia Mushrooms." (peq invention vs live: UNCONFIRMED).

### The toadstools
- Spawn: **"a Toxxulia toadstool"** (Allakhazam npc 47619), level 1 (Bonzz). Interactive objects: "The toadstools are
  interactive objects, so you have to target one, then type /open (or use the Open button in your abilities window),
  then loot the opened toadstool." (Sukrasisx, Nov 1 2006 [V]). Walkthrough: "You /open them like a chest and loot
  Toxxulia Toadstool." Bonzz: "These are not ground spawns as some other sites indicate."
- Respawn: "A Number of A Toxxulia Toadstool spawn every 5 minutes or less" (GOMN 2006 [V]); "just under 6 minutes"
  (Sukrasisx 2006 [P]).
- Bugs reported: "second shroom looted doesn't update task" (GOMN 2006 [P]); "Once you loot the 10th one, you
  mysteriously see that you have 11 of them" (GOMN [V]; Bonzz says the same: "you will find that you mysteriously have
  11 of them").
- 2019 behaviour: "the spawn points on the map don't help ... The toadstools aggro the scarecrows and chase them ...
  They are trackable tho." (JBMunky, Oct 13 2019 [V]). Sonicmurphy (Nov 5 2019): "Took literally less than 10min from
  start to finish ... zoned into tox from Paineel stone ... got 8 of them before bard speed faded".
- **Spawn points.** Allakhazam gives 25 lines "For your "toxxulia.txt" map file". `toxxulia` is the short name of the
  **rebuilt Toxxulia Forest** (peq zone 414), not classic `tox` (38). The numbers fall outside classic tox's X range
  (classic tox zone lines sit at x=-910 .. 2655), so these are **live rebuilt-zone positions and do not fit classic tox**.
  Conversion assumes the Brewall convention P = (-X, -Y, Z).

| # | Map line (as published) | /loc (Y, X, Z) | world x, y |
| --- | --- | --- | --- |
| 1 | P 761.5174, 1818.7858, 38.2706 | -1819, -762, 38 | -762, -1819 |
| 2 | P 2051.1235, 677.3686, 155.3069 | -677, -2051, 155 | -2051, -677 |
| 3 | P 1756.6611, 1677.5912, 64.7078 | -1678, -1757, 65 | -1757, -1678 |
| 4 | P 350.4720, 1801.4875, 45.4278 | -1801, -350, 45 | -350, -1801 |
| 5 | P 243.5448, -851.1718, 55.5215 | 851, -244, 56 | -244, 851 |
| 6 | P 1843.4877, -1139.3998, 34.3398 | 1139, -1843, 34 | -1843, 1139 |
| 7 | P 18.4986, 1447.5287, 51.5439 | -1448, -18, 52 | -18, -1448 |
| 8 | P 871.2758, 500.6535, 36.0330 | -501, -871, 36 | -871, -501 |
| 9 | P 547.1487, 792.6797, 58.5235 | -793, -547, 59 | -547, -793 |
| 10 | P 837.0746, 149.4734, 117.3322 | -149, -837, 117 | -837, -149 |
| 11 | P 2175.1797, -677.4822, 79.0849 | 677, -2175, 79 | -2175, 677 |
| 12 | P 1487.7140, -556.1827, 67.5929 | 556, -1488, 68 | -1488, 556 |
| 13 | P 840.6245, -274.5610, 90.7805 | 275, -841, 91 | -841, 275 |
| 14 | P 923.0574, -884.6240, 49.5938 | 885, -923, 50 | -923, 885 |
| 15 | P 622.4604, -474.4736, 106.9970 | 474, -622, 107 | -622, 474 |
| 16 | P -720.8629, -1929.6138, 59.5880 | 1930, 721, 60 | 721, 1930 |
| 17 | P 76.0274, -1706.1598, 82.8331 | 1706, -76, 83 | -76, 1706 |
| 18 | P 1180.3507, -1384.4940, 25.1366 | 1384, -1180, 25 | -1180, 1384 |
| 19 | P 671.9013, -1154.5884, 129.0514 | 1155, -672, 129 | -672, 1155 |
| 20 | P 550.6196, -842.8549, 97.9373 | 843, -551, 98 | -551, 843 |
| 21 | P 401.1509, -478.5786, 54.0603 | 479, -401, 54 | -401, 479 |
| 22 | P 1354.1862, -1112.9952, 23.6568 | 1113, -1354, 24 | -1354, 1113 |
| 23 | P 1567.6171, -1793.0985, 58.2810 | 1793, -1568, 58 | -1568, 1793 |
| 24 | P 1778.1122, 34.7584, 52.4555 | -35, -1778, 52 | -1778, -35 |
| 25 | P 790.1895, 998.8684, 39.1360 | -999, -790, 39 | -790, -999 |

### Items
| Item | Live id | Flags / data (EQ Resource live; peq agrees unless noted) |
| --- | --- | --- |
| Toxxulia Toadstool | **54725** | No Trade, TINY, stack 20, lore text "Toxxulia Toadstool". peq: nodrop 0, itemtype 10, weight 0. (Allakhazam/Bonzz: "No Trade, Weight 0.0") |
| Freemind Spore Earring (reward) | **53513** (Allakhazam 53536) | Magic, Lore, No Trade, Placeable. Slot Ear. SMALL, WT 0.2. **Rec Lvl 15, Req Lvl 8.** AC 5, HP 10, Mana 5, End 5, AGI 3, DEX 3, CHA 4, SvFire 3, SvCold 3, SvDisease 3. Effect: Summon Sporali Advisor (Req Lvl 15), cast 10 s, recast 5 s ("Pet Illusion: Sporali Advisor", "Blessing: Sporali Advisor"). Aug slot type 7. Lore text "Radiates with strange magic". peq: clickeffect 11502, clicktype 5, maxcharges -1 (unlimited). |

Spell 11502 "Sporali Advisor" (peq): self, cast 14000 ms in the spell (item overrides to 10 s), effect SE 108 (familiar)
with teleport_zone `SporaliFamiliar`, SE 48 base 15. Cast message `You summon forth a wise Sporali.` Bonzz: "summons a
familiar that increases disease and poison resists by 15 each, and adds 5 Regen per tic". XP: "You gain experience!!"
(amount unknown).

---

## 2. Nights of the Dead: Making Candy Apples (Allakhazam quest **3801**)

### Header (Allakhazam [V])
- Level 25, max 90. Solo task. Era "Serpents Spine". Added Oct 31, 2006.
- Header says "Repeatable: No", but 2006-2008 comments say it repeats on a timer:
  - Oct 31 2006 [V]: "You get 5 gummy bears, and the task is on a roughly 3 hour timer."
  - Nov 1 2006 [V]: "This quest is repeatable every 3 hours, I've done it twice now."
  - Nov 1 2006 [V]: "Timer for me shows 2 hours 45 minutes from as soon as I did turn in."
  - Oct 26 2008 [V]: "Reward: Caramel-Coated Candy Apple you get 5 of them on turn in you have to wait a bit over 2
    hours to redo the quest"
  - **Conclusion: repeatable, replay timer about 2h45m-3h** (exact value UNCONFIRMED).

### Giver: Wicked Winnie (Allakhazam npc 23814)
- Plane of Knowledge, Allakhazam **/loc +182, +270** "by a tree near the main bank"; Bonzz /waypoint 180, 275.
- Level 30 (Allakhazam). Look (screenshot, my read): **Dark Elf female**, white hair, long **yellow/gold robe** with red
  trim, carrying a **bloody scythe**. Screenshot https://zam.zamimg.com/images/e/5/e521b8f77b6b26260922bb29e376e297.jpg
- peq npc 202384 `Wicked_Winnie`, level 60, race 6 (Dark Elf), gender 1, texture 12, helm 12. peq spawn2 137434
  poknowledge x=621.1, y=433.6 = /loc (434, 621): **far from the live spot** /loc (182, 270).

### Dialogue (Allakhazam [V])
```
You say, 'Hail, Wicked Winnie'
Wicked Winnie says 'Salutations, are you enjoying the [festivities]? I know I am.'
You say, 'I'm enjoying the festivities.'
Wicked Winnie says 'This is my favorite time of year! Little hobgoblins running around, candy, and spooky hauntings. If I had some of my [Wicked Liquid Caramel] I could really dress up some apples. Divine!'
You say, 'Wicked liquid caramel?'
Wicked Winnie says 'Oh yes. Haunted Jack has some Haunted Candy Apples he is carting around, but those are nothing compared to my concoctions. Unfortunately, the caramel I use is very special and I've been so busy helping Sally out with her costumes this year that I haven't had time to [track it down].'
You say, 'I'll track it down for you.'
Wicked Winnie says 'Well, last time I ran across it through a gnome named Finkel. It's possible that he still has some. I believe he is doing business in Steamfont this time of year.'
```
- Completion (walkthrough [V]): `Wicked Winnie whips up a batch of her famous Caramel-Coated Candy Apples! You gain
  experience!!`
- Bonzz shortcut keyword: "Track it down".

### Task steps (Allakhazam [V])
1. `Collect 1 Haunted Candy Apple 0/1 (ALL)`
2. `Collect 1 Liquid Caramel 0/1 (Steamfont Mountains)`
3. `Deliver 1 Haunted Candy Apple to Wicked Winnie (Plane of Knowledge)`
4. `Deliver 1 Liquid Caramel to Wicked Winnie (Plane of Knowledge)`

peq task 5651 has a single step: deliver Liquid Caramel to Wicked Winnie (npc 202384), zone 202.

### Where the two items come from
- **Haunted Candy Apple(s)**: "sold (for nothing) by a merchant named Haunted Jack, found just north of Winnie in the
  Plane of Knowledge." Diepen 2022 and Sigpaos 2017 [V+]: "Haunted Jack is north from Winnie, not west." peq npc 202387
  `Haunted_Jack` (lastname 'Spooky Candies', race 82 scarecrow, level 30) at poknowledge x=288.8, y=277.5 = /loc (277,
  289); peq merchantlist 202387 slot 15 = item 85067.
- **Liquid Caramel**: "sold (for nothing) by Finkel Rardobaen, who may be found near the three huts in the Steamfont
  Mountains: location -1235, -1465." curdardh Oct 31 2007 [V]: "Finkel Rardobaen in Steamfont at 3 huts loc: -1234,
  -1467". Bonzz: "in one of the huts to the southeast ( /waypoint -1260, -1475 )". Live Steamfont is the SoF rebuild
  (`steamfontmts`; SoF launched November 2007). curdardh's comment is dated Oct 31 2007, which is probably before the
  rebuild, so -1234, -1467 may be a classic-Steamfont /loc; but peq's classic Finkel stands at /loc (-1515, -1844).
  Which spot is right for classic `steamfont`: UNCONFIRMED.
- Alternative: "Quana Rainsparkle in Toxxulia Forest inside the hut by the PoK book (Erudin side). At least for good
  characters. She does not like evil worshipers such as SKs." (nytmare, Oct 22 2017 [V]).
- peq: Finkel exists twice, classic `steamfont` npc 56112 (spawn2 x=-1844, y=-1515 = /loc (-1515, -1844)) and rebuilt
  npc 448144; Quana is classic `tox` npc 38070 (spawn2 x=-1111, y=2171 = /loc (2171, -1111), faction 210) and rebuilt
  414034. All four merchant lists (56112 slot 22, 448144, 414034, plus Parthar 408138 in Commonlands) sell item 54723.

### Rewards (conflict)
- Allakhazam reward list: Caramel-Coated Candy Apple and Delectable Gummy Bears. Bonzz: "Caramel-Coated Candy Apple
  ... and / or Delectable Gummy Bears".
- Players: 2006 "You get 5 gummy bears"; Nov 5 2007 got Caramel-Coated Candy Apples and questioned the gummy bears
  [P]; 2008 "Caramel-Coated Candy Apple you get 5 of them".
- **Most likely: 5x of one snack; which one (or level-based / random) is UNCONFIRMED.** Plus experience.

### Items
| Item | Live id | Flags / data (EQ Resource live) |
| --- | --- | --- |
| Haunted Candy Apples (merchant, free) | **85067** | Magic, No Trade, TINY, snack (5), stack 20. HP 30, STR 8, INT 8, WIS 8, AGI 5, DEX 5, SvMagic 5. Lore "A candy apple haunted by a spooky spirit". Note live name is plural **"Haunted Candy Apples"**. |
| Liquid Caramel (merchant, free) | **54723** | No Trade, TINY, stack 1, lore "Liquid Caramel". |
| Caramel-Coated Candy Apple (reward) | **85064** (Allakhazam 45453) | Magic, No Trade, TINY, snack (5), stack 20. HP 35, Mana 35, End 35, STR 10, STA 5, INT 10, WIS 10, DEX 5, SvMagic 5. Lore "A candy apple coated in sweet caramel". |
| Delectable Gummy Bears (reward) | **87315** (Allakhazam 53535) | Magic, No Trade, TINY, snack (5), stack 20. HP 75, Mana 70, End 40, STR 5, STA 5, INT 10, WIS 10, AGI 5, DEX 8, SvFire 5, SvCold 6. Lore "Gummy bears dipped in sweet sugar". |

---

## 3. Nights of the Dead: Find the Black Cat (Allakhazam quest 3799)

### Header (Allakhazam [V])
- Level 25, max 125. Solo task. Era "Serpents Spine". Added Oct 31, 2006.
- Header: "Repeatable: No" but **"Success Lockout Timer: 03:00:00"**; an anonymous Nov 3 2006 comment: repeat timer "3
  hours". **Repeatable with a 3-hour success lockout.**

### Giver: Syxa Jewlborn (Allakhazam npc 23810)
- Kithicor Forest, Allakhazam **/loc +1334, -1001 "at the Commonlands zoneline"**; Bonzz /waypoint 1335, -1000. peq
  Kithicor's Commonlands zone line is at x=-1089, y=1464, so this is classic Kithicor geometry.
- Level 35 (Allakhazam). Look (screenshot, my read): **Dark Elf female**, white hair, **black robe with purple/pink
  panels**, carrying a bloody scythe. Screenshot https://zam.zamimg.com/images/c/7/c753d1828b82a80979647e61e3576f79.jpg
- peq npc 20281 `Syxa_Jewlborn`: **race 11 (Halfling)**, gender 1, level 65, class 6 - wrong race vs live. peq spawn2
  137086 kithicor x=3840.8, y=1897.2 = /loc (1897, 3841), i.e. **at the Rivervale line, not the Commonlands line**.

### Dialogue (Allakhazam [V])
```
You say, 'Hail, Syxa Jewlborn'
Syxa Jewlborn says 'Please help me find my missing cat, she has gone astray and I can't seem to find her anywhere. Her name is Muffin. Will you [help] me? Oh please!'
You say, 'I will help!'
Syxa Jewlborn says 'Please bring her back safely!'
You have been assigned the task 'Find the Black Cat'.
You say, 'Hail, a black cat'
Muffin says 'meow...'
```
Return without the cat [V]: `Syxa Jewlborn says 'Did you find Muffin? I don't see her anywhere. Please return her to me
safely!'`
Return with the cat [V]: `Syxa Jewlborn says 'Oh you found her! How can I ever repay you.'`

### Task steps (Allakhazam [V])
1. `Find Syxa's missing cat 0/1 (Kithicor Forest)`
2. `Return Syxa's cat to her 0/1 (Kithicor Forest)`

### The cat (mechanic)
- "a black cat" roams "the middle / western part of the zone" (Bonzz); Allakhazam: central and western Kithicor.
  Trackable.
- Hailing it turns it into **"Muffin"** who follows you: "once you turn one into Muffin you can run back to the quest NPC
  at full speed and it will follow no problem, like a pet." (nytmare 2017 [V]).
- It takes your pet slot: Romen, Oct 27 2013 [V]: "I did this today and hailed the cat. when I got back to hail Sxya acted
  as if the cat weren't there. Then I realized something was funny with my pet - I couldn't buff it and couldn't suspend
  it (said I had a pet). I summoned pet and hailed and got update. It almost seemed like the cat was in place of my pet.
  After hail my pet was back to normal."
- Counts: "The track window shows there are 3 'a black cat' up at any given time. Once a cat is turned in, it respawns in
  just under 5 minutes." (nytmare, Oct 21 2017 [V]). "If you are boxing this mission keep in mind once someone hails a
  cat another one will not spawn until they either zone or do the final hail." (Aurastrider, Oct 22 2017 [V]).
- peq: `a_black_cat` 20282 and `#Muffin` 20283, both level 20, race 439, gender 2, bodytype 21; one spawn2 point
  (137087, x=3204, y=899). peq task 8278 steps: "Find the Black Cat." (speak to 20282) / "Return to Syxa Jewlborn."

### Reward
- **5x Scrumptious Jack-o-Lantern** (Allakhazam reward line "5x") plus experience.

| Item | Live id | Flags / data (EQ Resource live) |
| --- | --- | --- |
| Scrumptious Jack-o-Lantern | **87311** (Allakhazam 53533) | Magic, No Trade, TINY, snack (4), stack 20. HP 45, Mana 30, STR 3, STA 3, INT 5, WIS 5, AGI 3, DEX 3, SvFire 5. Effect: **Illusion: Scarecrow**, any slot, instant, expendable 1 charge. Lore "Contains red 5". peq: clickeffect 6107 (spell "Illusion: Scarecrow": SE 58 base 82 = scarecrow race, buffduration 360 ticks, cast 1.5 s in the spell, recast 90 s). |

---

## 4. Nights of the Dead: Great Zombie Attack (Allakhazam quest 3842)

### Header (Allakhazam [V])
- Level 1, max 125. Repeatable, no lockout listed. Solo task. Era "Serpents Spine". Added Nov 7, 2006.

### Giver: Crazy Charlie (Allakhazam npc 23837)
- Kithicor Forest, **/loc +1803, +3787 "outside Rivervale"** (quest page 1815, 3790; Bonzz /waypoint 1820, 3795).
- Level 36 (Allakhazam). Look (screenshot, my read): **Gnome male**, bald, red shirt, brown trousers, leather
  bandolier/apron, holding a dagger. Screenshot https://zam.zamimg.com/images/d/6/d6e2f28c07f4ad8f20b87eeba45c210a.jpg
- peq npc 20285 race 12 (Gnome), level 70; spawn2 137088 x=3790, y=1815 (matches live).

### Dialogue (Allakhazam [V], second fetch with full lines)
```
You say, 'Hail, Crazy Charlie'
Crazy Charlie says 'Dagnabbit! Don't creep up on folks like that, especially around here! What are ya trying to do, give somebody a heart attack! Noise attracts [their] attention, don't ya know.'
You say, 'Their attention?'
Crazy Charlie says 'Who? Look around! The zombies, of course! They aren't too bright, but seem attracted to noises. I just know the [epidemic] is going to spread.'
You say, 'What epidemic?'
Crazy Charlie says 'What epidemic? Are you mad? Where do you think all these zombies came from? Luclin? Someone has to be getting sick and turned or there wouldn't be any zombies! Of course there's an epidemic. I fear mass [carnage] is the only way to go.'
You say, 'Carnage?'
Crazy Charlie says 'Aye. If we kill them all, then there are none left to infect us. See? Yup. Mass carnage it is. Are you going to [fight] or just ignore the problem?'
You say, 'I will fight.'
Crazy Charlie says 'Good on ya! Get on out there then and kill some zombies! Bring me some hearts while you're at it. I want to have a look at what's going on in there.'
You have been assigned the task 'Great Zombie Attack'.
You receive a Fiery Wand of Retribution with 10 charges of Retributive Fire.
```
Task description [V]: `Crazy Charlie has asked that you find and torch 10 zombies with your Blazing Wand of
Retribution.` (live text says "Blazing"; the item is "Fiery").

### Task step (Allakhazam [V])
1. `Torch 10 zombies with the Blazing Wand of Retribution 0/10 (Kithicor Forest or Rathe Mountains)`
- **Auto-completes on the 10th torch; there is no return to Charlie.** Completion [V]: `The zombie presence seems somewhat
  lessened, and perhaps they have been quelled . . . for the time being.` then `You have successfully been granted your
  reward for: Great Zombie Attack`. Bonzz: "After the last one dies, the task is completed."
- "Bring me some hearts" is flavour; no heart step exists.

### Mechanic
- "When you cast the fiery wand it makes the zombies run away and then they die...corpse poofs so if they had a heart it
  poofs as well =)" (Marclar, Nov 9 2006 [V]). Bonzz: "they will flee and die".
- **Level check**: "I get the message 'Your target is too powerful to ignite'. Do I have to be a certain level?"
  (animekenji, Nov 1 2009 [V]). hullan, Nov 3 2019 [V]: "I'm level 4 and these can be torched [Rathe Mtns zombies]. The
  Zombie trooper in Kithicor can't by me at least. I also tried the regular zombies there and they didn't work. I think
  the zombies need to be within a certain ranger to your level in order to to be torched." Exact rule UNCONFIRMED.
- Which zombies: Bonzz says "zombie trooper" in Kithicor. Kithicor's regular night "Zombie Trooper" (Allakhazam npc
  1902) is level 33-37 with harm-touch-style nukes, so low levels use Rathe Mountains zombies instead.
- peq: task 5655 (one activity "Torch 10 Zombie Troopers", zone 20 only). peq made 23 custom `zombie_trooper` spawns
  (npc 20284, level 30, race 70, class 5, faction 1179, respawn 90 s) around eastern Kithicor.

### Items
| Item | Live id | Flags / data (EQ Resource live) |
| --- | --- | --- |
| Fiery Wand of Retribution | **87309** (Allakhazam 53664) | Magic, Lore, No Trade. Slot Primary, SMALL, WT 1.5. Effect Retributive Fire, any slot, instant, expendable 10 charges. IT10506. peq: clickeffect 3089, clicktype 1, scriptfileid 32767. |
| Crystallized Candy Corn (reward x5) | **87319** (Allakhazam 53665) | Magic, No Trade, TINY, snack (4), stack 20. Mana 60, SvMagic 6, SvFire 6, SvCold 6, SvDisease 6, SvPoison 6. Lore "Just like corn only better". |

Spell 3089 "Retributive Fire" (peq): single target, range 150, recast 12 s, SE 10 placeholder; messages `You call forth
retributive fire!` / `<target> ignites in flame.` The kill/flee is scripted or server-side.

---

## 5. Nights of the Dead: Lycanthrope's Cure (Allakhazam quest 3823)

### Header (Allakhazam [V])
- Level 30, max 125. Repeatable, no lockout listed. Solo task. Era "Serpents Spine". Added Nov 3, 2006.

### Giver: Laryen Lycanthrope (Allakhazam npc 23823)
- **Rivervale**, /loc **-185, -260** (Bonzz /waypoint -185, -260). Dragkila, Nov 3 2006 [V]: "Neg 187, Neg 261, Neg 7.
  North of Kithicor Forest zoneline."
- Level 32 (Allakhazam). Look (2007 screenshot, my read): **Dwarf male**, brown beard, dark leather/chain vest, brown
  trousers. Old suffix "(Halloween Quests)". Screenshot https://zam.zamimg.com/images/i/d/id23823.png
- peq npc 19151 race 8 (Dwarf), level 70; spawn2 137433 rivervale x=-260, y=-185 (matches live).

### Dialogue (Allakhazam [V])
```
You say, 'Hail, Laryen Lycanthrope'
Laryen Lycanthrope says 'Howdy. You venturing out into the [forest]? I have a quick favor to ask if you're heading out that way already.'
You say, 'Forest?'
Laryen Lycanthrope says 'Well, this lycanthropy stuff is pretty serious. It would be easy for me to reconcile just wiping them out if they weren't normal folks most of the time. Just doesn't sit well with me to be out there bashing people's skulls in that can't help themselves, you know? So, I've been working on a [cure].'
You say, 'What cure?'
Laryen Lycanthrope says 'I think I have the formula nearly right. I wouldn't recommend approaching any werewolves at full strength, but I see enough injured ones here and there to make it worth my while for [testing].'
You say, 'Testing?'
Laryen Lycanthrope says 'It's easy, you just hit them with the cure and back off. Keep an eye out for creepy crawlers nearby, if you get my drift. The forest is packed with them this time of year. Are you [up for it]?'
You say, 'I am up for it.'
Laryen Lycanthrope says 'That's the spirit! Take these cures and help out as many of those poor souls as you can.'
You have been assigned the task 'Lycanthrope's Cure'.
You receive a Wand of the Blood Curse, with 5 charges of Blood Curse Antidote.
```
Completion [V]: `Laryen seems disappointed at the instability of his cure, and shrugs a bit before fishing out your
reward.` / `You gain experience!! You have successfully been granted your reward for: Lycanthrope's Cure`

### Task steps (Allakhazam [V])
1. `Locate and cure 5 fallen werewolfs 0/5 (Kithicor Forest)` (live typo "werewolfs")
2. `Return to Laryen Lycanthrope 0/1 (Rivervale)`

### The werewolves
- "Head into Kithicor Forest. Find and target "a fallen werewolf" (trackable; found in a several different locations
  through the zone), then right-click the wand to cure them." Bonzz: "When you find one, it will be lying on the ground.
  Click the Wand of the Blood Curse on five (5) different a fallen werewolf."
- **a fallen werewolf** (Allakhazam npc 23824): level 30-32, race Werewolf, Kithicor. 2007 screenshot shows a werewolf
  model **lying on the ground** (https://zam.zamimg.com/images/i/d/id23824.png).
- Spawning: "You have to kill any wolf to get the werewolves to spawn.It is very slow.Took me over 1 hour." (Oct 27 2007
  [V]); "The Feign Death Troopers are the PH's you have to kill them to get Fallen Werewolves to spawn." (Oct 31 2007
  [V]); "they got really scarce last night" (UnholyCzars, Nov 7 2007). Placeholder rule UNCONFIRMED (two different
  claims).
- Comments confirm it still ran in 2014 ("its 2014 and the npc is up").
- peq: `a_fallen_werewolf` npc 20286 (level 19, race 14, gender 2) exists but has **no spawn2 row**; task 5654 has one
  activity "Cure 5 Fallen Werewolves" (type 8) plus "speak to Laryen".

### Items
| Item | Live id | Flags / data (EQ Resource live) |
| --- | --- | --- |
| Wand of the Blood Curse | **87310** (Allakhazam 53599) | Magic, Lore, No Trade, Placeable. Slot Primary, SMALL, WT 1.5, light source 6. Effect Blood Curse Antidote, instant, expendable 5 charges. IT10822. peq clickeffect 11658. Bonzz calls the effect "Blood Dose Antidote" (typo). |
| Gummy Bear Delight (reward x5) | **87318** (Allakhazam 53601) | Magic, No Trade, TINY, snack (5), stack 20. HP 100, Mana 100, End 20, STR 9, STA 3, INT 10, WIS 10, AGI 3, DEX 3, CHA 8, SvMagic 3, SvDisease 3, SvPoison 15. Lore "They taste so sweet". |

Spell 11658 "Blood Curse Antidote" (peq): single target, range 150, instant, no recast, SE 10 placeholder, other-message
`<target> is cleansed.` Cure effect is scripted/server-side.

---

## 6. Nights of the Dead: Monster Mash (Allakhazam quest 3800)

### Header (Allakhazam [V])
- Level 35, max 90. Repeatable, no lockout listed. Solo task. Era "Serpents Spine". Added Oct 31, 2006.

### Giver: Lurgh (Allakhazam npc 23813)
- Kithicor Forest, **/loc +1856, +3747 "just outside Rivervale"**; Bonzz "an Ogre near Rivervale ( /waypoint 1855, 3750
  )".
- Level 34 (Allakhazam). Look (2019 screenshot, my read): **Ogre male**, bald, full plate-style armour (dark grey with
  rust-coloured trim), no weapon. Screenshot https://zam.zamimg.com/images/4/a/4afecbe97eaa57c04526072f5539b954.jpg
- peq npc 20288 race 9 (Ogre), level 50, texture 2; spawn2 137435 x=3527, y=1604 = /loc (1604, 3527), about 270 units off
  the live spot.

### Dialogue ([V+]: Allakhazam fetch gave each line's opening, the ProjectEQ script `kithicor/Lurgh.pl` gives the same
lines in full)
```
You say, 'Hail, Lurgh'
Lurgh says 'Lurgh miss [friend].'
You say, 'Friend?'
Lurgh says 'Lurgh had friend that battle hard. We fight lots. Skeleton friend [dance] for me, but he gone now.'
You say, 'Dance?'
Lurgh says 'Lurgh laugh when skeleton dance. But now sad, [skeleton] ate by bear and no more dancin' for Lurgh.'
You say, 'Skeleton?'
Lurgh says 'Lurgh see lots of skeleton here. Maybe one be friend? You [help] Lurgh find friend?'
You say, 'I will help'
Lurgh says 'Gud. Find skeleton make Lurgh laugh and Lurgh help you, too.'
```
Completion (Allakhazam walkthrough [V+], same text in Lurgh.pl as an emote): `Lurgh is pleased with your success, and
offers you these dancing skeletons as a token of his appreciation. You gain experience!!`
Dec 31 2006 comment: you "didn't have to say 'candy corn'" to get the reward.

### Task steps (Allakhazam [V])
1. `Collect 1 Skeletal Skull (Kithicor Forest) 0/1`
2. `Collect 1 Skeletal Torso (Kithicor Forest) 0/1`
3. `Collect 1 Skeletal Leg (Kithicor Forest) 0/1`
4. `Collect 1 Skeletal Arm (Kithicor Forest) 0/1`
5. `Deliver Skeletal Skull to Lurgh 0/1`
6. `Deliver Skeletal Torso to Lurgh 0/1`
7. `Deliver Skeletal Leg to Lurgh 0/1`
8. `Deliver Skeletal Arm to Lurgh 0/1`
(step order and exact punctuation from one fetch; the four collect/deliver pairs are certain)

### Drops
- "These drop randomly from skeleton mobs in the forest." (walkthrough)
- "I had all 4 items drop from 'skeleton infantry', didnt see any other mob drop them" (Nov 2 2006 [V]); "I saw the four
  bone types on several different types of skeletons but none ever on any zombie mob" (kirbyramz, Nov 2 2006 [V]).
- "It has to be night and then all the correct skeletons show up." (Galadrena, Oct 29 2022 [V]). Kithicor's night
  undead are level 35+ (the 1999 Bloody Kithicor change), which fits the level-35 minimum.
- Drop rates: not published.

### Items
| Item | Live id | Flags / data (EQ Resource live) |
| --- | --- | --- |
| Skeletal Skull | **54718** (Allakhazam 53572) | No Trade, TINY, stack 1, lore "Skeletal Skull" |
| Skeletal Torso | **54719** (Allakhazam 53570) | No Trade, TINY, stack 1, lore "Skeletal Torso" |
| Skeletal Leg | **54720** (Allakhazam 53571) | No Trade, TINY, stack 1, lore "Skeletal Legs" |
| Skeletal Arm | **54721** (Allakhazam 53569) | No Trade, TINY, stack 1, lore "Skeletal Arms" |
| Candy Corn (reward x5, "quested version") | **87317** (Allakhazam 53534) | Magic, No Trade, TINY, snack (5), stack 20. HP 90, Mana 90, End 10, STR 8, STA 2, INT 8, WIS 8, AGI 2, CHA 5, SvFire 5, SvCold 6. Lore "Candy corn haunted by a spooky spirit". Do not confuse with **Candy Corn 84090** (Lore, stack 1, no stats), the 2005 Trick or Treat candy from Scary Miller. |

Reward quantity: ProjectEQ gives 5 (`summonitem(87317,5)`); Allakhazam's reward line does not state a count clearly.
Live quantity UNCONFIRMED (5 is likely, matching the other 2006 tasks).

---

## 7. ProjectEQ status (what the local data already has)

| Quest | peq task id (probably the live id) | peq script | peq NPC rows / spawns | Gaps vs live |
| --- | --- | --- | --- | --- |
| Toadstool Surprise | 5652 | none | hermit 202385 spawned in PoK | no toadstool objects; task step wording differs |
| Making Candy Apples | 5651 | none | Winnie 202384 (wrong spot), Haunted Jack 202387 + merchant list, Finkel, Quana | one-step task only |
| Find the Black Cat | 8278 | none | Syxa 20281 (wrong race, wrong zone line), cat 20282, #Muffin 20283 | no follow mechanic |
| Great Zombie Attack | 5655 | none | Charlie 20285, 23 custom zombie troopers | no Rathe Mountains option |
| Lycanthrope's Cure | 5654 | none | Laryen 19151; werewolf 20286 never spawns | |
| Monster Mash | 5653 | `kithicor/Lurgh.pl` (Perl, qglobal `halloween_monster_mash` H3, AddLevelBasedExp(10), 5x 87317) | Lurgh 20288 | no confirmed part drops |

The peq task ids 5651-5656 run in a block (5656 = Aragol's Seance), which suggests they are copied live ids; that is
UNCONFIRMED. All peq quest tasks also assign custom task 500219 "Happy Halloween!".

## 8. Could NOT find (not guessed)
1. Toadstool Surprise: live repeat timer; current hermit level (30 vs 50); live toadstool count/respawn now.
2. Making Candy Apples: which reward (5 Caramel-Coated Candy Apples vs 5 Delectable Gummy Bears, or both/level-based);
   exact replay timer; whether Finkel's numbers are classic or rebuilt Steamfont.
3. Find the Black Cat: the cat's spawn points; cat level/race on live.
4. Great Zombie Attack: the level rule behind "Your target is too powerful to ignite"; which Rathe Mountains zombies
   count; XP.
5. Lycanthrope's Cure: werewolf spawn points and the placeholder rule (any wolf vs "feign death troopers").
6. Monster Mash: drop rates, which skeleton names drop the parts, reward count.
7. All six: XP amounts; exact live NPC race/class codes (race above is read from screenshots).

## Sources
- Allakhazam quests: https://everquest.allakhazam.com/db/quest.html?quest=3802 , ?quest=3801 , ?quest=3799 ,
  ?quest=3842 , ?quest=3823 , ?quest=3800 ; achievement ?quest=8832
- Allakhazam NPCs: https://everquest.allakhazam.com/db/npc.html?id=23815 (hermit), 23814 (Winnie), 23810 (Syxa),
  23837 (Crazy Charlie), 23823 (Laryen), 23824 (a fallen werewolf), 23813 (Lurgh), 1902 (Zombie Trooper), 47619
  (a Toxxulia toadstool, linked from 3802); search pages ?q=Wicked+Winnie , ?q=Syxa
- Screenshots: zam.zamimg.com URLs listed per NPC above (local copies in `scratchpad\notd\web\img\`)
- EQ Resource live items: https://items.eqresource.com/items.php?id= 54725, 53513, 85067, 54723, 85064, 87315, 87311,
  87309, 87319, 87310, 87318, 54718, 54719, 54720, 54721, 87317 (raw copies in `scratchpad\notd\web\eqr\`)
- Bonzz: https://www.bonzz.com/nightsofthedead.htm (2006 #1-#7) and https://www.bonzz.com/spore.htm (Toadstool)
- Official news: https://www.everquest.com/news/imported-eq-enus-51169 (2008), https://www.everquest.com/news/imported-eq-enus-52055 (2010)
- Patch note Oct 30, 2006: https://github.com/nazwadi/patcheq (local copy `scratchpad\notd\raw\patches\p-2006-2.txt`)
- Fanra wiki Halloween page (lists all six quest links): https://fanra.fandom.com/wiki/Halloween
- ProjectEQ: https://github.com/ProjectEQ/projecteqquests (clone 2124cc0: kithicor/Lurgh.pl) and the local peq dump
  (tables items, spells_new, npc_types, spawnentry, spawn2, tasks, task_activities, merchantlist, zone_points)
