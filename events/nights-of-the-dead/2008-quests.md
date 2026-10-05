# Nights of the Dead 2008 quests: Rongol #1, Rongol #2, Necromancer's Garden

Gathered 2026-10-05. Read-only web research plus read-only greps of the local peq dump and our quest tree; nothing
under C:\Git\test was changed.

**Quote reliability.** Allakhazam returns 403 to curl and PowerShell, so every Allakhazam text below came through
WebFetch, which runs the page through a summarizing model. I asked for word-for-word output each time.
- Quest walkthroughs 4901, 4902 and 4903 came back as dialogue lines that read as verbatim; still treat the exact
  punctuation as **possibly paraphrased**.
- Comments marked (V) came back as quoted text. Comments marked (P) were condensed by the tool and are paraphrased.
- The everquest.com 2008 news article, the EQ Resource item and spell pages, the patch notes (local patcheq copy),
  the peq dump and the GitHub files were read raw or verbatim and are exact.

**Coordinate convention.** Allakhazam and Bonzz numbers are in **/loc order (Y, X, Z)**. Proof:
- peq spawn2 for Innkeep Danin is y=-1513.88, x=-13004.88, and Allakhazam shows "-1514, -13005, 17".
- A 2009 Allakhazam comment pastes "[Sun Nov 01 19:04:39 2009] Your Location is -1115.13, -1930.06, 25.14", which is
  /loc output, at Leavalin; the quest page gives "-1115, -1930, 25".
- Brewall-format map labels store (-X, -Y), and they agree.

Bonzz calls its numbers "/waypoint", but they are in the same Y, X order as /loc.

---

## 0. Year and level questions settled

### Year: all three are **2008** (Allakhazam's "2007" / "2009" labels are wrong)
- **Official news, Oct 22 2008, "The Haunting of Norrath is Here!"** (https://www.everquest.com/news/imported-eq-enus-51169).
  It lists "**Fresh Hauntings!**: Necromancer's Garden ... Scarecrow Roundup" as the new content, running Oct 24 to
  Nov 7, 2008. Exact text of both entries:
  > **Necromancer's Garden** A crazed necromancer has recently snuck into Greater Faydark and spread some sort of
  > seeds about the forest. The seeds have taken root and are sprouting into horrible skulls! Leavalin Mossbite was
  > tasked to hire adventurers to help stop a threat to the folks of the Faydark.
  >
  > **Scarecrow Roundup** Rongol and Anderia's farm in West Karana has been struggling, leaving them little to sell and
  > barely meeting their own needs. Believing he figured out how the Millers have been so successful with their farm
  > all these years, Rongol created a scarecrow but his effort was unsuccessful and forced him to take more drastic
  > measures. He sought the help of a witch. Unfortunately, the magical powers of the witch were a bit more than
  > Rongol and Anderia were prepared to handle. The couple is now seeking the help of brave adventures.

  The same article lists **Corporal Gravlin** (Undead Rising) under "Ancient Hauntings", which means it existed
  before 2008. That settles the inventory's Undead Rising "2007 vs 2009" conflict: it is 2007, not 2009. The article
  gives **no levels**.
- **Patch notes, Oct 29, 2008** (local patcheq copy notd/raw/patches/p-2008-2.txt:630-743):
  "The Haunting of Norrath continues until Novemeber 7th."; "Fixed a pathing bug in West Karana that was causing
  scarecrows to be far too scarce."; and, under Previously Hotfixed, "Corrected a faction issue with Rongol and Anderia
  that was preventing some races from getting their quests." No levels are given. No other 2007-2010 patch note names
  these quests, Leavalin, the shillelagh or the skulls (grepped p-2007-2 .. p-2010-2, p-2014-2 .. p-2017-2).
- Allakhazam's Leavalin NPC record says "NPC Added: 2008-10-28". The first comment, by Rickymaru, is dated Oct 28 2008.
- Allakhazam quest 4902's page says the entry was made on Oct 29, 2009, which is probably why that page says "2009".
  A 2009 comment on it says "In 2008 most of the scarecrows for this quest were way up in the NE corner of the zone."

### Necromancer's Garden minimum level: every source

| Source | What it says | Notes |
| --- | --- | --- |
| Allakhazam quest 4903 header | Level **70**, max 125 | No reasoning given. The same database gives Scarecrow Roundup 1-125, even though its Scarecrow Potion also needs level 70, so 70 is probably not the task's own gate. |
| Allakhazam item pages, Blessed Shillelagh (78939) and Worm Skull Muffin (78935) | "Level to Attain: 70" | This is Allakhazam metadata copied from the quest level. The stat blocks themselves have **no** "Required level" line (checked both). |
| Floating Skull Potion: Allakhazam 78934, EQ Resource 80057, peq 80057 | **Req Lvl 70** (item) | The item needs 70. The task does not. |
| Scarecrow Potion (Rongol #2 reward): EQR 80058, peq | **Req Lvl 70** (item) | The quest is still listed 1-125. |
| **Oxgoad (ZAM Administrator), Oct 28 2015**, Allakhazam quest 4903 (V) | "You can do this quest at least as early as level **11**, but you can't use both rewards, just the stat food. Also, the lockout timer is definitely back. It's 20 hours." | **The only first-hand statement of the level a character took the task at.** It is the source of the wiki's 11. |
| Allakhazam wiki EQ:Halloween (last modified 2023-04-03) | Min. Lvl **11**. Row: "Necromancer's Garden \| Shared (1-6 players) \| 11 \| Leavalin Mossbite \| Greater Faydark \| Floating Skull Potion, Worm Skull Muffin \| 2008 \| Clickie the skulls to death! The Floating Skull Potion has a required level of 70, but the stat food can be used by all. 20 hour lockout on completion." | Same table: Carry the Torch and Scarecrow Roundup min **1**. |
| willimina, Nov 05 2009 (V) | "You can't use the potion reward until level 70." | About the item, not the task. |
| Allakhazam quest 8834 (Garden Variety Ghouls achievement: Carry the Torch + Scarecrow Roundup + Necromancer's Garden + Witch's Wishes) | Levels 1-125 | This is achievement metadata. |
| Player levels in comments | Wreck 2014 signs as "Drudarn Canbakeit 100 Druid"; Sonicmurphy 2012 is a bard (no level); Andhrimnir 2024 did it on Yelinak TLP (SoD era), no level | None of these say what the minimum is. |
| everquest.com 2008 / 2010 / 2014 news, Oct 2008 patch notes, Bonzz | No level stated | |
| EQ Resource | Has no page for this quest. Its NotD guide covers only 2021, 2022 and 2025. | |
| Fanra wiki, Wayback Machine, eqshadowknight.net thread | Could not read: 403, 429 / "unable to fetch", and a JS redirect | |

**Conclusion.** No source shows a task-side level gate of 70. The only first-hand report is that the task works at
level 11 or lower, with the reward potions locked to 70+. The exact minimum (1? 10? 11?) is **not documented
anywhere I could reach**. A gate at or below 11 matches the evidence. The two illusion potions are Req Lvl 70 on live
(Scarecrow Potion included), which matters at our 65 cap.

---

## 1. Nights of the Dead: Rongol #1 - Carry the Torch (Allakhazam 4901)

Sources: https://everquest.allakhazam.com/db/quest.html?quest=4901 ; Bonzz https://www.bonzz.com/nightsofthedead.htm
- Type: task, solo (1 player). Level 1-125. Repeatable with **no lockout**. Allakhazam: "Era: Secrets of Faydwer"; the
  real year is 2008 (section 0). Zone: West Karana (peq qey2hh1).
- Experience or other reward: **none stated anywhere**. The completion text only says "Rongol seemed pleased that you
  would take your time to help him out."

### Dialogue (Allakhazam walkthrough, possibly paraphrased in punctuation)
The hail is the same line as the classic Rongol hail, so the existing classic Rongol script already says it.
- You say, 'Hail, Rongol' -> Rongol says 'Great!! I have fifty acres to seed and now I have visitors stopping by to waste my time!!'
- You say, 'What's up with all the crazed scarecrows?' (**not bracketed in the hail; a hidden keyword**) -> Rongol
  says 'Oh, so you noticed them, eh? Well, there are a few more than I'd expected. And, well, I guess I never asked the
  [witch] to make them scary, not exactly. And when she asked me if I wanted more than one, of course I said yes! I
  don't see how any of this is my fault.'
- 'What witch?' -> 'That crazy wart-faced old hag! All I wanted was to have a chance at a good farm. The Millers have
  those scarecrows, you see. They scare off the vermin and most of the bandits as well. So their fields grow and they
  actually get to harvest most of their crops. If anything crops make past the vermin to harvest in our fields they are
  taken by the bandits! So I thought we could use some help, magical help. Well, I guess I got what I [asked for], and
  then some!'
- 'You asked for..' -> 'I had made this scarecrow, you know, out of straw and old clothes. I plopped on a pumpkin,
  which I had to buy from the Millers, and set it out in the fields. Of course it didn't help. The vermin don't notice
  the thing, except to eat parts of the pumpkin, and it certainly doesn't scare any bandits. So I ask around. The
  Millers have no idea where their scarecrows came from, so they can't help. But I hear about a witch livin' [under the
  bridge], so I go lookin' for her.'
- 'Under the bridge?' -> 'I thought it was crazy too. How could anyone live under that bridge and not be noticed by
  the guards? But I went, and sure enough, a witch steps out of the waters with a fish in her mouth. I know she's a
  witch 'cause she's so ugly, you see. I explain to her my problem and she cackles and tells me that she'll do as I
  ask, I just have to bring her a [jade bowl].'
- 'A jade bowl?' -> 'I can't afford a jade bowl! I mean, I can't without using up all of our savings, which isn't
  much. Even then I had to promise Crow a discount on any crops I have for sale next harvest. I even named the stupid
  scarecrow after him. I bring the bowl to the witch, and she comes along and has me say exactly what I want. I told
  her I wanted a scarecrow that could walk around in my fields. She asks me if that's all, if I don't want more. I
  says, sure, more is good. She laughs and casts her spell. The she just walks away. That stupid scarecrow just keeps
  makin' more of itself and they wander all over the place! I don't suppose you could [help] me corral these things?'
- 'I'll help' -> "You have been assigned the task 'Carry the Torch'." Rongol says 'That would be so kind of you! I've
  found that they're sort of afraid of fire, so the first thing we'll need to do is set up some torches around the
  coral. That way if we can get them into the corral they might stay there. Of course I don't have any torches left, I
  sort of used mine trying to keep those things out of the house. I'm sure Dannin, the Innkeep, will have some. Four
  should be enough.'
  (Live text spells it "coral" and "Dannin". Crow is a real PoK/Qeynos-area merchant: peq npc 2063 'Crow',
  General Supplies.)
- Task step: **"Deliver 4 Torch to Anderia 0/4 (West Karana)"**. Give 4 Torches to Anderia, who stands near Rongol.
- "Your task 'Carry the Torch' has been updated." Rongol tells you, 'Wonderful! We've hired some folks to hold the
  torches. Now all you need to do is get some of those crazed scarecrows into the corral. I've got a few [pitchforks],
  Karana knows I don't need them for my crops. I bet you can prod them into the corral. If you could just get enough
  of them into the corral maybe we can be free of them.'
- "Rongol seemed pleased that you would take your time to help him out."
- Anderia says 'Ah, Rongol, your friends have brought us torches. This should help.'
- Scripted: "The hired hands in the house behind Anderia then move into place around the corral."
- Scripted: "When the torches go out (in about an hour) the hired hands return to the house and any captured
  scarecrows are released (your task stays updated)."
  - a crazed scarecrow says 'We blew and we blew and finally blew your torches out!'
  - a crazed scarecrow says 'Run away!'
- Galadrena (Oct 30 2022, V): when the hands went home at 9/10 on Roundup, "I didn't know you could reset them by
  doing the first quest again. I did and the hire hands came back. You only get the update when the hired hands are
  there." So the hired-hand state is **zone-wide** and any player's Carry the Torch turn-in resets it.

### Torches
- Innkeep Danin sells Torch for **1sp** (Allakhazam merchant list). Allakhazam walkthrough: "a building along the path
  going east. If you have sneak, you can sneak behind him and right click to shop regardless of faction."
- Comments: an Iksar could not buy and ported to PoK for torches (Oct 24 2014, P). Zaztik (Nov 01 2009, V): "torches
  can be bought in PoK for part 1 of the quest."
- Item: **Torch, live id 13002** (EQ Resource https://items.eqresource.com/items.php?id=13002): "Placeable, Quest",
  Slot Secondary, SMALL, WT 0.5, lore text "Torch", aug slot 1 type 7, usable in tradeskills. **Not** No Trade and
  **not** Lore. peq 13002: nodrop=1 (tradeable), questitemflag=1, light=2, itemtype 16, price 10. It is on Danin's peq
  merchant list (merchantlist 12102 slot 10). The live text does not show whether the delivered torches are consumed;
  the "Deliver" step type normally takes them.

---

## 2. Nights of the Dead: Rongol #2 - Scarecrow Roundup (Allakhazam 4902)

Source: https://everquest.allakhazam.com/db/quest.html?quest=4902
- Type: task, solo (1-1). Level 1-125. Repeatable, **18-hour lockout** (Allakhazam). Sonicmurphy (2012) says
  "repeatable every 19 to 20 hours". Allakhazam: "Era: Secrets of Faydwer"; the real year is 2008.
- Prerequisite: none on the task itself. "You can request Scarecrow Roundup without having done Carry the Torch but
  you cannot get any updates without the hired hands being in place around the corral. So if multiple people are doing
  at the same time, only one needs to complete Carry the Torch." Allakhazam wiki: "Someone must complete Carry the
  Torch in order to spawn the mobs who will corral the scarecrows."

### Dialogue
- Rongol tells you (end of #1) ... [pitchforks] ... (see above)
- You say, 'Pitchforks?' -> "You have been assigned the task 'Scarecrow Roundup'." Rongol says 'Aye, here ya go.
  Don't hold back, those pumpkin-headed chatterboxes could use some serious stabbing.' "You receive Rongol's Pitchfork."
- Task step: **"Force the scarecrows into the corral with the pitchfork Rongol gave you 0/10 (West Karana)"**
- Completion: "Your task 'Scarecrow Roundup' has been updated." "Rongol and Anderia are very grateful to you for your
  help." "You have successfully been granted your reward for: Scarecrow Roundup". Reward: **20 Spiced Crow's Blood,
  10 Scarecrow Potion**.
- Sonicmurphy (Oct 21 2012, V): "the reward for the potion scarecrow illusion is only from the first time you complete
  quest.. if you do the quest more than once you only get the food as the reward .. did it twice so i know".

### Mechanic (walkthrough plus comments)
- "Equip the pitchfork. It's a 2-hander, so remove your secondary first. Click the pitchfork while standing next to
  and targetting a crazed scarecrow. Hopefully it will go toward the corral that is surrounded by the hired hands.
  Usually away from you. The scarecrows path randomly around and if they stop long enough in the corral they will be
  caught. By using the pitchfork you can encourage them to path through and stop in the corral. You have to be somewhat
  near the corral when they are caught to get the update."
- Galadrena 2022 (V): "make sure you are on top of the mob before you click the pitchfork, else nothing will happen.
  Clicking the pitchfork makes the scarecrow run in a random direction."
- Wreck 2014 (V): "They run about 50 feet... If you're too close to the corral, they will run right through and you
  won't get credit... get about 55 feet away from the corral when you poke the scarecrow... It took me a little over an
  hour to do 10 Scarecrows... I was grouped, and we did not get each others updates." (signed "Drudarn Canbakeit 100
  Druid Prexus").
- Ironic and Diani 2017 (V): it will not equip unless the secondary slot is empty; it is classed as a 2H piercer.
- (Deleted user) Oct 31 2009 (V): the scarecrow "always either run through it or stops right next to it becoming stuck
  and un clickable."
- Lenaddar 2016: about 20 minutes. Zaztik 2009: about 15 minutes.
- **The corral's location, the number of crazed scarecrows, their spawn points and respawn time, and the radius that
  counts as "in the corral" are not published anywhere.**

---

## 3. Nights of the Dead: Necromancer's Garden (Allakhazam 4903)

Sources: https://everquest.allakhazam.com/db/quest.html?quest=4903 ; Leavalin
https://everquest.allakhazam.com/db/npc.html?id=31561
- Type: **shared task 1-6** (Allakhazam header and wiki). Rickymaru 2008 called it "a solo task" that needs friends.
- Level: see section 0. Allakhazam says 70-125, but the evidence points to 11 or lower.
- Time limit: Allakhazam header "approximately 10 minutes". Wreck 2014 (V): "The quest is 10 minutes long". Rickymaru
  2008 (V): "There is a time limit to this task. I believe its 7 minutes." Yther Ore 2009 (V): "very short 5min or
  less, I forget the exact time." **The exact time limit is unconfirmed: reports say 10, 7, and 5 or less minutes.**
- Lockout: 20 h. Loknessy 2009 (V): "The lock out timer is 20 hours". willimina 2009, Sonicmurphy 2012, Oxgoad 2015:
  "definitely back. It's 20 hours". Wreck 2014: "They removed the 20 hour lock out" (that year only).
- Failure: the task expires when the timer runs out. No failure text is published.

### Dialogue (Allakhazam, possibly paraphrased in punctuation)
- You say, 'Hail, Leavalin Mossbite' -> Leavalin Mossbite says 'Hail adventurer! Please, I know you have much to do,
  but the Faydark needs your [assistance]!'
- 'Assistance?' -> 'The forest and her people are under attack by nefarious magics! Someone, most likely a
  necromancer of great power, has planted some sort of seeds in the forest to the north west of here. These seeds
  cannot be purged from the ground despite the best efforts of our druids. And now that the Nights of the Dead have
  arrived, these seeds are coming to [life]!'
- 'Life?' -> 'Perhaps life was not the proper word. The seeds are sprouting into deadly skulls! They spring from the
  ground and gather their strength for but a moment, then they seek out the good folk of the forest and attack them
  with dark magic! It is believed that the skulls will cease to sprout once the Nights of the Dead have passed, but
  until then we need help crushing them. They must be crushed with a magical shillelagh that I can provide you, and it
  must be done moments after they sprout. Unfortunately the power of the shillelagh is short lived, so you must hurry
  and crush as many as you can. I can even offer a small reward should you defeat a satisfactory number of them in
  time. Will you [help]?'
- 'I'll help' -> Leavalin Mossbite says 'Thank you! Here is what you need. Go quickly and go with the will of Tunare and
  the thunder of Karana!' "You have been assigned the task 'Necromancer's Garden'." "You receive Blessed Shillelagh."
- Task step: **"Destroy the skulls growing in Greater Faydark before they become too powerful 0/10 (Greater Faydark)"**
- Reward (Allakhazam): "10x Floating Skull Potion, Worm Skull Muffin". A comment on the Leavalin page (Rickymaru 2008,
  as attributed by the tool) says "Once you complete it you will get 20 Worm Skull Muffin and 10 Floating Skull
  Potion." Merf 2009 (V): "The reward is a stack of 10 Floating Skull Potion, 1 charge each." willimina 2009 (V): "It
  seems that once you have completed the quest one time, you only get the food as a reward." **The muffin count
  (1 vs 20) is unconfirmed.** 20 matches Rongol #2's 20 drinks.
- Faction text: Yther Ore 2009 shows "Leavalin Mossbite regards you indifferently -- what would you like your
  tombstone to say?"

### Mechanic
- Rickymaru 2008 (V): "You will need to find skulls and pound them into the ground with an item that she gives you. It
  refreshs every 6 seconds and you will need to pound each skull in at least 8 times".
- Yther Ore 2009 (V): "The clicky on the Shillelagh only takes the skulls down about 18-20%, so it takes several
  clicks".
- Wreck 2014 (V): "you track Graveskull, run to the first mob, target him, and right click on the Shillelagh (in your
  primary slot). He will stay at 100% health, but he will get smaller and smaller with each hit. After the 10th hit, he
  will break apart, still with 100% health. There seems to be groups of three mobs close by... some of the mobs poof.
  They just disappear... The respawn time on the mobs is about 10 seconds (according to tracking), but they rarely
  respawn in the same spot."
- **Any mob in the zone counts** (Sonicmurphy 2012, Sheldor 2014, Edenwrath 2015, Dogpaw 2022). Clicks scale with
  mob size: Edenwrath 2015 (V): "Bats, and faeries are 2/3 clicks, Wasps, skeletons, and orc pawns are 4/5 Wolvesn and
  drakes are 5/6". HSishi 2017: "Pixies need 2, spiders, 3, ... trees and bigger fat orks more than 6." So the
  mechanic is: each Pound shrinks the target by a fixed step, and the target "breaks apart" (despawns) and gives
  credit once it is small enough. Kills do not count.
- Group credit: Loknessy 2009 (V): "Everyone must be near the skull that is being pounded to get credit for the kill."
- Skull location: Adani 2014: "Skulls are actually Northwest of NPC". The NPC dialogue also says "north west". A
  summary of Yther Ore's comment said "northeast"; that word did not appear when I asked for the comment verbatim.
- Live bug since 2022: frothel 2022 and Andhrimnir 2024 say you can target yourself and click 20 times (10 to shrink
  you, 10 for updates). Andhrimnir: the self-shrink "doesn't seem to work outside of GFay". This suggests live counts
  any "shrink to the minimum" on any target in Greater Faydark.
- Mobs: "Graveskull" is the name players track. **No database has an entry for it**: Allakhazam search "graveskull"
  finds nothing, and so does EQ Resource. Its level, race, exact name ("a graveskull"?), spawn points and count are
  unknown. The likely model is the floating skull (EQEmu race 512 FloatingSkull, the same as the reward illusion),
  but **no screenshot was found** to confirm it.

---

## 4. NPCs

| NPC | Live (Allakhazam) | Location (/loc Y, X, Z) | Look | peq (local dump) |
| --- | --- | --- | --- | --- |
| **Rongol** | id 2687, level 5. "This mob spawns at -3696.19, -9281,69, -1.44 in the south center part of West Karana. Only spawns during the Nights of the Dead period around october." Allakhazam also lists the classic quest Temple Blankets for him, so live seems to have a NotD-only copy, or the spawn text is wrong. **Unconfirmed.** | -3696.19, -9281.69, -1.44 (quest page: -3695, -9280, -1.44). Bonzz: "a barn in the mid-south part of the zone (area of /waypoint -3700, -9280)" | Human male, bald, blond goatee, black sleeveless tunic, maroon pants, brown boots. Nameplate "Rongol (Nights of the Dead Quests)". Screenshot https://zam.zamimg.com/images/0/b/0b62703bf70ca7ed48b2b222a0142e72.jpg | **Exists, classic**: npc_types 12107 'Rongol', level 4, race 1, gender 0, class 1, texture 0, face 0, faction 121, loottable 5131, hp 56. spawngroup 6238 (100%), spawn2 4085 qey2hh1 x=-9290 y=-3706 z=-0.13 heading 146, respawn 640. No content flags. |
| **Anderia** | id 2689, level 6 | -3723, -9255 ("near Rongol") | Human female, black bob hair, white blouse, blue bodice, brown capri pants. Screenshot https://zam.zamimg.com/images/9/2/920cc811cf2c5f12af9702227df40764.jpg (a wall torch is visible behind her) | **Exists, classic**: 12106 (level 5) and 12152 (level 4), race 1, gender 1, face 1, faction 121, loottable 5132. spawngroup 6237 (50/50), spawn2 4084 x=-9256 y=-3725 z=-0.13 heading 409. |
| **a hired hand** (x4) | id 53254, level 5. "4 of them take place around the corral during the Nights of the Dead task" | Idle "in the house behind Anderia"; they walk to the corral. **Corral coordinates are unknown.** | Human male, white hair and beard, the same black tunic as Rongol, holding a lit torch. Screenshot https://zam.zamimg.com/images/6/8/681e09492b3363f178e6755cd582ad45.jpg | **Not in peq** |
| **a crazed scarecrow** | id 41040, level 25, Undead, "Mob sees through invisibility: Yes". stef0knee 2014 (V): "Cannot attack and cannot be attacked, although they con kos." | West Karana. 2008: mostly in the NE corner (pathing bug fixed 10/29/2008). | Pumpkin jack-o'-lantern head, blue long coat, red sash, ragged legs. This looks like the newer scarecrow model (probably EQEmu race 575 Scarecrow2), not classic race 82. **Unverified.** Screenshot https://zam.zamimg.com/images/e/7/e7bde09ebd1c1abab27e2148f013e7bb.png | **Not in peq**. peq does have classic an_animated_scarecrow 12003/12121/12129 and a_scarecrow 12186 (race 82), and Scary_Miller 12174. |
| **Innkeep Danin** | id 2722, level 30, merchant, Findable: No. Faction: + Circle of Unseen Hands; - Coalition of Tradefolk, Antonius Bayle, Merchants of Qeynos, Guards of Qeynos. Sells 12 items incl. Torch 1sp. | -1514, -13005, 17 | Human male, reddish hair, green shirt, brown apron. Screenshot https://zam.zamimg.com/images/i/d/id2722.png | **Exists**: 12102 'Innkeep_Danin', level 30, race 71, class 41, merchant_id 12102, faction 95. spawngroup 6233, spawn2 4080 x=-13004.88 y=-1513.88 z=17.13 heading 101. merchantlist 12102 includes Torch 13002. |
| **Leavalin Mossbite** | id 31561, level **85**. "This mob spawns at -1110, -1941 on the north path coming from Northern Felwithe." NotD only. NPC added 2008-10-28. | -1110, -1941 (quest page -1115, -1930, 25; Yther Ore /loc -1115.13, -1930.06, 25.14). Good's map label: `P 1941.5988, 1110.4153, 23.4731 ... Leavalin_Mossbite_(Q)` = /loc (-1110.4, -1941.6, 23.5). Bonzz: "/waypoint -1100, -1940". | Female elf (blonde, pointed ears; high or wood elf, not certain), full silver plate-style armor. Nameplate "Leavalin Mossbite (Nights of the Dead Quests)". Screenshot https://zam.zamimg.com/images/b/a/ba007ecbc3f49d4f31b63c955e0e1356.jpg | **Not in peq** |

Race and gender are not printed on any of these Allakhazam pages. The "Look" column is from the screenshots.

---

## 5. Items (live ids = EQ Resource ids, and they are the same ids in peq)

| Item | Live id | Flags (EQ Resource / Allakhazam) | Details | peq row |
| --- | --- | --- | --- | --- |
| Torch | 13002 | Placeable, **Quest** | Secondary, SMALL, WT 0.5, lore "Torch", tradeskill item. Danin sells it for 1sp. | 13002 exists, sold by Danin |
| **Rongol's Pitchfork** | **49060** | **Lore, No Trade, Placeable** (not Temporary, not Quest) | Slot Primary, skill **2H Piercing**, no damage or delay listed, MEDIUM, WT 3.0, Class/Race ALL. Effect **Prod** (spell 12888), Must Equip, Casting Time: Instant, Recast Delay 5s, recast type -1, Unlimited charges. Lore text "A pitchfork". ITFile 11035 (shared with Farmer's Pitchfork / Pitchfork of the Town Rebels; tssequip.eqg). Not sellable. | 49060 exists: itemtype 35, slots 8192, nodrop 0, loregroup -1, clickeffect 12888, clicktype 4, recastdelay 5, icon 1861 |
| **Blessed Shillelagh** | **49061** | **Lore, No Trade, Placeable** | Primary, MEDIUM, WT 3.0, ALL/ALL. Effect **Pound** (spell 12887), Must Equip, Instant, Recast 6s, recast type -1, Unlimited. Lore "A tree limb given by the forest to the heroes of Faydark". ITFile 10945 (tssequip.eqg). **No Req Lvl.** | 49061 exists: itemtype 11, slots 8192, nodrop 0, loregroup -1, clickeffect 12887, casttime 2, recastdelay 6, icon 1803 |
| **Scarecrow Potion** | **80058** | Magic, No Trade, Expendable, 1 charge | **Req Lvl 70**. Effect **Illusion: Scarecrow** (spell 6107), Any Slot, cast 1.5s, recast 5s, recast type 13. SMALL, WT 0.3, stack 10. Lore "Made with crushed straw and tattered fibers". | 80058 exists (reqlevel 70, stacksize 10) |
| **Spiced Crow's Blood** | **80060** | No Trade | Drink ("flowing drink! (50)" on EQ Resource; Allakhazam says duration 42; peq casttime_ 42). STA +6, INT +6, WIS +6, HP +15, Mana +25, SV Magic +15, SV Poison +15. SMALL, WT 0.1, stack 20. Lore "A popular drink among ghouls and goblins". No level requirement. | 80060 exists, matches |
| **Floating Skull Potion** | **80057** | Magic, No Trade, Expendable, 1 charge | **Req Lvl 70**. Effect **Illusion: Floating Skull** (spell 13393), Any Slot, cast 1.5s, recast 5s, recast type 13. SMALL, WT 0.3, stack 10. Lore "The skulls writhe in rotting splendor". | 80057 exists (reqlevel 70) |
| **Worm Skull Muffin** | **80059** | No Trade | Food (Allakhazam: "This is a feast!", Feast(42)). STA +15, INT +15, WIS +15, CHA -5, HP +30, Mana +20, SV Fire +5, SV Cold +5, SV Disease -5, SV Poison -5. SMALL, WT 0.2. Allakhazam: stack 20; EQ Resource shows "Stack Size: 0". Lore "Most of the nutrition comes from the worms". **No Req Lvl** in the stat block. | 80059 exists (stacksize 20) |

Note for peq rows: nodrop=0 means No Trade in EQEmu; peq weight is x10 (30 = 3.0); norent=1 means not temporary.

### Click spells (EQ Resource spell pages + peq spells_new)
- **12888 Prod**: "Prods the target in the right direction... Hopefully!" Not a player spell. Instant, Target **Self**,
  Beneficial, skill Conjuration. peq: effectid1=10 (empty CHA placeholder), targettype 6. **The behaviour (making the
  scarecrow flee in a random direction about 50 ft) is server-side and must be scripted.**
- **12887 Pound**: "Pounds the target into the ground!" Same shape (Self, effect 10 placeholder). **The shrink step,
  despawn and credit must be scripted.** The live self-target bug (shrinking yourself) suggests live applies a shrink
  to the current target, or to the caster when it targets itself.
- **6107 Illusion: Scarecrow**: Slot 1 "Illusion: Old Scarecrow" (peq base 82 = classic scarecrow race), cast 1.5s,
  recast 1m30s on the spell, duration 36m, Divination, Self. Land text "You feel different." / "'s image shimmers." /
  "Your illusion fades." Also used by Guise of Horror (52356) and Scrumptious Jack-o-Lantern (87311).
- **13393 Illusion: Floating Skull**: race 512, duration 36m, Self. "Cloaks you in a shimmering illusion that makes you
  appear to be a giant floating skull."

---

## 6. ProjectEQ / EQEmu status

- **peq dump** (notd_web/peq-dump/create_tables_content.sql, Sep 2025):
  - Rongol 12107, Anderia 12106/12152, Innkeep_Danin 12102 (+ merchant list with Torch 13002) exist as **classic**
    NPCs. Spawns are listed in section 4.
  - All 6 quest items and all 4 click spells exist at their live ids.
  - **Absent**: Leavalin_Mossbite, a_hired_hand, a_crazed_scarecrow, any Graveskull, and any `tasks` or
    `task_activities` row for "Carry the Torch", "Scarecrow Roundup" or "Necromancer's Garden". The dump has zero
    matches for those strings and for "Nights of the Dead".
- **GitHub ProjectEQ/projecteqquests**:
  - qey2hh1/Rongol.lua is classic only: hail, "follower of Karana", "blanket", "karana bandits", and the Temple
    Blankets turn-in.
  - There is no Anderia, Innkeep_Danin, hired-hand or scarecrow script.
  - gfaydark has no Leavalin, Mossbite, skull or graveskull file.
  - GitHub code search across all repos found no EQEmu script for Leavalin, Graveskull, crazed_scarecrow, "Scarecrow
    Roundup" or "Necromancer's Garden". The hits were only map labels (Good's gfaydark_2 Leavalin label) and
    actordef.h IT model names.
- **Our tree** (read-only look): C:\Git\test\NMS-Quests\qey2hh1 has **both Rongol.lua and Rongol.pl** (classic
  Temple Blankets only; commit 8ebd4b7). gfaydark has no Leavalin. EQQuests has no entry for these three quests.

---

## 7. Could NOT find (not guessed)

1. Necromancer's Garden's **exact minimum level**. The only evidence is that it is 11 or lower (Oxgoad 2015). Nothing
   supports 70 as a task gate.
2. Necromancer's Garden's **exact time limit** (reports say 10, 7, and 5 or less minutes) and the **muffin count**
   (1 vs 20).
3. **Experience** or coin rewards for any of the three tasks.
4. The **Graveskull** NPC: exact name, level, race/model, spawn points, how many, respawn (about 10 s per Wreck 2014),
   and whether it attacks players (the dialogue says the skulls "attack them with dark magic").
5. The **shrink step per Pound** and the exact despawn threshold. Players give click counts by mob size (2 to 10).
6. The **corral** location, its radius, the hired hands' home and post coordinates, the number of crazed scarecrows,
   their spawn points and respawn timer, and the exact torch duration ("about an hour").
7. The crazed scarecrow's race number (looks like the pumpkin-head model, probably 575) and the hired hands' textures.
8. Leavalin Mossbite's exact race (elf, high or wood) and texture. Race/gender/class are not printed for any of these
   NPCs on Allakhazam.
9. Whether live's Rongol is a separate NotD-only spawn or the classic NPC with an event lastname (Allakhazam's spawn
   text and its Temple Blankets link conflict).
10. Whether Anderia keeps the 4 torches (the step is "Deliver").
11. Failure, expire and lockout messages; the task descriptions shown in the task window (Allakhazam gives only the
    step text).
12. Fanra's wiki (403), the Wayback Machine (429 / blocked) and the eqshadowknight.net 2008 thread (JS redirect) were
    unreadable.

## Sources
- https://everquest.allakhazam.com/db/quest.html?quest=4901 , =4902 , =4903 , =8834
- https://everquest.allakhazam.com/db/npc.html?id=2687 (Rongol), 2689 (Anderia), 53254 (a hired hand), 41040
  (a crazed scarecrow), 2722 (Innkeep Danin), 31561 (Leavalin Mossbite)
- https://everquest.allakhazam.com/db/item.html?item=78934 , 78935 , 78936 , 78937 , 78938 , 78939 (Allakhazam ids)
- https://everquest.allakhazam.com/wiki/EQ:Halloween
- https://www.everquest.com/news/imported-eq-enus-51169 (Oct 22 2008) ; https://www.everquest.com/news/imported-eq-enus-52055
  (2010) ; https://www.everquest.com/news/nights-of-the-dead-2014
- https://items.eqresource.com/items.php?id=13002 , 49060 , 49061 , 80057 , 80058 , 80059 , 80060 (saved in notd/r2008/)
- https://spells.eqresource.com/spells.php?id=12887 , 12888 , 13393 , 6107 (saved in notd/r2008/)
- https://achievements.eqresource.com/achievements.php?id=200115 (Garden Variety Ghouls objectives)
- https://www.bonzz.com/nightsofthedead.htm
- github.com/nazwadi/patcheq (local copy notd/raw/patches/p-2008-2.txt lines 630-743)
- github.com/ProjectEQ/projecteqquests qey2hh1/Rongol.lua, qey2hh1 and gfaydark listings
- github.com/RedGuides/goodurden-maps "Good's Maps/gfaydark_2.txt" line 37 ; github.com/xackery/eq-darkmodemaps
  rof2/qey2hh1_1.txt lines 77-78
- Local peq dump notd_web/peq-dump/create_tables_content.sql (npc_types, spawnentry, spawn2, merchantlist, items,
  spells_new); extracts in notd/r2008_items_peq.txt and notd/r2008_npcs_all.txt
- Screenshots downloaded to notd/r2008/img_*.jpg|png
