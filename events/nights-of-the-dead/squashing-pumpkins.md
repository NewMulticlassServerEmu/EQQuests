# Squashing Pumpkins (EQ Live, Nights of the Dead, added 2021) - research

Researched 2026-10-05. Read-only web research. UNKNOWN = not found in any source; never guessed.

## Sources
- EQ Resource quest page (raw HTML fetched, verbatim): https://special.eqresource.com/squashingpumpkins.php
  - step map: https://special.eqresource.com/expacimages/squashingpumpkins.jpg (local copy: sq_map.jpg)
  - Bale of Hay ground spawn picture: https://special.eqresource.com/expacimages/squashingpumpkins1.jpg (local: sq_hay.jpg)
- ZAM quest page: https://everquest.allakhazam.com/db/quest.html?quest=10523
  (ZAM blocks curl (CloudFront 403); read through WebFetch, which returns quotes, not a raw dump.
  The dialogue lines below are the quotes it returned. Treat the ZAM wording as near-verbatim, not byte-exact.)
- ZAM NPCs: Levy Cullpay https://everquest.allakhazam.com/db/npc.html?id=57251 ; Winter Squash https://everquest.allakhazam.com/db/npc.html?id=57252 ; a wandering scarecrow https://everquest.allakhazam.com/db/npc.html?id=57250
- ZAM Carving Pumpkins (prior quest, Hule's hand-off line): https://everquest.allakhazam.com/db/quest.html?quest=10522 (local zam_q10522.txt)
- EQR items (raw, verbatim): items.eqresource.com/items.php?id= 13990, 113458, 113459, 113461, 113464, 113465, 113466, 94095, 94097
- EQR spell 26895 + raw data: https://spells.eqresource.com/spells.php?id=26895 , https://spells.eqresource.com/rawspells.php?id=26895
- EQR achievement: https://achievements.eqresource.com/achievements.php?id=200130

NOTE: ZAM item and NPC ids (140864, 142989, 142991, 57251...) are ZAM-internal ids, NOT game ids. Use the EQR ids (the real live item ids) below.

## Quest metadata (EQR, verbatim)
- Zone: The Western Plains of Karana (qey2hh1). Quest Giver: Levy Cullpay. Request Phrase: `magnificent winter squash`
- Time Limit: Unlimited | Task Type: Solo | Repeatable: Yes
- Rewards: 5x Ghastly Gummy Bears (94095), 5x Ominous Orangeade (94097)
- Achievement: Nights of the Dead: Magnificent Winter Squash (EQR id 200130)
- ZAM: Level range 0-125; repeatable; "only available seasonally"; expansion tag Claws of Veeshan (released for NotD 2021).
- ZAM also lists "5 Eerie Jelly Beans on the Mischief server" (Mischief-only variant).
- Whether the 5 food + 5 drink are BOTH given or a CHOICE: UNKNOWN. EQR lists both as rewards. ZAM's prior quest (Carving Pumpkins) shows a selectable "Dreadful Drinks / Dreadful Foods" reward set, so a choice is plausible, but no Squashing source says so.
- Experience: UNKNOWN for the task itself. The achievement's reward line on EQR reads "AA (Scales to Level)" / "Experience" (that is the achievement reward, not the task).
- Lockout: none stated (EQR Time Limit Unlimited, Repeatable Yes). No source mentions a repeat timer. UNKNOWN beyond that.

## Prerequisite / chain
- The achievement needs 3 tasks: Missing Pumpkins (Arlien Browch, Commonlands) -> Carving Pumpkins (Hule C. Zarshcl, W Karana) -> Squashing Pumpkins (Levy Cullpay). Achievement: 10 points.
- Carving Pumpkins ends with Hule pointing to Levy (ZAM q10522, quoted):
  - Hule C. Zarshcl says, 'Ha. Such a good kid. Maybe you will get to [ see the ] Magnificent Winter Squash.
  - You say, 'See the what?'
  - Hule C. Zarshcl says, 'Yes. Head out into the fields, Levy Scarecrow should help you out with that.'
- Hard gate (must have finished Carving Pumpkins before Levy gives the task): UNKNOWN. No source says it is gated. In practice the Pumpkin Carving Kit + Knife only come from Hule's Carving Pumpkins task:
  - EQR: "If you completed the Carving Pumpkins Quest you should already have a Carving Knife and Kit container, you can get more if needed by having the Quest Active and Saying 'delivered pumpkins' to Hule C. Zarshcl, and go through text, to get a new Knife and/or Carving Kit"
  - ZAM comment aparker (Oct 13 2025): "...You can go back to Hule and get the quest again and then just say ' Doubt that' and he will give you another one."
  - ZAM q10522 comment Dogpaw (Nov 5 2021): "Get an extra pumpkin to carve for the next quest - you will use it to make the costume"

## 1. NPC dialogue - Levy Cullpay (ZAM walkthrough, in order)
Live saylinks: the player's spoken line differs from the bracketed word. "You say" lines are as ZAM shows them.

```
You say, 'Hail, Levy Cullpay'
Levy Cullpay says, 'Ha. Ha. Ha. Isn't it just [wonderful]? I just love this time of the year.'
You say, 'It is wonderful, but how do you mean?
Levy Cullpay says, 'Ha. Ha. Ha. [Harvest] season is almost done. There is less of a reason to guard the fields and more to wander around.'
You say, 'Aw, you like the harvest?'
Levy Cullpay says, 'Ha. Ha. Ha. Of course I do. It's fun to see all [the farmers] run around hooting and hollering. Trying to get the last of it before the season changes.'
You say, 'You watch the farmers while they work?'
Levy Cullpay says, 'Ha. Ha. Ha. What else have I got to do? With all the noise they make they scare away any varmints before I can. I'm just sitting here, waiting to [wake up].'
You say, 'What do you mean wake up?'
Levy Cullpay says, 'Ha. Ha. Ha. I sit here year-round watching the fields and scaring away pests, but after the harvest I get to [run around].'
You say, 'You get to run around?'
Levy Cullpay says, 'Ha. Ha. Ha. Yes. Once the harvest is done, the [Magnificent Winter squash] flies by, granting all the good scarecrows the chance to wander until the season changes.'
You say, 'The Magnificent Winter Squash?'
You have been assigned the task, 'Squashing Pumpkins'.
Levy Cullpay says, 'Ha. Ha. Ha. He is a great being, powerful, big, and round. He only shows himself to those who really [believe in him].'
You say, 'I believe in him. How can I meet him?'
Levy Cullpay says, 'Ha. Ha. Ha. I don't know. I have never met him, but I know he exists. Maybe if he thought you were [a scarecrow]?'
You say, 'And how would I get him to think I was a scarecrow?'
Levy Cullpay says, 'Ha. Ha. Ha. You could [dress up] like one and then visit places that he has been seen.'
You say, 'How would I dress up like one?'
Levy Cullpay says, 'Ha. Ha. Ha. You can gather a bale of hay, tattered clothes, and a perfectly carved pumpkin. You can then craft them into a costume that you can wear near these places that I have noted down.'
   -> completes step 1 "Speak with Levy about dressing up"
... (steps 2-12) ...
You say, 'I'm not finding anything.'
Levy Cullpay says, 'Ha. Ha. Ha. The Magnificent Winter Squash must have seen through your disguise. He's out there, I know it. I may not meet him this year, but I will meet him.'
```
Completion text (task completion message):
"You heard about the legend of the Magnificent Winter Squash and decided to check it out for yourself. After spending some time running around and trying to find the Magnificent Winter Squash, all you found was someone else trying to track him down. Better luck next year."

Notes / gaps:
- One WebFetch pass rendered the [run around] line as "...granting all the good scarecrows the chance to [run around] until the season changes" and the next pass as "...chance to wander until the season changes." The ordered transcript above (with "wander") is the one ZAM gave in sequence; exact word UNKNOWN (one of the two).
- EQR's request phrase is `magnificent winter squash`: the task is assigned when the player says the Magnificent Winter Squash line, BEFORE Levy's "great being" reply.
- The task step names `dressing up` (step 1) and `not finding` (step 13) are the in-game step texts. The bracket Levy shows is [dress up]; the player line is "How would I dress up like one?".
- Exact player line for the bracket [wonderful] etc. are what ZAM shows; the trailing quote missing on "It is wonderful, but how do you mean?" is ZAM's typo.
- What Levy says if hailed while the task is active, or after completion: UNKNOWN.
- No dialogue for Winter Squash besides the death line. No spawn or aggro shout recorded: UNKNOWN.

## 2. NPCs - location / look / level
Coordinates: ZAM gives them as `/waypoint A, B[, C]`. Checked against the EQR step map (pixel positions of markers 1-5 and Levy): the first number is north/south and the second is east/west, i.e. the SAME ORDER AS /loc (Y, X, Z). For EQEmu spawn2: x = 2nd value, y = 1st value, z = 3rd.

| NPC | /loc (Y, X, Z) | Look | Level | Screenshot |
|---|---|---|---|---|
| Levy Cullpay (Nights of the Dead Quests) | -3146.53, -4422.88, 39.42 (ZAM comment Wreck, Nov 1 2022: "a Scarecrow standing in the middle of a plowed field (Miller's Farm?)... WAY closer to Qeynos Hills than North Karana") | Pumpkin-headed scarecrow (jack-o-lantern head, straw hands, brown shirt, blue patched trousers, boots). It looks like the classic Karana Scarecrow model, but the race id is UNKNOWN (not stated). Gender UNKNOWN. Surname shown: "(Nights of the Dead Quests)". | 45 (ZAM) | https://zam.zamimg.com/images/7/c/7ca20d48f0b9c9c4e0888976378e4af0.jpg ; map pin: https://zam.zamimg.com/images/c/7/c7d2357f268cc5e807abfc17a85c8ee1.jpg |
| Winter Squash (task spawn) | spawned by clicking the Winter Squash Trap at 1300, -13225 (NE corner, by the North Karana zone line) | Cyclops (ZAM + Wreck "Winter Squash, is a Cyclops"). Screenshot: old-model one-eyed cyclops with a yellow/green "squash" coloured body. Race id / texture UNKNOWN. | 31-32 (ZAM) | https://zam.zamimg.com/images/7/d/7d07250d201a3d73440a016e5648a228.jpg ; map pin: https://zam.zamimg.com/images/f/8/f83c90a9b94441743a35939fab7b3db3.jpg |
| a wandering scarecrow (drops Carving Pumpkin, and per EQR the Tattered Scarecrow Clothes) | spawn point -3734, -7073 (ZAM q10522 comments); they wander far, pathing near Hule | Scarecrow | 25 (ZAM) | https://zam.zamimg.com/images/2/9/2989853dca3d4b3089e137b3d7282952.jpg |
| Hule C. Zarshcl (previous quest, replacement kit/knife) | -3721.55, -7646.95, 2.63 (ZAM q10522 comment Wreck) next to a barn near the water | - | - | - |

- Winter Squash HP, damage, special abilities, class: UNKNOWN (no source lists them).
- Death line: "Winter Squash's corpse says, 'Oh. I squashed.'" Loot: none recorded (UNKNOWN).
- Wreck (Nov 1 2022): "This was the last quest in the achievement set. 'Winter Squash', is a Cyclops. When you get done killing him, succor or levant. It takes you much closer to Levy. Beats running across this stupid zone."
- Live NPC ids: UNKNOWN (ZAM ids are internal).

## 3. Task steps (EQR step list, verbatim in-game names, 13 steps)
1. Speak with Levy about dressing up 0/1 - "Continue through Levys text"
2. Create the scarecrow costume 0/1 - the combine (see section 4)
3. Look near the guard tower to the southwest 0/1 - EQR map marker 1. EQR: "This will auto update at the spot, near a rock"
4. Wait for the Magnificent Winter Squash 0/1 - EQR: "While in the Scarecrow Illusion you created, this will eventually update, make sure to stay in the Scarecrow Illusion for future step Wait updates"
5. Look near the farm to the north 0/1 - marker 2, auto update at the spot
6. Wait for the Magnificent Winter Squash 0/1 - "This will auto update after a bit of time"
7. Look near the farm to the southeast near undead 0/1 - marker 3
8. Wait for the Magnificent Winter Squash 0/1 - "This will auto update after a bit of time if still in illusion"
9. Look near the hills to the north 0/1 - marker 4
10. Wait for the Magnificent Winter Squash 0/1 - "...after a bit of time if still in illusion"
11. Inspect the Winter Squash Trap 0/1 - marker 5: "This will auto update at the spot, it is a Trap on the ground"
12. Defeat the non-magnificent Winter Squash 0/1 - "Defeat the Winter Squash that aggros"
13. Speak with Levy about [not finding] 0/1 - "Return to and Say 'not finding' to Levy"

Spot coordinates (ZAM walkthrough, `/waypoint` = /loc order Y, X) and the step texts ZAM quotes:
| Step | /loc (Y, X) | ZAM text |
|---|---|---|
| 3 guard tower SW | -2891, -1703 | "Travel to the first location. The Magnificent Winter Squash has been spotted near a boulder close to the southwestern guard tower." Just west of the tower near a small boulder. |
| 5 farm north | -95, -5535 | "Travel to the second location. The Magnificent Winter Squash has been seen to the north in the fields behind a farmhouse overrun by bandits." Farm with 2 huts. |
| 7 farm SE near undead | -2400, -15080 | "Travel to the third location. The farmers to the southeast have mentioned seeing strang happens near the ruins." (sic) Undead ruins east of the Wizard Spires. |
| 9 hills north | 512, -13893 | "Travel to the fourth location. There have been some rumors of a large strange orange creature running through the granite hills to the North." Forested hilly area. |
| 11 trap | 1300, -13225 | "Head northeast to the zone line... You will find a 'Winter Squash Trap' on the ground. Click it to spawn Winter Squash." |
These "Travel to the ... location" lines look like the per-step task descriptions. Whether they are exact in-game text: UNKNOWN (they came through WebFetch quotes).
Map check: the EQR marker pixels match these coordinates at about 20 units per pixel. Marker 4 is drawn about 900 units east of ZAM's 512, -13893; the rest are within ~150.

The Wait steps:
- Message at each Look/Wait (ZAM): "There are signs that something large has recently passed this way. Maybe you should keep looking." ZAM gives this text for spot 1 and says "Same update message" for spots 2-4.
- Wreck (Nov 1 2022): "When you get to each waypoint, and you get the yellow 'Task stage updated' message, wait there (maybe 15 seconds?) until you get the next yellow 'There are signs...' message, before proceeding to the next waypoint." / "And don't forget to be in costume. You won't get the updates without it."
- ZAM step 3: "click the 'Winter Squash Scarecrow Costume' to turn yourself into a scarecrow and get the update."
- Exact wait duration: UNKNOWN (only "maybe 15 seconds?", "eventually", "a bit of time").
- Whether the costume is checked only on the Wait steps or also on the Look steps: ZAM says you need it for the update at spot 1; Wreck says it is needed for "the updates". EQR ties it to the Wait steps. Exact live check: UNKNOWN.
- What happens on a Wait step (any visual, emote, or spawn) besides the "There are signs..." message: nothing recorded. UNKNOWN.
- Trap: a clickable object on the ground, name "Winter Squash Trap". Model/appearance: UNKNOWN. Clicking it updates step 11 and spawns Winter Squash, which aggros (EQR: "Defeat the Winter Squash that aggros").

## 4. Scarecrow costume
- Container: Pumpkin Carving Kit (113458): Magic, Lore, Quest; 4 slots; size capacity GIANT; weight 0.1; weight reduction 1%; "This item can be used in tradeskills." Given by Hule in Carving Pumpkins.
- Combine (ZAM): "In the 'Pumpkin Carving Kit', combine the 'Pumpkin Carving Knife', 'Perfectly Carved Pumpkin', 'Tattered Scarecrow Clothes', and 'Bale of Hay'. You will receive a stack of (5) 'Winter Squash Scarecrow Costume'."
  - So 4 items: Knife (113459) + Perfectly Carved Pumpkin (113461) + Tattered Scarecrow Clothes (113465) + Bale of Hay (13990).
  - Knife consumed: YES. EQR: "...this will use the Knife up in the combine". Search summary of ZAM: everything is consumed except the kit.
  - Perfectly Carved Pumpkin = Kit combine of Knife + Carving Pumpkin (113464); the knife is kept in that combine (Carving Pumpkins quest).
  - Skill / trivial / fail chance: UNKNOWN (no source).
- Result: Winter Squash Scarecrow Costume (113466): Magic, Lore, Quest; SMALL; stack size 1; "Expendable - Charges: 5".
  Note: EQR says Stack Size 1 + Charges 5; ZAM says "a stack of (5)" = 5 charges.
  - Lore text: "This costume has been stitched together by someone really excited at the chance to catch a pumpkin. You would think that the Nights of the Dead don't come around every year."
  - Effect: CLICK, "Any Slot, Casting Time: Instant", spell 26895 (not worn).
- Spell 26895 "Illusion: Scarecrow" (the same spell as the Enchanter 86 spell; the costume casts it):
  - SPA 58 (Illusion), base1 = 575 (race 575 Scarecrow), base2 = 3, max 3; Target Self (6); beneficial; skill Divination.
  - Duration formula 3, value 360 ticks = 36 minutes. Duration Frozen: 1. Dispellable shown Yes on the page, raw flag 0. Spell icon 163.
  - Texts: "Changes your form to that of a scarecrow." Land on you: "You feel different." Others: "Target feels different." Wear off: "You return to your normal form."
  - Whether race 575 renders in the RoF2 client: not checked (outside web scope). Verify with client_race_table.py --check before use.

## 5. Components - where from
- Bale of Hay (13990): an OLD classic item, not new. Magic, Lore, Quest; GIANT; weight 10.0; Lore group "Straw of Karana"; stack 1. EQR: "This item is a ground spawn in the following zones: West Karana".
  - EQR walkthrough: "a ground spawn around the edges and in the Miller Farm Field area, that Levy Cullpay is in".
  - ZAM comment mathscitch (Oct 11 2024): "Found bales at the following locs: -3357.82, -4195.47, 39.12; -3722.98, -5554.98, 13.60; -2673.71, -5399.90, 6.52 ... They are NOT the easiest to see but are near/within Miller's Farm square."
  - ZAM comment Drakah: "The hay is in the field itself, not in the huts. Its just a pile of sand really."
  - Grove (Nov 5 2021): "...more like a very small sand bucket of hay without the bucket."
  - Respawn timer / full spawn list: UNKNOWN. Because it is a classic item, PEQ may already have qey2hh1 ground spawns for it. Not checked (read-only, web scope).
- Tattered Scarecrow Clothes (113465): Lore, Quest; SMALL; stack 1; no other text.
  - EQR: "Tattered Scarecrow Clothes, dropped from the Scarecrows". ZAM walkthrough: "Kill 'a wandering scarecrow' and loot 'Tattered Scarecrow Clothes'."
  - Drop rate: UNKNOWN. ZAM's drop table for it is Premium-only, and ZAM's wandering scarecrow page lists only Carving Pumpkin. Whether it drops only while the task is active (task-gated loot): UNKNOWN.
- Carving Pumpkin (113464): Quest, SMALL, stack 10, "This is a perfect pumpkin to carve into a Jack O'Lantern." Drops from a wandering scarecrow ("pre-lootable and tradeable" per ZAM q10522).
- Perfectly Carved Pumpkin (113461): Quest, SMALL, stack 10, "You have perfectly carved this pumpkin into a classic Jack O'Lantern. Hule C Zarshcl will be proud of this carved gourd."
- Pumpkin Carving Knife (113459): Lore, Quest, SMALL, "This item can be used in tradeskills. / This knife has the initials H.C.Z. lovingly carved into its worn pumpkin-colored handle."

## 6. Rewards
- Ghastly Gummy Bears (94095): icon 1690; Class All, Race All; SMALL; wt 0.5; Tribute 600; Req Lvl 100; AC 155, HP 1200, Mana 950, End 600; "This is a miraculous meal! (90)"; Lore "Ghastly Gummy Bears"; stack 20; sells 0.001p. No click effect listed.
- Ominous Orangeade (94097): icon 3064; All/All; SMALL; wt 0.5; Tribute 240; Req Lvl 100; AC 155, HP 1200, Mana 1200, End 400; "This is a miraculous drink! (90)"; stack 20. No click effect listed.
  Both are stat food/drink, not clickies. No click spell or duration exists for them.
  The same items also reward Missing Pumpkins / Carving Pumpkins / The Witch's Wishes.
- Mischief server: 5 Eerie Jelly Beans (ZAM; stats not researched).
- Achievement: "Nights of the Dead: Magnificent Winter Squash" - 10 points; achievement reward "AA (Scales to Level)" / "Experience"; icon 1481. Objectives: Missing Pumpkins, Carving Pumpkins, Squashing Pumpkins.
- Task XP: UNKNOWN.

## 7. Repeatable / lockout / level / group
- Repeatable: Yes (EQR + ZAM). Lockout/timer: none stated. UNKNOWN whether live has a repeat timer.
- Level: ZAM 0-125. Reward food needs level 100 to eat.
- Solo task (EQR "Task Type: Solo"). Note from Carving Pumpkins: its kill step updates a whole group; for Squashing, nothing on group credit (UNKNOWN).
- Requires Carving Pumpkins first: no hard gate documented (UNKNOWN). In practice you need its Kit + Knife (section "Prerequisite / chain").

## UNKNOWN summary
1. Exact wait time on the "Wait for the Magnificent Winter Squash" steps (only "maybe 15 seconds?").
2. Winter Squash race id/texture, HP, damage, special abilities, loot.
3. Levy's race id, gender, and any reply when hailed mid-task or after completion.
4. Winter Squash Trap object model.
5. Tattered Scarecrow Clothes drop rate and whether the drop is task-gated.
6. Bale of Hay respawn timer and full spawn list (3 locs known).
7. Rewards: both items or a choice of one; task experience amount.
8. Combine skill/trivial (presumably none or no-fail, but not documented).
9. Whether Levy requires Carving Pumpkins done (hard gate) - not documented.
10. Exact single word "run around" vs "wander" in Levy's [run around] reply (two ZAM reads differed).
11. Whether the illusion is checked on the Look steps or only the Wait steps.
