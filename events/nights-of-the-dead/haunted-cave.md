# Nights of the Dead: Haunted Cave (live EverQuest) - rebuild research

Gathered 2026-10-05. Read-only: web pages, the PEQ dump in `scratchpad\notd_web\peq-dump` (2025-09-28 export),
the PEQ quests clone in `scratchpad\notd_web\peqquests` (ProjectEQ/projecteqquests @ 2124cc0f, 2026-09-21), the
patch notes clone `scratchpad\notd_web\patcheq` (nazwadi/patcheq), map files, and SELECT-only queries on the local
`peq` DB. Nothing under C:\Git\test was changed.

**Quote reliability.** Allakhazam blocks raw downloads, so every Alla quote below came through WebFetch, which runs
the page through a summarizing model. I fetched the key comment (Nov 05 2009, the only full play-through) three
times and asked for a character-for-character copy. The text came back the same each time and keeps the poster's
typos ("Jillian Floratine"). It is probably verbatim, but treat it as **possibly paraphrased**. Items marked [P]
were clearly summarized and are not verbatim.

---

## 1. Quick facts

| Field | Value | Source |
| --- | --- | --- |
| In-game task name | **Haunted Cave** ("You have been assigned the task 'Haunted Cave'.") | Alla NPC 26733 comment, Nov 05 2009 |
| Alla name | Nights of the Dead: Haunted Cave (quest=4904) | Alla |
| Type | Task, solo (group size 1) | Alla quest 4904 |
| Level range | 20-90 | Alla quest 4904; Alla wiki EQ:Halloween gives min 20 |
| Repeatable | **No** (one completion per character). After finishing, Jilian says "I'm sorry I dont have anything for you right now". | Alla quest 4904 comments, Nov 07 2009 (two posters) |
| Time limit | None reported | not found anywhere |
| Lockout / replay timer | None reported (not repeatable at all) | n/a |
| Zone | Crescent Reach (`crescent`, zone id 394, PEQ expansion 12 = TSS) | local DB `zone` |
| Era tag on Alla | Serpent's Spine | Alla |
| Reward | **5x Pirate's Gold** (snack) + experience (amount unknown) | Alla 4904 + Nov 05 2009 comment ("You gain experience!!") |
| Achievement | One of the 9 parts of "Nights of the Dead: The Monster Mash" (Alla 8832; EQR achievements id 200105) | halloween_inventory.md |

---

## 2. Year added: settled as 2006

The sources disagree: the Alla quest page says "introduced in October 2009", Bonzz files it under 2009 (#6), and
the Alla wiki EQ:Halloween table says 2006.

**Evidence for 2006:**
1. The Oct 30, 2006 patch note is the first Halloween patch after The Serpent's Spine launched (TSS added Crescent
   Reach, patches-2006-2.txt:35). It says: "Folks in need of assistance have been taking refuge within the Plane of
   Knowledge and Crescent Reach. The festivities kick off tonight at midnight PST..." (patcheq `patches-2006-2.txt`
   lines 507-518).
2. Comments on the ZAM copy of that patch note (https://legacy.fanbyte.com/story.html?story=8196):
   - Oct 31 2006 6:43 AM, `__DEL__1592278481314`: "Jilian Florantine, next to the water wheel. Aragol Gloomflow, in
     the undead cave."
   - Oct 31 2006 10:18 AM, `__DEL__1592763295172`: "Anyone else got any tasks ... so far here is what ive seen
     Pralak The Bone Collecter, Jillian Florantine, and Aragol Gloomflow in Crescent Reach a wizened hermit, and the
     toffee apple task in POK"
3. Allakhazam's own NPC database lists "NPC Added" as 2007-11-07 for all three quest NPCs: Jilian Florantine
   22:17:52, Ghost of All Hallows Eve 22:17:07, and Shadow of All Hallows Eve. All three, ghosts included, were
   already in the game during the 2007 event.

**Conclusion:** Jilian has stood by the waterwheel since Nights of the Dead **2006**, and the ghost mobs existed by
**2007** at the latest. The "October 2009" on Alla is when Alla wrote up the quest page: quest ids 4898-4904 were all
written up together in 2009, and the first comments are from Nov 2009. Nothing found shows that her 2006 task had the
same steps as the 2009 write-up. That gap is still open.

Aragol Gloomflow was seen the same day (Oct 31 2006). His Alla quest page says "introduced in October 2007", and his
Alla NPC record was added 2008-08-29. The 2006 forum comment beats both dates, so Aragol is 2006 too.

---

## 3. NPCs

### 3.1 Jilian Florantine (quest giver)

| Field | Value | Source |
| --- | --- | --- |
| Name | `Jilian Florantine`, one L. An Alla comment from Oct 25 2018 says the name is Jilian, as in the screenshot. Alla's text and players often misspell it "Jillian". | Alla NPC 26733 |
| Surname (title line) | 2009 screenshot: "(Halloween Quests)". 2019 screenshot: "(Nights of the Dead Quests)". | zam screenshots below |
| Level | 22 | Alla NPC 26733 |
| Race | **Not stated in any text.** In both screenshots the head is normal-sized (Erudites have a large cranium), with a jewel or marking on the forehead. I read it as **Drakkin (522)**, but that is my reading of the image only. | screenshots |
| Gender | Text calls her "she" (2009 comment). The screenshots look male to me. **Unresolved.** | Alla comment vs image |
| Look | Long dark-purple/black robe with red-pink trim and a purple glow pattern, sandals, short dark hair. She holds a **scythe** in the primary hand. | screenshots |
| Spawns | "Spawns only during Nights of the Dead period" [P] | Alla NPC 26733 |
| Location (Alla) | "+314, -2119 - by the waterwheel next to the large building full of undead" (comment Nov 05 2009). NPC page: "+312, -2120 in the undead area outside a house by the river" [P]. | Alla |
| Location (Bonzz) | "/waypoint 315, -2125", "near a building near the river" | bonzz.com |
| Location (map label) | Good's Maps `crescent_2.txt`: `P 2121.0884, -312.2162, -105.7981, 127, 64, 0, 2, Jilian_Florantine_(Q)` | scratchpad\notd_web\gmaps |

**Coordinate order (verified).** The Alla and Bonzz numbers are in **/loc order (Y, X)**. Checks:
- Aragol: Alla gives "+527, -2668" and Bonzz "/waypoint 525, -2670". The PEQ spawn2 row (#142515, group 104055,
  flag `peq_halloween`) has **x = -2666.09, y = 535.59**, z = -63.97, heading 85.25. So the first number is Y.
- Map-file labels store (-X, -Y, Z). Good's Maps puts Aragol at `P 2669.27, -528.01, -66.90`, i.e. x = -2669,
  y = 528, which matches spawn2.
- Jilian's label `P 2121.09, -312.22, -105.80` gives **server x = -2121.1, y = 312.2, z = -105.8**. That agrees
  with Alla's (Y 314, X -2119).
- The waterwheel: local DB `doors` row 14124 `OBJ_PADDLE` sits at x = -2166.94, y = 340.25, z = -94.19, about 50
  units from that spot. This matches the "by the waterwheel" wording.

**For a spawn2 row:** x = -2121, y = 312, z ≈ -105.8 (the map label's z; snap to ground). No live heading is known.

Screenshots:
- https://zam.zamimg.com/images/c/8/c80a3ea1ffe9e6f3fef28047e2dd3368.jpg ("Nights of the Dead Quests" title,
  uploaded Oct 11 2019 by Drewinette; thumb .th96.png)
- https://zam.zamimg.com/images/2/a/2ad69b066c9d250f54d11d6e79c955c4.jpg ("Halloween Quests" title, 2009 comment)
- Local copies are in `scratchpad\notd_web\img\hc_*.jpg`.

### 3.2 Shadow of All Hallows Eve (boss, kill target)

| Field | Value | Source |
| --- | --- | --- |
| Name | `Shadow of All Hallows Eve` (no apostrophe) | Alla NPC 26731 + screenshot |
| Level | 22 | Alla 26731 |
| Max hit | 44 (Alla). A user reports a 73 hit, "not too much different" [P]. | Alla 26731 |
| Behavior | Flees at low health. Kill on sight (KOS). | Alla 26731; Nov 05 2009 comment ("They're all KOS") |
| Look | Hooded, robed humanoid spirit with a **tan/dirty-white** robe texture. Players call it "Erudite spirits". The model matches race **118 EruditeGhost** (my match from the screenshot). The comment calls it "a large Shadow", so it is bigger than the ghosts. | screenshot https://zam.zamimg.com/images/0/d/0da8152184c628a82b29135bddee5642.jpg (uploaded Nov 4 2011 by Railus) |
| Spell / proc | "may have an illusion proc or spell that turns you into an erudite spirit .. (this happened to my pet, but I was unable to recreate it with a friend)" | Nov 05 2009 comment |
| Candidate spell | **3090 "Call of All Hallow's Eve"** (PEQ dump and local DB). Effects: SE 127 base -40; **SE 58 Illusion race 118 (Erudite Ghost)**; SE 11 attack speed 60 (40% slow). Single target (targettype 5), range 300, 0 cast time, 15 s recast, duration formula 11 / 5 ticks, resisttype 0, uninterruptable, no_partial_resist, nodispell. Messages: "Poisoned hatred invades your body." / "'s body is consumed in poisoned hatred." / "The poisoned hatred fades away." No PEQ `npc_spells_entries` row uses it. The match to the Shadow's illusion is **my inference** from the spell name and the race-118 illusion, not a confirmed live link. | PEQ dump / local `spells_new` |
| Drops (Alla) | Sullied Silk (Alla item 68295), Thalium Ore (Alla 68298) | Alla 26731 |
| Spawn | Haunted side of the Nokk cave (see 4.2). It sits among a "bundle" of ghosts. No coordinates. | Nov 05 2009 comment |
| Respawn | A 2012 comment: "I had someone come in and snag out the boss and then it never reset even after I got a new quest." This suggests one shared world spawn on a long or event-only respawn, not a per-player spawn. Not confirmed. | Alla 4904, dylothe, Oct 22 2012 |

### 3.3 Ghost of All Hallows Eve (adds)

| Field | Value | Source |
| --- | --- | --- |
| Name | `Ghost of All Hallows Eve` | Alla NPC 26732 |
| Level | 20 | Alla 26732 |
| Count | "a bundle of little Ghost of All Hallows Eve". The exact count is unknown. | Nov 05 2009 comment |
| Look | The same hooded robed spirit model in a **white/grey translucent** texture, smaller than the Shadow. Race 118 match (my reading). Screenshot: https://zam.zamimg.com/images/8/a/8ab52ac4ec946e86637a0ccea8c813a8.jpg | Alla 26732 |
| Behavior | KOS. Getting close to any of them updates step 1. | Nov 05 2009 comment |
| Drops (Alla list, ids are Alla's) | Bone Chips 2754, Fine Bone Powder 56455, Fine Steel Great Staff 492, Fine Steel Rapier 654, Large Cloth Cap/Cape/Choker/Cord/Gloves/Pants/Sandals/Shawl/Shirt/Sleeves/Veil/Wristband (22917-22928), Large Raw-Hide Gorget 22261, Large Raw-Hide Sleeves 22266, Makeshift Binding Powder 70234, Putrid Skeleton Bones 52027, Reinforced Incendiary Chestguard 52073, Rotting Zombie Flesh 54567, Salty Loam 68324, Skeleton Parts 77666, Zombie Skin 7772. | Alla 26732 |

This drop list is the Nokk-cave undead table plus holiday items: Fine Bone Powder is Aragol's quest drop, and
Skeleton Parts is the Monster Mash quest drop. It looks as if the ghosts reuse the cave's undead loot table. In PEQ,
the Aragol drops sit in lootdrops 90606 `90163_a_rotting_corpse_` (Foul Ichor Residue 87298 + Fine Bone Powder 87299,
20% each) and 90607 `90142_a_risen_elder_` (87298, 20%).

### 3.4 Not in PEQ or our DB

- **ProjectEQ quests:** `crescent/` has no Jilian script. A repo-wide grep for jilian / florantine / "haunted cave" /
  "all hallows" / "hallows eve" found nothing. The only Halloween script in crescent is `#Aragol_Gloomflow.pl`.
- **PEQ dump:** no npc_types row for Jilian, Ghost of All Hallows Eve or Shadow of All Hallows Eve. No task titled
  Haunted Cave. Unrelated rows: `##Eve_Hallows` 20259 (a level-70 invulnerable GM-type NPC) and `Halloween_Trigger`
  63109.
- **Local `peq` DB (SELECT only):** same result. Only Aragol (394263) and task 5656 "Aragol's Seance" are present.
  Pirate's Gold 87314 exists as an item.

Everything for Haunted Cave (NPCs, spawns, task, script) has to be built new.

---

## 4. Dialogue and walkthrough

### 4.1 Dialogue

Source: Alla NPC 26733, comment by `__DEL__1592791055003`, **Nov 05 2009 4:55 AM** (probably verbatim, see the
reliability note at the top). The same four lines appear on the Alla quest page.

```
This NPC can be found at +314, -2119 - by the waterwheel next to the large building full of undead

She gives the quest Haunted Cave

You say, 'Hail, Jillian Florantine'

Jillian Florantine says 'Traveller, how did you find me? Ghosts have mysteriously begun running rampant up the hill here in the [cave of the dead].'

You say, 'What cave of the dead?'

Jillian Florantine says Yes.. The cave just up the hill here. Would you be [willing] to see if you can figure out what is causing the disturbance?'

You say, 'I am willing'

Jillian Florantine says 'Great, return to me when you have figured out what evil is brewing down there.'

You have been assigned the task 'Haunted Cave'.

Figure out why the undead cave has become haunted 0/1 Crescent Reach

This cave is the Nokk cave, entrance at +676, -2416; you need to head down to the opposite side of where you find the 'discarded bones' for the Charm of Lore .. the other side has a bundle of little Ghost of All Hallows Eve, and a large Shadow of All Hallows Eve. They're all KOS and look like Erudite spirits. When you approach any of them, the task will update.

Kill the Shadow of All Hallows Eve 0/1 Crescent Reach

Kill the big ghost and the task updates again. The Shadow of All Hallows Eve may have an illusion proc or spell that turns you into an erudite spirit .. (this happened to my pet, but I was unable to recreate it with a friend)

Return to Jillian Floratine 0/1 Crescent Reach

You say, 'Hail, Jillian Florantine'

Your task 'Haunted Cave' has been updated.
You have completed the task, 'Haunted Cave'
You gain experience!!

Jillian Florantine says 'Great work! I knew you could do it. Thank you for your assistance, it will not go unnoticed.'

The reward is 5 snacks named Pirate's Gold.
```

NPC lines for the script ("Jillian" is the poster's spelling; the NPC's name is Jilian):

| Trigger | Line |
| --- | --- |
| hail (task not held) | "Traveller, how did you find me? Ghosts have mysteriously begun running rampant up the hill here in the [cave of the dead]." |
| `cave of the dead` | "Yes.. The cave just up the hill here. Would you be [willing] to see if you can figure out what is causing the disturbance?" (the opening quote is missing in the source) |
| `willing` | "Great, return to me when you have figured out what evil is brewing down there." + task assigned |
| hail with step 3 active | completes the task, then "Great work! I knew you could do it. Thank you for your assistance, it will not go unnoticed." |
| hail after completion | "I'm sorry I dont have anything for you right now" (quoted inside the Nov 07 2009 comment; this may be the client's generic no-task text rather than a scripted line) |
| hail while steps 1-2 active | **Unknown.** No source records it. |

The player's keyword lines "What cave of the dead?" and "I am willing" fit an auto-say from the bracketed links. The
NPC lines rely only on the keywords `cave of the dead` and `willing`.

### 4.2 Task steps (in-game text, from the same comment)

| Step | Objective text (verbatim per comment) | Count | How it updates | Zone |
| --- | --- | --- | --- | --- |
| 1 | Figure out why the undead cave has become haunted | 0/1 | **Proximity/explore**: "When you approach any of them [the ghosts/Shadow], the task will update." | Crescent Reach |
| 2 | Kill the Shadow of All Hallows Eve | 0/1 | Kill | Crescent Reach |
| 3 | Return to Jillian Floratine (sic; probably "Jilian Florantine" in game) | 0/1 | Hail/speak to Jilian. Her hail updates and completes the task ("Your task 'Haunted Cave' has been updated." then completed). | Crescent Reach |

The steps show one at a time ("0/1" for each as it appears), so they are sequential.
Bonzz describes step 1 as: "head into the nearby 'Nokk' cave (area of /waypoint 675, -2420), for a location update,
where you will see Ghost of All Hallows Eve and Shadow of All Hallows Eve." Bonzz places the update at the cave
**entrance area**. The 2009 comment ties it to approaching the ghosts. These may simply be different players' views
of the same update.

### 4.3 Locations inside the cave (PEQ spawn2, server x/y/z)

- Nokk cave entrance: Alla "+676, -2416" and Bonzz "675, -2420", i.e. **x ≈ -2418, y ≈ 676**. a_Nokk_elder spawn2
  #76760 stands at x -2417.88, y 776.25, z -55.1.
- Aragol Gloomflow: x -2666.1, y 535.6, z -64.0 (spawn2 #142515).
- "discarded bones" ground spawn for the Charm of Lore (Broken Nokk Insignia): PEQ spawn2 #76881 (npc 394149
  `discarded_bones`) at **x -2919, y 460, z -114.5**. Brewall: `GS:_Discarded_Bones` at map 2913.0, -460.9, -115.2.
  Good's: `CoL:Broken_Nokk_Insignia`.
- The Nokk cave spawns in PEQ cover roughly x -2170 to -2920, y 250 to 860. The upper level is around z -40 to -76,
  the lower level around z -111 to -115.
- **Haunted area:** "head down to the opposite side of where you find the 'discarded bones'". This means the lower
  level (z ≈ -111), on the other side from (-2919, 460). The lower-level PEQ spawns are at x -2741 to -2877 and
  y 254 to 564. The "opposite side" is probably the y ≈ 250-350 end (-2770..-2818, 254..344). That is my inference;
  **no exact live coordinates exist** for the ghosts or the Shadow.

---

## 5. Items

| Item | Live id | Flags | Stack | Stats / effect | Source |
| --- | --- | --- | --- | --- | --- |
| **Pirate's Gold** (reward x5) | **87314** (PEQ dump + local DB). Alla's page is item=61077, but that is Alla's internal id: PEQ 61077 is "Harmonic Disruptor". The icon matches (645 in both Alla and PEQ). | **NO TRADE** (PEQ nodrop=0; Alla "No Trade"); not temporary (norent=1); magic=1; not lore; not quest-flagged | 20 (stackable) | Food (itemtype 14), "This is a snack!" (casttime_ = 4). STR +6, INT +8, WIS +8, CHA +3, HP +70, Mana +60, SV Cold +3, SV Magic +5, SV Poison +7. Lore text "Hidden beneath a golden shell". WT 0.0, size TINY, all classes and races. No click effect. reqlevel 0 in PEQ; Alla's stat box shows no required level. Icon 645, idfile IT63, created 2015-11-28 (source 13THFLOOR). | PEQ dump row; Alla item 61077; Bonzz |

No other items are involved. The task hands out nothing at the start and needs no turn-in. Step 3 is a hail.
On completion live also grants unspecified experience.

---

## 6. How it connects to Aragol's Seance (Alla 4623)

- **Same place, same night.** Both NPCs were reported together on Oct 31 2006, the night of the 2006 event (see
  section 2). Aragol stands **inside** the Nokk cave (x -2666, y 535.6, z -64; Alla "+527, -2668 in the Nokk
  caves"; Alla quest: "Nokk Cave (northernmost cave)"). That cave is the one Jilian sends players into ("the cave just
  up the hill here").
- **Same "undead cave".** Aragol's materials (Foul Ichor Residue, Fine Bone Powder) drop from the cave's undead
  (risen/Nokk elders, mummified/rotting corpses). The Haunted Cave ghosts' Alla drop list includes Fine Bone Powder,
  so the ghosts appear to share that undead loot.
- **Sister rewards.** Fiery Rock Candy 87313 (Aragol, 5x per Alla, but `summonitem(87313, 20)` in the PEQ script) and
  Pirate's Gold 87314 (Jilian, 5x). The ids are consecutive, both have the same created/updated stamps, both are
  20-stack No Trade snacks with similar stats.
- **Same achievement.** Both count toward "Nights of the Dead: The Monster Mash".
- **No quest dependency.** Neither task requires or flags the other. Haunted Cave is once per character; Aragol's
  Seance is repeatable.
- **PEQ's Aragol vs live.** PEQ (`peqquests/crescent/#Aragol_Gloomflow.pl`, task 5656, spawn behind content flag
  `peq_halloween`) has the hail and `help` lines only, plus a 10-minute "Trick or treat! Smell my feet!" shout.
  Live's completion scene (per Alla 4623, possibly paraphrased) is missing from it: "Rise up my love, rise!" /
  "I... Iris, can you hear me?" / *Iris Gloomflow appears* "I am here, Aragol. I have been watching over you." /
  "Iris.. I was never able to tell you how much I love you my darling. Please don't go." / "I must go Aragol.. Don't
  worry about me, you have your own life to worry about now. We will be together again soon. I love you." /
  *Iris disappears* "No... Wait! Don't go!" / "She's gone.. I can't believe she's gone again. I must go to her.
  Thank you for all you have done, ____. I will see to it that you are well taken care of." PEQ's reward count (20)
  also differs from Alla's 5. (Flagged only; out of scope here.)
- **PEQ task 5656 as a template** (types per EQEmu): activity 0 = loot (type 3) Foul Ichor Residue 87298 from
  "Undead creatures", zone 394, step 1. Activity 1 = loot Fine Bone Powder 87299, step 1. Activity 2 = tradeskill
  combine (type 6) Pouch of Ethereal Essence 87308, step 2. Activity 3 = deliver (type 1) to "Aragol Gloomflow",
  goalmethod 2 (script-updated), step 3. Task type 2, repeatable 1, reward_method 2, reward text "Fiery Rock Candy".

---

## 7. Our era / scope notes (facts only)

- Crescent Reach is a TSS zone (local `zone.expansion` = 12). This quest is outside a GoD-capped server unless the
  zone is open or the quest is moved (this was already noted in halloween_inventory.md).
- Levels: Jilian 22, ghosts 20, Shadow 22. Task range 20-90.

---

## 8. Could NOT find

1. **Experience amount** of the reward ("You gain experience!!" only).
2. Jilian's line when hailed **during** steps 1-2 (if she has one), and whether the "I'm sorry I dont have anything
   for you right now" line is hers or the client's generic text.
3. **Live coordinates** of the ghosts and the Shadow. Only "opposite side of the discarded bones, down" is known.
   Also unknown: the number of ghosts, their respawn timers, and whether the Shadow spawns per player or is one
   shared world spawn (a 2012 comment suggests shared and slow to reset).
4. The exact **trigger** for step 1: a proximity radius around the ghosts (2009 comment) or an explore box at the
   cave mouth (Bonzz). No size is known.
5. Jilian's **race and gender** in text form. The screenshots suggest Drakkin and look male, while the text says
   "she". Her heading is also unknown. Her z is taken from a map label.
6. The ghosts' and Shadow's **race id, texture, size, HP, AC, attack delay, resists and special abilities**. Only
   the levels, the Shadow's max hit (44, one report of 73) and "flees" are known; the race-118 Erudite Ghost match
   comes from screenshots. Also unconfirmed: the Shadow's illusion spell id. Spell 3090 is a candidate only.
7. Whether the 2006 version of Jilian's task matched the 2009 write-up. Her presence in 2006 is proven; the 2006
   task content is not.
8. The live **task id** and any time limit (none reported, and none appears in the in-game text).
9. Lucy (lucy.allakhazam.com) returned no page content, and Fanra's wiki, The Druid's Grove archive and EQ Resource
   achievements returned 403. The 2017 YouTube walkthrough (Lenexa1776, f1O9LajExu8, 8:36) was not transcribed.

---

## Sources

- https://everquest.allakhazam.com/db/quest.html?quest=4904 (Haunted Cave; comments Nov 07 2009 x2, Oct 22 2012
  dylothe, Oct 31 2016)
- https://everquest.allakhazam.com/db/npc.html?id=26733 (Jilian Florantine; comments Nov 05 2009, Oct 25 2018; added
  2007-11-07 22:17:52)
- https://everquest.allakhazam.com/db/npc.html?id=26731 (Shadow of All Hallows Eve)
- https://everquest.allakhazam.com/db/npc.html?id=26732 (Ghost of All Hallows Eve; added 2007-11-07 22:17:07)
- https://everquest.allakhazam.com/db/item.html?item=61077 (Pirate's Gold, Alla id)
- https://everquest.allakhazam.com/db/quest.html?quest=4623 and https://everquest.allakhazam.com/db/npc.html?id=30501
  (Aragol; NPC added 2008-08-29)
- https://everquest.allakhazam.com/wiki/EQ:Halloween (lists Haunted Cave under 2006)
- https://www.bonzz.com/nightsofthedead.htm (Haunted Cave under 2009 #6; Aragol under 2006 #8)
- https://legacy.fanbyte.com/story.html?story=8196 (ZAM copy of the Oct 30 2006 patch notes plus Oct 31 2006
  comments)
- https://github.com/nazwadi/patcheq `patches-2006-2.txt` 507-518 and 35; `patches-2007-2.txt` 399;
  `patches-2008-2.txt` 630-639
- https://www.youtube.com/watch?v=f1O9LajExu8 (Lenexa1776, 2017-11-02; metadata only)
- Screenshots: zam.zamimg.com/images/c/8/c80a3ea1ffe9e6f3fef28047e2dd3368.jpg,
  /2/a/2ad69b066c9d250f54d11d6e79c955c4.jpg, /0/d/0da8152184c628a82b29135bddee5642.jpg,
  /8/a/8ab52ac4ec946e86637a0ccea8c813a8.jpg
- PEQ dump `scratchpad\notd_web\peq-dump\create_tables_content.sql` (items 87298/87299/87307/87308/87313/87314;
  task 5656 + activities; spawn2 crescent; spells 3090; lootdrops 90606/90607)
- PEQ quests `scratchpad\notd_web\peqquests\crescent\#Aragol_Gloomflow.pl`
- Map labels: `scratchpad\notd_web\gmaps\Good's Maps\crescent_2.txt`,
  `scratchpad\notd_web\bmaps\Brewall's Maps\crescent_1.txt`
- Local DB (SELECT only): npc_types, tasks, items, spawn2/spawnentry, doors (OBJ_PADDLE 14124), spells_new 3090,
  loottable_entries/lootdrop_entries
