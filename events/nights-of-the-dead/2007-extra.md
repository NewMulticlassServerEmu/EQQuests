# Nights of the Dead 2007: Toxxulia Pie Fling, Nektulos Ghost Rider

Gathered 2026-10-05. Read-only web research plus read-only reads of the local peq dump and the ProjectEQ quest clone
(`scratchpad\notd_web\`). Nothing under C:\Git\test was changed. (Troublemakers in Faydark and Undead Rising, the other
two 2007 tasks, are already in `2006-2007-quests.md`.)

## 0. Read this first
- **Quote reliability**: same tags as the other NotD research files. **[V+]** = same wording from two sources (here
  usually Allakhazam + the peq task/script data, which was imported from live); **[V]** = one verbatim-style WebFetch
  transcript of Allakhazam (Allakhazam blocks curl); **[P]** = paraphrase by the fetch model.
- **Coordinates**: Allakhazam NPC locations and Bonzz "/waypoint" values are **/loc order (Y, X)**. peq spawn2 and quest
  script values are world **(x, y)**. Map-file "P" lines (Brewall format) store **(-X, -Y)**.
- **Item ids**: live ids from EQ Resource (items.eqresource.com) = peq ids. Allakhazam ids for these items are internal.
- **Year 2007**: Allakhazam quest pages added Nov 1 and Nov 4, 2007 ("Era: The Buried Sea"); Grom Shives NPC page added
  Nov 1, 2007; Marta Stalwart NPC page added Nov 4, 2007; first comments Nov 2-5, 2007. Patch note 2007 (generic): "Halloween
  Events: Citizens and denizens of Norrath and beyond will encounter new and old ghoulish tasks and fiends as the spirit of
  Halloween takes over EverQuest this eerie season." The official 2008 and 2010 news list both under "Haunting Tasks":
  - "Marta Stalwart in Toxxulia is baking pies to celebrate an old Erudite pie flinging tradition started by an angry wife
    who scolded her lazy husband by throwing pies at him."
  - "Grom Shives in Nektulos is retelling the tale of the legendary ride of a dark elf warrior who swindled magic from
    powerful creatures, and managed to evade them in Nektulos as he returned to Neriak."
- **Achievement**: both count toward "Nights of the Dead: Undead Rising" (Allakhazam 8833) with Troublemakers in Faydark
  and Undead Rising.

---

## 1. Nights of the Dead: Toxxulia Pie Fling (Allakhazam quest 4319)

### Header (Allakhazam [V])
- Level 2, max 90. Solo (min 1 / max 1). Task. Repeatable. Added Nov 4, 2007. No lockout, no time limit listed.
  nytmare (Oct 2017): "No replay timer." [P]
- peq task **3539** "Toxxulia Pie Fling" (levels 1-85, repeatable, reward_text "Loot and Experience", description
  "Hit 10 scarecrows with pies."). 3539/3540 look like live task ids (the peq Mask of Eyes script uses 3540); UNCONFIRMED.

### Giver: Marta Stalwart (Allakhazam npc 26717)
- Allakhazam: **Toxxulia Forest 2.0**, **/loc +1987, -739** "outside a building, south of the Erudin zoneline". Merf, Nov
  2007 [P]: "+1988, -740" by a building near the Erudin zone entrance. Bonzz: "in a building near Erudin ( /waypoint 1985,
  -740 ) and should be on 'Find.'" (Bonzz misspells her "Marta Stewart").
- Level 60 (Allakhazam). Look (screenshot, my read): **Erudite female**, dark skin, lavender hood, orange/tan robe with a
  leather corset top and bracers. Suffix "(Nights of the Dead Quests)". Screenshot
  https://zam.zamimg.com/images/d/d/dd8581ee6e7ec44fcc3d63364b88b04e.jpg
- peq npc 38178 `Marta_Stalwart` (lastname 'Halloween Quests', level 45, race 3 Erudite, class 1, gender 1, texture 1).
  peq spawn2 137481 in **classic `tox`** at x=-121, y=30 = /loc (30, -121), i.e. next to peq's pie mobs, **not** at the
  live building near Erudin. Classic tox's Erudin zone line is at x=296, y=2550.

### Dialogue (Allakhazam [V])
```
You say, 'Hail, Marta Stalwart'
Marta Stalwart smiles graciously at you, 'Have you come to participate in our pie flinging [tradition]?'
You say, 'Tradition?'
Marta Stalwart nods understandingly, 'I see you are not familiar with this particular tradition... It began long ago when an Erudite wife grew tired with her lazy, loafing [husband].'
You say, 'Her husband?'
Marta Stalwart chuckles politely, 'Oh yes, this Erudite fellow wouldn't lift a finger to help anyone, let alone his loving wife... poor woman, worked her fingers to the bone for him day in and day out. Well, good things only last so [long].'
You say, 'How long?'
Marta Stalwart shifts her stance slightly, 'Having just baked a fresh pair of squash pies, this hard working wife suddenly snapped as she looked down at her napping husband, and [hurled] both pies down at him, scolding him angrily as he tried to understand what had just happened to him.'
You say, 'Hurled pies?'
Marta Stalwart laughs, 'Well, I guess there isn't much more to the story, but somehow it has evolved into a wonderful tradition that takes place in the forest of Toxxulia each year... Participants don scarecrow costumes, and fling freshly baked pies at each other... I have some freshly baked pies, if you would like to [take part].'
You say, 'I would like to take part.'
Marta Stalwart hands you a stack of warm squash pies, 'You will also need to put on a [costume] when you are ready to start flinging pies.'
You have been assigned the task 'Toxxulia Pie Fling'.
You receive a Stack of Squash Pies with unlimited charges of Throw Pie.
You say, 'What costume?'
Marta Stalwart helps you into an itchy scarecrow costume, 'Good luck, if you get hit with any pies, come back and I'll help you get get cleaned up and [try] again.'
```
- "get get" is live's typo; keep it.
- Completion [V]: `Marta Stalwart claps in amusement, 'Bravo _____, you've done very well and managed to dodge every pie
  thrown at you, quite remarkable. Why don't you relax and enjoy some of these fresh baked pies I've just made.'`
- Retry keywords: "try", then "costume" (nytmare 2017: "re-requests the task with 'try' and 'costume' after each hit").
  Bonzz shortcuts: "Hurled" to get the task, "Costume" for the illusion. The response to "try" is UNCONFIRMED.
- The costume is a scarecrow illusion: "You immediately change into a scarecrow illusion after saying, 'costume'." [P]

### Task steps ([V+]: Allakhazam = peq task_activities 3539 description_override, word for word)
1. `Have Marta help you into a [costume] 0/1 (Toxxulia Forest)`
2. `Throw squash pies at others in scarecrow costumes 0/10 (Toxxulia Forest)`
3. `Let Marta know how well you've done, don't get hit on the way! 0/1 (Toxxulia Forest)`

### The pie fight (messages [V])
- Targets: **a pie flinger** (Allakhazam npc 26714), **a pie hurler** (26715), **a pie thrower** (26716): scarecrows,
  locations vary. Other players in the scarecrow costume also count: "You can also throw pies at other players if they
  are doing this quest as well." (lymark 2020 [P]).
- Range: Bonzz "Go near them, but not too close (range 150, max), target them and click the Stack of Squash Pies on them."
- Hit: `SPLAT! Your victim is covered in a warm gooey squash pie.` The target despawns.
- Miss: `Your pie misses, and your target prepares to return fire! A squash pie is flung at you, run _____ to dodge it!`
  The blank is North / South / East / West, or the message says to **DUCK**: "when a PC or NPC throws at you there is a
  random chance of getting an emote message to run North, South, West, or East ***OR*** to DUCK. Not listed in the quest
  detail above so be ready." (Nov 2007 comment [V]). The exact DUCK wording is UNCONFIRMED.
- Hit on you: `SPLAT! You are covered in warm gooey squash pie, better go clean up!` - the scarecrow illusion is removed
  and the throw step stops counting until Marta re-costumes you (Bonzz: "If you do not avoid the pie, the pie will hit you
  and your scarecrow illusion will be dispelled ... you will need to start over, by going back to Marta ... and saying
  'Costume'"). Whether the 0/10 count resets is UNCONFIRMED (Bonzz "start over" suggests yes).
- Step 3 wording ("don't get hit on the way!") means you can still be hit while walking back.
- Tactics from comments: "Standing beside mobs facing north prevents aggro" (Sheldor 2018 [P]); "a large concentration of
  scarecrows at -323, -99; found 10 targets without relocating" (ArahgornCrystalclaw, Nov 2007 [P]); "It is so much easier
  to go against other players. Player 2 just stands there and takes the abuse, and re-requests the task with 'try' and
  'costume' after each hit, while Player 1 racks up hits without all the running around and ducking nonsense." (nytmare,
  Oct 2017 [V]). Bonzz: the pie mobs are "near the wall".
- **Geometry note**: ArahgornCrystalclaw's 2007 /loc (-323, -99) matches peq's pie-thrower spawn (x=-99, y=-303) in
  classic `tox`, while Marta's live /loc (1987, -739) is on the "Toxxulia Forest 2.0" map. Whether the 2007 event ran in
  classic tox or the rebuilt zone is UNCONFIRMED.
- peq: 18 pie mobs (npcs 38175 flinger / 38176 hurler / 38177 thrower: level 1, race 82 scarecrow, class 1, gender 2,
  hp 11, respawn 90 s) in classic tox between /loc (-1012..-59, -800..517).

### Items
| Item | Live id | Flags / data |
| --- | --- | --- |
| Stack of Squash Pies | **80038** (Allakhazam 68282) | EQ Resource: Lore, Quest. TINY, WT 0.8. Effect Throw Pie, instant, recast 5 s; unlimited charges (Allakhazam "unlimited charges of Throw Pie"). peq: loregroup -1, questitemflag 1, nodrop 1 (tradeable), clicktype 5, clickeffect 11575, **scriptfileid 8808**. Bonzz: "You also get to keep the Stack of Squash Pies." |
| Tasty Squash Pie (reward **x10**) | **80044** (Allakhazam 69370) | EQ Resource: no flags (tradeable), SMALL, WT 0.2, stack 20, "enduring meal (55)". HP 20, Mana 20, STR 15, STA 15, INT 15, WIS 15, **CHA -10**, SvCold 10. Lore "Useful for curing hunger, and scolding lazy husbands". peq agrees (price 5). Allakhazam reward line: "10x Tasty Squash Pie". |

Spell 11575 "Throw Pie" (peq): targettype 8 (targeted AE), range 150, aoerange 30, cast 3000 (item makes it instant),
recast 1500, buffduration 4, SE 10 placeholder. The hit/miss/dodge logic is scripted (item script 8808 is not in the
ProjectEQ repo).

---

## 2. Nights of the Dead: Nektulos Ghost Rider (Allakhazam quest 4317)

### Header (Allakhazam [V])
- Level 1, max 125. Solo (1-1). Task. Added Nov 1, 2007. Header "Repeatable: No"; failures can be retried with [try]
  (below). Whether a success can be repeated on live is UNCONFIRMED (peq: repeatable).
- **Time limit: 4 minutes** from "ready" to the tenth checkpoint (Grom's own words, below).
- peq task **3540** "Nektulos Ghost Rider" (levels 1-85, reward_text "Loot", description "Reach the gates of Neriak in 4
  minutes."). The ProjectEQ Mask of Eyes script refers to task 3540.

### Giver: Grom Shives (Allakhazam npc 26664)
- Allakhazam zone label **"Nektulos Forest 3.0"**, **/loc -1915, +1205** "Southwest corner"; quest page -1915, 1200; Bonzz
  "southwest corner of the zone (area of /waypoint -1920, 1210 )". Findable with Ctrl-F.
- Level 60 (Allakhazam). Look (screenshot, my read): **Dark Elf**, bald, blue skin, probably male; dark blue padded armour
  with red trim. Screenshot https://zam.zamimg.com/images/a/0/a02e725e40c6c6deb0901b44ae0fc0e3.jpg
- peq npc 25436 `Grom_Shives` (lastname 'Halloween Quests', level 50, race 485, class 12, gender 2, helm 255).
  peq spawn2 137449: nektulos **version 1**, x=1200, y=-1915 (matches live). See the zone-version note below.

### Dialogue ([V]: two fetches; the second returned every line in full)
```
You say, 'Hail, Grom Shives'
Grom Shives says 'Have you also come to stand [vigil] on this day of grim history?'
You say, 'Vigil?'
Grom Shives says 'Ah, I see you are not familiar with the vigil for Ritrim Shives, my ancestor who cheated the creatures that dwell below the forest roots and lived to tell the [tale].'
You say, 'Tale?'
Grom Shives says 'The Tale is a horrifying one... in exchange for the life of his only child, these creatures agreed to bestow upon Ritrim a dark and terrible [power].'
You say, 'Power?'
Grom Shives says 'The power to harm any living creature with a mere touch of the hand.. After a gruesome ceremony, when he was granted the dark power, he acted quickly and used his new power to slay the creatures even as they prepared to sacrifice his child, and feast upon his flesh... in his haste to subvert the agreement, Ritrim failed to realized the [toll] that the power would take upon him.'
You say, 'Toll?'
Grom Shives says 'Using his new power drained his energy, leaving him weak and vulnerable. With his son, he moved towards his mount, a powerful black warhorse, a single enemy blocked his path... Ritrim reached out again with his power, killing his foe, but not quickly enough... a shout was given, and he felt a searing pain as his [eyes] were burned away.'
You say, 'Eyes?'
Grom Shives says 'Blinded, and in great pain, Ritrim mounted his steed to make his escape, the voice of his son guiding him as he charged through the forest of Nektulos weaving a [crooked path] in order to evade his pursuers, and return to Neriak.'
You say, 'Crooked path?'
Grom Shives says 'If you are really that interested, I will summon you a dark [mount] so that you may follow the path for yourself.'
You say, 'Summon me a mount.'
Grom Shives says 'When you are [ready], I will give you a mask with eyes to guide you along the path, ride with haste and reach the gates of Neriak before the fourth minute has passed.'
You say, 'I am ready.'
Grom Shives says 'This will be your only guide, ride quickly and do not hesitate... Remember, you have only four minutes to reach the gates of Neriak.'
```
- Live typos kept: "mere touch of the hand.." and "failed to realized".
- Items: you receive **Bridle of the Cursed** at the [mount] step and **Mask of Eyes** at [ready] (Allakhazam [P]; Bonzz
  agrees). The exact "You have been assigned" moment is UNCONFIRMED (task step 1 is "Let Grom know when you are ready to
  begin", so the task is assigned before "ready", most likely at "Summon me a mount").
- Success [V]: `Amazing! You rode swiftly and true... few could rival your speed! Take this cloak, and wear it to
  commemorate this day.`
- Failure [V]: `You managed to find your way through Nektulos to Neriak, but you did not as quickly as you could have...
  Let me know if you would like to [try] again.` (Bonzz: "If you fail, you can say 'Tray again,'" [sic].)

### Task steps (Allakhazam [V])
1. `Let Grom know when you are ready to begin 0/1`
2-11. `Reach the first checkpoint 0/1` ... `Reach the tenth checkpoint 0/1` (ordinal words "first" .. "tenth")
12. `Return to Grom and report the speed of your ride 0/1`

peq task_activities 3540: activities 0-9 are type 5 (explore) in zone 25, activity 10 is "speak with Grom Shives"; there
is no "let Grom know" step and no 4-minute timer in the task row (duration 0).

### Checkpoints (all sources agree once the axis order is fixed)
Labels are from Kuponya's Nov 3 2007 guide (Allakhazam [P]) and Bonzz.

| # | Landmark | ProjectEQ Mask of Eyes script (world x, y) | /loc (Y, X) | Allakhazam map line (-X, -Y) | Bonzz /waypoint |
| --- | --- | --- | --- | --- | --- |
| 1 | sculpture with two halflings | 1035, -1110 | -1110, 1035 | -1027.14, 1116.78 | -1100, 1035 "near a statue" |
| 2 | undead statue, south-east corner | -890, -1910 | -1910, -890 | 886.92, 1904.86 | -1900, -885 "near a statue" |
| 3 | the Nektulos bridge | 25, -1195 | -1195, 25 | -24.71, 1178.61 | -1190, 30 "bridge" |
| 4 | skinny white tree ("slow down") | 1045, -505 | -505, 1045 | -1029.64, 512.28 | -500, 1050 "right up at a tree" |
| 5 | Leatherfoot camp, atop a tree stump | 530, 890 | 890, 530 | -523.22, -879.56 | 870, 525 "at a tree stump" |
| 6 | hill in the corner | -530, -865 | -865, -530 | 530.97, 875.18 | -870, -525 "on a hill" |
| 7 | north-east end of the wizard spire | -760, 0 | 0, -760 | 755.29, -23.41 | -5, -755 "near the Wizard spire" |
| 8 | the newbie log | -75, 860 | 860, -75 | 119.50, -876.24 | 865, -75 "at the 'newbie' log" |
| 9 | rock outcropping ("snowman") | 700, 1685 | 1685, 700 | -717.12, -1699.47 | 1680, 700 "at some rocks" |
| 10 | Neriak entrance (do NOT zone) | -950, 1820 | 1820, -950 | 943.56, -1833.42 | -1825, -955 (Y sign wrong on Bonzz) |

- Ishtass (Oct 31 2015 [P]): fifth checkpoint "should be POS 890, POS 530" = /loc (890, 530), agrees with the table.
- Diani (Oct 15 2017) posted a map-file correction for checkpoint 5 [P].
- **Zone version.** These positions match peq's **nektulos version 1** (the rebuilt "Nektulos Forest 3.0"): peq's Neriak
  zone line drops you into nektulos instance/version 1 at x=-977, y=1824 (= checkpoint 10), but into version 0 (classic)
  at x=-1108, y=2300. Grom also spawns only in version 1 in peq. **So live runs this quest in the rebuilt Nektulos, and
  classic Nektulos geometry would need new checkpoints.** (Whether live already used the rebuilt zone in 2007: UNCONFIRMED;
  the Allakhazam map lines date from 2015-2017 comments.)

### Mechanics (comments)
- Kuponya, Nov 3 2007 [V]: "This quest is a HORSE RACE against the clock using a black nightmare horse with fast speed
  (Abyssal Steed)." / "You need to hit 10 check points, in correct order, within Nektulos Forest, inside 4 minutes." /
  "The reward is a cloak with 10-charges of 'Spirit of Eagle' usable at level 15." / "I think this is a fresh take on the
  'explore' style quests and adds a short, virtual 'driving' game to EQ." Also [P]: the Abyssal Steed vanishes if it
  touches water (use the bridge), keep speed buffs up, practise the route; a full attempt takes "5-6 minutes from start
  to finish".
- nytmare, Oct 23 2017 [V]: "A good run is 3:20, a not-so-good run is 3:30, so there is some spare time for missed
  markers or other mistakes. Do not zone into Neriak at the last marker — that will cause a fail every time."
- Nov 5 2007 [P]: a level 73 bard finished on foot with Selo's Song of Travel ("I had tried many times on my druid on the
  horse, but this was the first time I was successful"; "I do not think it could be done by someone autofollowing a bard.
  Too many obstructions to break the autofollow.").
- Bonzz: "it appears that you do not actually have to use the Mask of Eyes. So long as you hit all ten (10) update spots
  (mount or no mount... or any mount) in the four allotted minutes time, you should be good." "The Mask of Eyes can be
  clicked (spam click it) to provide some direction on which way to run." "If you would this mount to keep, after you have
  completed this task, you can go back, get the Mount and not complete the task." (UNCONFIRMED; the Bridle is a 1-charge
  item on live.)
- Nov 2 2007 [P]: "Expendable quests are annoying...not rechargeable" (about the cloak's charges).

### Items
| Item | Live id | Flags / data |
| --- | --- | --- |
| Bridle of the Cursed | **80039** (Allakhazam 69375) | EQ Resource: Lore, Quest. TINY, WT 0.8. Effect **Abyssal Steed**, any slot, cast 1 s, **expendable 1 charge**. Lore "Summons a nightmare from the past". peq: nodrop 1, questitemflag 1, clicktype 3, clickeffect 8978, scriptfileid 8809. Not the same item as "Bridle of the Cursed Kirin" (40679). |
| Mask of Eyes | **80043** (Allakhazam 69386) | EQ Resource: Lore, Quest. TINY, WT 0.8. Item text: "A mask with a single eye to guide you along the path of Ritrim Shives in Nektulos. Right click to have it guide you." peq: scriptfileid **8819**. |
| Cloak of Death (reward) | **80056** (Allakhazam 69374) | EQ Resource: Lore, No Trade. Slots Ammo, Back. SMALL, WT 0.2. Effect **Spirit of Eagle** (Req Lvl 15), any slot, cast 2 s, recast 60 s, **expendable 10 charges**. Lore "Black and sleek, enfolds the wearer in darkness". peq: clickeffect 2517, clicktype 3, price 5. |

Spells (peq): **8978 "Abyssal Steed"** self, SE 113 (summon horse) with teleport_zone `SumNightmareFast`, buffduration
3600. **2517 "Spirit of Eagle"** single target, range 100, SE 3 movement +30 and SE 57 levitate, `Your body pulses with an
avian spirit.`

### ProjectEQ Mask of Eyes script (`global/items/script_8819.pl`, not live text)
- Only works in `nektulos`; checks `istaskactivityactive(3540, N)` for N = 0..9 and prints a compass direction to the next
  checkpoint: `The waypoint lies to the NorthWest.` (and NorthEast, North, SouthWest, SouthEast, South, West, East).
  Outside Nektulos: `This item can only be used in Nektulos Forest.`; after the last point: `This item can no longer help
  you as there are no more waypoints.` These messages are ProjectEQ's own; the live text is UNCONFIRMED.

---

## 3. Could NOT find (not guessed)
1. Pie Fling: the exact DUCK message; the message on a successful dodge; whether a hit resets the 0/10 count; the reply to
   [try]; XP amount; whether the 2007 event used classic or rebuilt Toxxulia; Marta's classic-zone spot.
2. Ghost Rider: whether a completed run can be repeated; the live Mask of Eyes messages; what happens at the 4-minute mark
   mid-run (fail message only quoted for a slow finish); exact "assigned" line position; Grom's race/gender code.
3. Both: live task ids (3539/3540 are peq ids, probably live).

## Sources
- Allakhazam quests: https://everquest.allakhazam.com/db/quest.html?quest=4319 , ?quest=4317 , achievement ?quest=8833
- Allakhazam NPCs: https://everquest.allakhazam.com/db/npc.html?id=26717 (Marta), 26714 / 26715 / 26716 (pie mobs),
  26664 (Grom Shives); search https://everquest.allakhazam.com/search.html?q=Grom+Shives
- Screenshots: https://zam.zamimg.com/images/d/d/dd8581ee6e7ec44fcc3d63364b88b04e.jpg (Marta),
  https://zam.zamimg.com/images/a/0/a02e725e40c6c6deb0901b44ae0fc0e3.jpg (Grom) (local copies `scratchpad\notd\web\img\`)
- EQ Resource live items: https://items.eqresource.com/items.php?id=80038 , 80044 , 80039 , 80043 , 80056
- Bonzz: https://www.bonzz.com/nightsofthedead.htm (2007 #1 and #4)
- Official news: https://www.everquest.com/news/imported-eq-enus-51169 (Oct 22 2008), https://www.everquest.com/news/imported-eq-enus-52055 (Oct 22 2010)
- Patch notes 2007 (generic Halloween line): https://github.com/nazwadi/patcheq (local `scratchpad\notd\raw\patches\p-2007-2.txt:399`)
- ProjectEQ: https://github.com/ProjectEQ/projecteqquests `global/items/script_8819.pl` (clone 2124cc0); local peq dump
  (items, spells_new, npc_types, spawn2, spawnentry, tasks, task_activities, zone_points)
