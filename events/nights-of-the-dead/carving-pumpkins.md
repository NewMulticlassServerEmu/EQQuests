# Carving Pumpkins (EverQuest LIVE, Nights of the Dead, added Sept 2021) - research

Research date: 2026-10-05. Web-only. Every fact carries its source. **UNKNOWN** = not found in any source; **INFERRED** = my reasoning, not stated by a source.

## Sources

- [EQR-Q] EQ Resource quest page: https://special.eqresource.com/carvingpumpkins.php (author Riou, Sept 28 2021). WebFetch gets a 403; curl with a browser UA works.
- [ZAM-Q] Allakhazam quest page: https://everquest.allakhazam.com/db/quest.html?quest=10522 (entered Oct 27 2021, modified Oct 23 2022). Allakhazam/CloudFront blocks curl, so I read the full text from the Wayback snapshot http://web.archive.org/web/20230324062524id_/https://everquest.allakhazam.com/db/quest.html?quest=10522 . The current live page, read via WebFetch, matches it but now says Max Level 125.
- [ZAM-NPC-H] https://everquest.allakhazam.com/db/npc.html?id=57248 (Hule C. Zarshcl)
- [ZAM-NPC-S] https://everquest.allakhazam.com/db/npc.html?id=57250 (a wandering scarecrow)
- [ZAM-R] https://everquest.allakhazam.com/db/recipe.html?recipe=60636 (Perfectly Carved Pumpkin recipe)
- ZAM item pages (ZAM ids are NOT game ids): Kit 142987, Knife 142988, Perfectly Carved Pumpkin 142989, Carving Pumpkin 142990, Bale of Hay 3091, Ominous Orangeade 140861, Ghastly Gummy Bears 140854
- [EQR-I] EQ Resource item pages, https://items.eqresource.com/items.php?id=N . These use the real LIVE item ids; the "Advanced Loot" string is id^icon^name.
- [EQR-A] Achievement: https://achievements.eqresource.com/achievements.php?id=200130
- [EQR-SQ] Follow-up quest (context for the knife, kit and scarecrow clothes): https://special.eqresource.com/squashingpumpkins.php
- Coordinate order: https://www.redguides.com/docs/projects/everquest/commands/cmd-waypoint/ gives `/waypoint <y>, <x>, [<z>]` and says "EverQuest always displays the Y coordinate first".

---

## 0. Header / meta

| Field | Value | Source |
|---|---|---|
| Quest name | Carving Pumpkins | EQR-Q, ZAM-Q |
| Zone | The Western Plains of Karana (westkarana) | both |
| Giver | Hule C. Zarshcl, title "(Nights of the Dead Quests)" | ZAM-Q, screenshot |
| Request phrase (task assigned on) | `few tasks` | EQR-Q |
| Time limit | Unlimited | EQR-Q |
| Task type | Solo | EQR-Q; ZAM-Q "Group Size: Solo" |
| Repeatable | Yes | EQR-Q, ZAM-Q |
| Repeat timer / lockout | **UNKNOWN**. No source mentions one. | - |
| Level | 20 (recommended/min) | ZAM-Q |
| Max level | 120 (2023 snapshot); 125 (current live page) | ZAM-Q |
| Seasonal | "This Quest is Seasonal", Nights of the Dead only | ZAM-Q |
| Era tag | Claws of Veeshan | ZAM-Q |
| Shroudable / Monster Mission | No / No | ZAM-Q |
| Achievement | Nights of the Dead: Magnificent Winter Squash (see section 7) | EQR-Q, EQR-A |
| Follow-up quest | Squashing Pumpkins (Levy Cullpay, West Karana). Hule's last line points to it. | ZAM-Q, EQR-SQ |

---

## 1. Full dialogue, verbatim from ZAM-Q

Typos kept as written ("get red of", "didn't plan any"). On live, clicking a [bracket] makes the player say a long reply sentence; that sentence is shown on the "You say" lines. For EQEmu, the trigger is the bracketed keyword.

```
You say, 'Hail, Hule C. Zarshcl'
Hule C. Zarshcl says, 'Would you just look at this place? It's really gone to seed. I am ashamed to have spilled so much blood and sweat [ over this land ].'
You say, 'I have looked over this land, and I think it looks great. What's wrong with it?'
Hule C. Zarshcl says, 'What's wrong with it? Are you blind? This farm was once fertile and productive, an achievement like no other. We supplied most of the food for Qeynos. Now look at it, overrun with scarecrows and wild grasses. How are my dullards of [ descendants ] supposed to manage?'
You say, 'Can I help your descendants?'
Hule C. Zarshcl says, 'Bah. There's not much to help, unfortunately. They're both [ so busy ], pretending that they can't see me.'
You say, 'If they are so busy, what are they doing?'
Hule C. Zarshcl says, 'They are getting ready for the Nights of the Dead, but do you see any pumpkins around here? They didn't even [ plant any ].'
You say, 'They didn't plan any because they purchased some from Arlien Browch.'
Hule C. Zarshcl says, 'Did they purchase crops? Are they merchants now? Just [ send ] me back, I can't hear anymore of this.'
You say, 'How can I help send you back?'
Hule C. Zarshcl says, 'Oh, you'd like that, wouldn't you? Hrmph. Fine then. I have a [ few tasks ] that need to be done before discussing the Nights of the Dead celebration.'
You say, 'What few tasks?'
Hule C. Zarshcl says, 'First, get red of some of the scarecrows, and then help clean up the cropland. When you are done let me know and we can discuss what's next.'
 You have been assigned the task 'Carving Pumpkins'.
```

Keyword chain: `over this land` -> `descendants` -> `so busy` -> `plant any` -> `send` -> `few tasks` (assigns the task).

Task description (journal text): "Hule C. Zarshcl is frustrated with how his descendants have been taking care of the farm. He wants you to help them out before he will tell you what he wants to be done for the Nights of the Dead." (ZAM-Q)

When the wild grass is turned in:
```
Hule C. Zarshcl says, 'Well, that's not too shabby.'
Your task 'Carving Pumpkins' has been updated.
```

Step "[delivered pumpkins]":
```
You say, 'Delivered pumpkins.'
Hule C. Zarshcl says, 'Ha. In my time we would grow our own pumpkins. We'd use the pieces for food and the shell for fun and [ scary faces ].'
You say, 'I am good at carving scary faces.'
Hule C. Zarshcl says, 'Eh? You think you can carve a perfect pumpkin? Well, I just [ doubt that ].'
You say, 'Oh. I don't doubt that. Give me a chance? You won't regret it.'
Hule C. Zarshcl says, 'Well, alrighty then. Here, take this carving kit and knife. Show me what you've got.'
-> You are given a Pumpkin Carving Knife and a 4-slot container, Pumpkin Carving Kit.
```
Keyword chain: `delivered pumpkins` (updates the step) -> `scary faces` -> `doubt that` (gives the knife and kit).

EQR-SQ adds: with the task active, saying 'delivered pumpkins' to Hule again and going through the text gives a new knife and/or kit. This is how players re-get them for the follow-up quest.

When the 10 carved pumpkins are turned in:
```
Your task 'Carving Pumpkins' has been updated.
Hule C. Zarshcl says, 'Well now. That is not so bad. You did a good job on these [ ].'
```
The brackets are empty in ZAM's capture. EQR-Q says "Say ' carved pumpkins ' to complete the quest", and the step text is "Talk with Hule about the [carved pumpkins]". The keyword is therefore **carved pumpkins**. The exact wording inside the brackets on live is **UNKNOWN**; it is probably "[ carved pumpkins ]".

Final step:
```
You say, ' I did take my time to make sure that they were perfectly carved pumpkins.'
Your task 'Carving Pumpkins' has been updated.
 (completion text) You helped Hule C. Zarshcl clean up the farm, and in turn, he had you do more work. It's a good thing that you wanted to help him out.
Hule C. Zarshcl says, 'Ha. Such a good kid. Maybe you will get to [ see the ] Magnificent Winter Squash.
You say, 'See the what?'
Hule C. Zarshcl says, 'Yes. Head out into the fields, Levy Scarecrow should help you out with that.'
```
The text says "Levy Scarecrow". The follow-up NPC is "Levy Cullpay" (EQR-SQ), so this may be a live typo or a nickname. It is quoted as captured.

**UNKNOWN (no source has them):** what Hule says to keywords when the task is not active or the step is wrong; replies to wrong or partial turn-ins (for example fewer than 10 grasses or pumpkins); any idle or proximity text.

---

## 2. NPCs, locations, appearance

**Coordinate format:** every coordinate here is `/waypoint` / `/loc` order, **(Y, X, Z)**. Redguides: `/waypoint <y>, <x>, [<z>]`, and EQ always shows Y first. For EQEmu spawn2: `x` = 2nd number, `y` = 1st number. INFERRED check: West Karana is wide east-west, so the larger-range number (around -7600) is the E-W axis (X). Both maps show Hule at the south edge, near the middle.

### Hule C. Zarshcl
- Location: `/waypoint -3721.55, -7646.95, 2.63` (Y, X, Z), "standing next to a barn near the water", southern part of West Karana, "slightly closer to Qeynos Hills than North Karana" (ZAM-Q comment by Wreck, Oct 31 2022). In EQEmu terms: x=-7646.95, y=-3721.55, z=2.63. Heading **UNKNOWN**.
- Map: EQR map with a black square marker at the south edge, middle of the zone: https://special.eqresource.com/expacimages/carvingpumpkins.jpg . ZAM map with a red dot in the same place: https://zam.zamimg.com/images/0/7/07bfedc642419ef7e415c76797496ebf.jpg
- Level 50 (ZAM-NPC-H).
- Appearance (from the screenshot https://zam.zamimg.com/images/4/1/4110e5ec937005799e909efbe2edffac.jpg): an old **human male**, grey hair and beard, sleeveless dark-teal shirt, teal pants, bare-looking feet, holding a **wooden bucket** in his right hand. The whole model is **translucent / ghostly**: he is a dead ancestor ("pretending that they can't see me", "send me back"). He stands by a barn. The race and gender are INFERRED from the picture; the race id, texture, translucency setting and held item id are **UNKNOWN**.
- Title / lastname "(Nights of the Dead Quests)" (screenshot).
- Class, faction, body type, and whether he can be attacked: **UNKNOWN**.
- Nearby NPC mentioned: "Tukk", on the other side of the barn from Hule (ZAM-Q comment). Who Tukk is: **UNKNOWN**.

### a wandering scarecrow
- Exact name `a wandering scarecrow` (ZAM-Q, ZAM-NPC-S). Level **25** (ZAM-NPC-S).
- Spawn point: `/waypoint -3734, -7073` (Y, X): one spawn point listed (ZAM-Q, ZAM-NPC-S). That is about 570 units east/west of Hule along the same southern line (INFERRED from the numbers).
- Behaviour (ZAM-Q text and comments):
  - "One paths to the area of Hule every few minutes or you can use a tracker to find more faster."
  - "Once you kill a scarecrow they immediately respawn and agro. 10 kills in as many seconds." "They seem to wander NW." (Chardlb, Oct 12 2022)
  - "Tracking will not be good for you if you use it to hunt for the Wandering Scarecrows. They wander far and wide. Best to get them close to Hule near their spawn point" (Wreck)
  - EQR-Q: "Defeat scarecrows, found throughout the zone".
  - So: one spawn point, near-instant respawn, the mob is aggressive and roams around the zone (wanders NW).
- Appearance (screenshot https://zam.zamimg.com/images/2/9/2989853dca3d4b3089e137b3d7282952.jpg): modern scarecrow model with a **carved jack-o'-lantern pumpkin head**, brown patched coat with straw cuffs and hem, blue patched trousers, brown boots. Race id, texture and gender: **UNKNOWN**. The RoF2 client's scarecrow race models need checking.
- Drops: **Carving Pumpkin** (ZAM-NPC-S "Known Loot"). Drop rate: **UNKNOWN**; no percentage published. ZAM-Q says pumpkins are "pre-lootable and tradeable". A comment (Dogpaw) says "Get an extra pumpkin to carve for the next quest", so pumpkins drop often enough that people farm extras.
- **Tattered Scarecrow Clothes** (live id 113465): EQR-SQ says it is "dropped from the Scarecrows". It is used in the **Squashing Pumpkins** costume combine, **not** in Carving Pumpkins. Which scarecrows drop it (the wandering ones or others) and the rate: **UNKNOWN**.
- How many are up at once: **UNKNOWN** beyond "one spawn point" with an instant respawn.
- HP, class, special abilities: **UNKNOWN**.
- Kill credit is shared: "This portion will update an entire group if you are grouped." (ZAM-Q)

---

## 3. Task steps (EQR-Q's 7 steps; ZAM-Q merges steps 2 and 3)

| # | Step text (live) | Count | Update type | Details |
|---|---|---|---|---|
| 1 | Kill the wandering scarecrows (The Western Plains of Karana) | 0/10 | KILL `a wandering scarecrow`; group-wide credit (ZAM-Q) | Description: "Weed out some of the wandering scarecrows." |
| 2 | Weed the wild grasses (The Western Plains of Karana) | 0/10 | LOOT / ground-spawn pickup of `Wild Grass` (ZAM-Q "Loot 10 'Wild Grass'"; EQR "ground spawn") | Description: "Weed the wild grasses from the croplands." |
| 3 | Deliver the wild grasses to Hule (The Western Plains of Karana) | 0/1 | DELIVER (hand in) Wild Grass to Hule | Reply "Well, that's not too shabby." How many must be handed over is **UNKNOWN**, presumably the 10 (INFERRED from step 2 = 10, step 3 = 0/1). |
| 4 | Talk with Hule about the [delivered pumpkins] | 0/1 | SPEAK `delivered pumpkins` | Then `scary faces` -> `doubt that` gives the Knife and Kit. |
| 5 | Carve pumpkins for Hule | 0/10 | Updates on a COMBINE (each Perfectly Carved Pumpkin made) | Description: "Find some pumpkins from the Wandering Scarecrows and carve them for Hule." On live, task updates from a tradeskill combine are triggered by the combine result. Whether the update comes from the combine event or from looting the result: **UNKNOWN** (INFERRED: combine). |
| 6 | Deliver the perfectly carved pumpkins to Hule | 0/10 | DELIVER 10 x Perfectly Carved Pumpkin | Description: "Return the Perfectly Carved Pumpkins to Hule." |
| 7 | Talk with Hule about the [carved pumpkins] | 0/1 | SPEAK `carved pumpkins` -> task complete, reward | Description: "Talk with Hule about the carved pumpkins." |

Item requirements in total: 10 scarecrow kills, 10 Wild Grass, 10 Carving Pumpkins (loot from scarecrows), 10 combines.

---

## 4. Ground spawn: Wild Grass

- Item: **Wild Grass**, live id **113460** (EQR-I). Picked up by clicking "grassy looking patches" (ZAM-Q).
- Model: a small clump of green leaves on the ground. Picture: https://special.eqresource.com/expacimages/carvingpumpkins1.jpg . Model or actor name: **UNKNOWN**.
- Respawn: **60 seconds** (ZAM-Q: "The grass respawn is 60 seconds.")
- Locations, `/waypoint` order (Y, X, Z), all from ZAM-Q comments:
  - -3635.30, -7687.74, 3.87 (barn close to Hule)
  - -3769.57, -7681.92, 2.05 (next to Tukk, on the other side of the barn from Hule)
  - -3746.24, -7060.06, 2.29 (tree a bit west of Hule; this is right at the scarecrow spawn point)
  - -3787.34, -7288.79, 1.76 (tree a bit west of Hule)
  - -3367.67, -7217.16, "2329" (tree a bit NW of Hule; the Z is a typo, probably 23.29)
  - -3280.68, -7494.86, 32.97 (tree a bit north of Hule)
  - -3372, -7217 and -3315, -7090 (NW of Hule, "about halfway to the house out that way"; ArtulynStarsummoner, Nov 3 2021; the first is the same spot as -3367/-7217)
- Other notes: "There are 2 grassy looking patches near the NPC" (ZAM-Q body). "at least 4 or more wild grasses in the immediate area of quest giver up at the same time. Look at the base of the trees." (Dogpaw). "Grass patch at the spawn point, two beside Tukk's barn and one at tree between barn and spawn." (Chardlb). EQR-Q: "around Hule, with some a little west and north of him".
- Max number up at once: **UNKNOWN** (at least 4 by the comments, with about 7 distinct spots).

---

## 5. Items

Live ids are from EQR "Advanced Loot" (id^icon^name). ZAM ids are listed only for cross-reference.

### Pumpkin Carving Kit: live 113458, icon 730 (ZAM 142987)
- Flags: **Magic, Lore, Quest** (EQR-I). ZAM: "Lore Item, Quest Item". **Not No Trade** (no source lists No Trade).
- Container: **Capacity 4**, **Size Capacity GIANT**, **Weight Reduction 1%**, weight 0.1, size SMALL, stack 1. "This item can be used in tradeskills." (EQR-I, ZAM)
- Lore text (ZAM): "This is the Zarshcl family Pumpkin Carving Kit. Hule has been gracious enough to let a nonfamily member use it to carve pumpkins for Nights of the Dead."
- Container combine type number: **UNKNOWN** (it is a quest-specific tradeskill container; neither site shows a bag type).
- Temporary: not indicated by any source.
- Given by Hule at step 4 (after `doubt that`).

### Pumpkin Carving Knife: live 113459, icon 1299 (ZAM 142988)
- Flags: **Lore, Quest** (EQR-I; ZAM "Lore Item Quest Item"). Not Magic, not No Trade. WT 0.0, Size SMALL, stack 1. "This item can be used in tradeskills."
- Item info: "This knife has the initials H.C.Z. lovingly carved into its worn pumpkin-colored handle."

### Wild Grass: live 113460, icon 6132
- Flags: **Quest**. Size SMALL. **Stack 50**. No lore text. Not sellable. (EQR-I)

### Carving Pumpkin: live 113464, icon 1696 (ZAM 142990)
- Flags: **Quest**. Size SMALL, WT 0.0, **stack 10**. Text: "This is a perfect pumpkin to carve into a Jack O'Lantern." Tradeable and pre-lootable (ZAM-Q). Drops from `a wandering scarecrow`.

### Perfectly Carved Pumpkin: live 113461, icon 1481 (ZAM 142989)
- Flags: **Quest**. Size SMALL, WT 0.0, **stack 10**. Text: "You have perfectly carved this pumpkin into a classic Jack O'Lantern. Hule C Zarshcl will be proud of this carved gourd." Also used in Squashing Pumpkins. Icon screenshot: https://zam.zamimg.com/images/3/9/39315eb7af8af8be327a930a46896fbb.png

### Recipe: Perfectly Carved Pumpkin (ZAM-R recipe 60636)
- Tradeskill: **Non-Tradeskill**. Container: **Pumpkin Carving Kit**. Class ALL.
- Components: 1 x Carving Pumpkin + 1 x Pumpkin Carving Knife -> **1 x Perfectly Carved Pumpkin**.
- Trivial: none listed (non-tradeskill). No-fail: not stated (**UNKNOWN**).
- **Is the knife consumed? No (INFERRED, strongly supported).** ZAM-R does not show a "returned" flag, but:
  - Hule gives the knife once; it is Lore, and the step needs 10 combines.
  - ZAM-Q comment: "don't throw away the Pumpkin Carving Knife and Pumpkin Carving Kit. You'll need them for the next quest."
  - EQR-SQ says the follow-up costume combine (Perfectly Carved Pumpkin + Tattered Scarecrow Clothes + Bale of Hay) "will use the Knife up in the combine". It calls that out only for the costume combine, so the carving combine returns the knife.
  - For EQEmu: give the knife a recipe entry with componentcount 1 and successcount 1 (returned).

### Context items from the follow-up quest (not part of Carving Pumpkins)
- Bale of Hay (ZAM 3091; listed under ZAM-Q "Quest Items"): a ground spawn for Squashing Pumpkins (EQR-SQ).
- Tattered Scarecrow Clothes, live 113465: Lore, Quest, SMALL, stack 1.
- Winter Squash Scarecrow Costume, live 113466: Magic, Lore, Quest; clicky "Winter Squash Scarecrow Costume", Any Slot, Instant, Expendable 5 charges.

---

## 6. Rewards

The sources disagree, probably because live changed the rewards between years.

- **EQR-Q (written Sept 28 2021 = the 2021 event): "5x Ominous Orangeade".** This matches the 2021 brief.
- ZAM-Q "Reward(s)" (submitted by Cylius & Laurana; page modified Oct 2022):
  - Dreadful Drinks: (5) Ominous Orangeade
  - Dreadful Drinks: (5) Bone-Chilling Brew ("AC: 10, HP: 250, Mana: 300, End: 200, Corrupt: 2. This is an enduring drink!")
  - Dreadful Foods: (5) Ghastly Gummy Bears
  - Comments: Diepen (Oct 12 2022) "5x Bone-Chilling Brew" with screenshot https://i.postimg.cc/3rDb8Lvx/BCB.png ; Wreck (Oct 31 2022) "I got the Orangeade".
  - The "Dreadful Drinks/Foods" headings suggest the reward is chosen by level or at random from a group. **Which mechanism: UNKNOWN.** Bone-Chilling Brew (rec level 90) first appears on EQR in Nov 2022, so it is probably a 2022 addition, likely for characters below level 100 (INFERRED).
- Experience reward from the quest itself: **UNKNOWN** (no source mentions XP for the task). The achievement gives AA and experience (section 7).
- Currency or faction: none mentioned (**UNKNOWN**).

### Ominous Orangeade: live 94097, icon 3064 (ZAM 140861)
- Item type **Drink**: "This is a miraculous drink! (90)", meaning drink duration value 90 ("Miraculous Drink(90)" on ZAM).
- Stats: **AC 155, HP +1200, Mana +1200, Endurance +400**.
- **Required level 100.** Weight 0.5, Size SMALL, Class ALL, Race ALL.
- **Stack 20.** Tribute 240. Merchant value 1 cp. No Lore, No Trade or Magic flags shown, so it is tradeable.
- Click effect / spell: **none**. Neither EQR nor ZAM lists an Effect line.
- The 2022 ZAM snapshot (IC updated 2022-01-17) and the current EQR (updated Sep 24 2024) show the same stats.
- Screenshot: https://zam.zamimg.com/images/e/2/e2cdd81d45ce1d6b0aa07a23631d7146.jpg
- Also a reward of: Squashing Pumpkins, The Witch's Wishes (South Karana).
- How live applies stats on food and drink (while carried, on consume, or other): not stated in these sources (**UNKNOWN**). EQEmu/RoF2 note (INFERRED): stats on a non-equippable drink do nothing in stock EQEmu.

### Ghastly Gummy Bears: live 94095, icon 1690 (ZAM 140854)
- Food: "This is a miraculous meal! (90)". AC 155, HP 1200, Mana 950, End 600. Required level 100. WT 0.5, SMALL, stack 20, tribute 600. No effect.

### Bone-Chilling Brew: live 94096, icon 3063
- Drink: "This is an enduring drink! (60)". AC 10, HP 250, Mana 300, End 200, Corruption 2. **Recommended** (not required) level 90. WT 0.5, SMALL, stack 20, tribute 10. No effect.

---

## 7. Achievement

- **Nights of the Dead: Magnificent Winter Squash** (EQR achievement id 200130). Category Events > Holiday. **10 points.** Rewards: "AA (Scales to Level)" and "Experience". Not a world achievement.
- Objectives (all three needed):
  1. Arlien Browch in The Commonlands - Missing Pumpkins
  2. Hule C. Zarshcl in The Western Plains of Karana - Carving Pumpkins
  3. Levy Cullpay in The Western Plains of Karana - Squashing Pumpkins
- No separate achievement for Carving Pumpkins alone was found.

---

## 8. Repeatable / lockout / level / group

- Repeatable: Yes (EQR, ZAM). Lockout or repeat timer: **UNKNOWN**; none is mentioned anywhere.
- Time limit: Unlimited (EQR).
- Level 20 to 120 (2023) or 125 (now) (ZAM).
- Solo task (EQR "Task Type: Solo", ZAM "Group Size: Solo"), but scarecrow kills credit the whole group (ZAM-Q).
- Lore context: Hule's descendants bought pumpkins from Arlien Browch, which links to Missing Pumpkins (Commonlands). The follow-up is Squashing Pumpkins with Levy Cullpay.

---

## Not found (explicit unknowns)

1. The text inside Hule's empty "[ ]" bracket after the pumpkin turn-in. The keyword is "carved pumpkins" per EQR and the step text.
2. Hule's replies to wrong, partial or out-of-order hand-ins and keywords, and any text when no task is active.
3. Hule: race id, texture, translucency setting, held-item (bucket) id, heading, class, faction, body type, attackable or not. Seen in the picture as a ghostly old human male with a bucket.
4. Scarecrow: race id, texture, HP, class, special abilities, how many are up at once; drop rates for Carving Pumpkin and Tattered Scarecrow Clothes.
5. Wild Grass ground-spawn model or actor name and max number up at once (respawn 60 s is known).
6. The Pumpkin Carving Kit bag-type / combine-type number; whether the carve combine can fail. The knife being returned is inferred, not stated.
7. Whether the 'Carve' step updates on the combine or on looting the result (inferred: combine).
8. How many Wild Grass the turn-in step takes (inferred: 10).
9. Experience from the quest itself; the reward-selection rule behind ZAM's three-item reward list (2022+). The 2021 reward was 5x Ominous Orangeade.
10. Repeat lockout timer.
11. Who "Tukk" is (an NPC next to Hule's barn).
