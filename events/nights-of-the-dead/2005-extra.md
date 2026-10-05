# Nights of the Dead 2005: extra detail for Trick or Treat for the Old Man, The Hungry Halfling, Out With the Old

Gathered 2026-10-05. Read-only. Adds only what EQQuests does not already have. Existing text:
- Trick or Treat for the Old Man: `expansions/01-ruins-of-kunark.md:12417-12521` (full dialogue, codex clues, all ten
  NPCs and their treat lines).
- The Hungry Halfling and Out With the Old: `events/nights-of-the-dead.md:186-243` (dialogue, recipes, waves, rewards;
  Out With the Old's story dialogue is shortened there).
- Bone Mask of Horror: `events/nights-of-the-dead.md:143-182`.

Tags: **[V+]** two sources agree, **[V]** one verbatim WebFetch transcript of Allakhazam, **[P]** paraphrase. Bonzz,
EQ Resource, Fanra and the patch notes were read raw. Coordinates are **/loc (Y, X)** unless marked world (x, y).

---

## A. Item-id correction for the whole 2005 set (important)

EQQuests labels several 2005 ids as "live item ids", but they are **Allakhazam's internal ids**. The live ids (EQ
Resource, which uses live ids, and the peq live import agree):

| Item | EQQuests / Allakhazam id | **Live id** | Live flags (EQ Resource) |
| --- | --- | --- | --- |
| Bristlebane's Ticket of Admission | 45441 | **85062** | Magic, No Trade, Quest; TINY; stack 20; lore "Good for one showing" |
| Bone Mask of Horror | 45517 | **90040** | Magic, Lore, No Trade; Face; Rec 70, **Req 60**; AC 15, HP/Mana/End 135, STR 15, STA 10, INT 15, WIS 15, AGI 5, DEX 5, SvMagic 15, SvFire 5, SvCold 5, SvDisease 10, SvPoison 5; Illusion: Frost Bone, cast 5 s; lore "A bone mask that will scare the fearless" |
| Solid / Calcified / Strengthened / Hardened / Cracked Bone Mask of Horror | 45522 / 45518 / 45523 / 45521 / 45519 | **90041 / 90042 / 90043 / 90044 / 90045** | peq: Req 50 / 40 / 30 / 20 / 10, Rec 60 / 50 / 40 / 30 / 20 |
| Dusty Bone Mask of Horror | 45520 | **90046** | Rec 10, no Req; AC 5, HP/Mana/End 15 |
| Spell: Illusion: Frost Bone | 61079 | **90047** | Magic, No Trade; Enchanter; races Dark Elf, Drakkin, Erudite, Gnome, High Elf, Human |
| Shield of the Void | 46176 | **90033** | Magic, Lore, No Trade, Placeable; Secondary, "Type 20 (Weapon Ornamentation)"; AC 30, HP/Mana/End 130, STR 12, STA 5, INT 12, WIS 12, AGI 10, DEX 10, SvMagic 20, SvFire 10, SvCold 10; lore "From another time and place" |
| Shield of the Void [artifact] | 46195 | **36116** | Magic, Lore, No Trade, Artifact, Quest; same stat block; "Item details show the highest potential item level. Actual statistics may vary based on the level of your main character." |
| Lesser Shield of the Void | 46174 | **90034** | AC 20, HP/Mana/End 100, STR 10, STA 4, INT 10, WIS 10, AGI 8, DEX 8, SvMagic 15, SvFire/Cold 10 |
| Chipped Shield of the Void | 63750 | **90035** | AC 15, 75/75/75, STR 8, STA 4, INT 8, WIS 8, AGI 6, DEX 6, SvMagic 10, SvFire/Cold 10 |
| Cracked Shield of the Void | 63751 | **90036** | AC 12, 40/40/40, STR 7, STA 4, INT 7, WIS 7, AGI 5, DEX 5, SvMagic 9, SvFire/Cold 8 |
| Split Shield of the Void | 63754 | **90037** | AC 8, 30/30/30, STR 6, STA 4, INT 6, WIS 6, AGI 5, DEX 5, SvMagic 8, SvFire/Cold 6 |
| Fractured Shield of the Void | 63752 | **90038** | AC 6, 25/25/25, STR 5, STA 2, INT 5, WIS 5, AGI 4, DEX 4, SvMagic 7, SvFire/Cold 4 |
| Splintered Shield of the Void | 58571 | **90039** | AC 5, 15/15/15, STR 4, STA 1, INT 4, WIS 4, AGI 2, DEX 2, SvMagic 6, SvFire/Cold 2 |
| Caramel-Coated Candy Apple | 45453 | **85064** | see Trick or Treat rewards |
| Delicious Pumpkin Bread | 45454 | **85068** | |
| Sweetened Gummy Bears | 45482 | **85065** | |
| Tasty Sugar Pop | 45481 | **85063** | |

All shields: Magic, Lore, No Trade, Secondary, TINY, WT 1.0, IT212, aug slot type 7. Only the full Shield of the Void
(90033) is Placeable. None has a required level on EQ Resource or in peq.

---

## B. Trick or Treat for the Old Man (Allakhazam 3254): additions

### Header extras (Allakhazam [V])
Level 10-90, repeatable, solo, quest page added **Oct 30, 2005**. ProjectEQ runs it as a task with its own custom id
**500220** (steps = the ten codex clues, then "Full Trick-or-Treat Bag", then Old Man Draykey); live's task id is unknown.

### NPC levels and spots (Bonzz levels; ClericRachael Oct 25 2022 waypoints [V] are /loc Y, X)
| NPC | Zone | Bonzz level | Waypoint (ClericRachael 2022) | Bonzz note |
| --- | --- | --- | --- | --- |
| Old Man Draykey | Kithicor Forest | 70 | 1915, 4535 | "northwest corner area"; Fanra: "Kithicor, North of HHP zone" |
| Grand Librarian Maelin | Plane of Knowledge | 75 | 0, 914, 4 | top of the Library |
| Sergeant Ragus | The Commonlands | 25 | between 188, -2726, 11 and 65, -1940, 40 | "wanders along the main path, in the area of what used to be **East Commonlands**" |
| Wraps McGee | Befallen | 28 | -555, -174, -57 | "near the locked door to the final area"; Bonzz tricks: illusion as wolf/gnome and target through the door from the well side, or pick the lock (shroud/persona rogue). OzadarZek 2022: "Just stand at the door: 1. /target Wraps McGee 2. /say trick or treat 3. ding . . . candy." |
| Crabby the Rotten | Estate of Unrest | 50 | 355.1, 33.27, 6.33 and 385, 126, 5 | "randomly spawns in either of the hedge mazes" |
| Nate | Castle Mistmoore | 25 | -36, 430, -233 | "in the graveyard" |
| Immug Lashtail | Field of Bone | 50 | -253, 1248, -64 | wanders the pit ("arena") |
| Fuzz Selppa (Bonzz "Fuzz Selpa") | Toxxulia Forest | 50 | -333, 1172, 46 | "on the far west wall, by the beach, near where the Kerra Isle zone used to be" |
| Scary Miller | West Karana | 50 | -3550, -4843, 2 | the Miller farm |
| Poil Lolp | Netherbian Lair | 25 | 784, -778 and 385, -482, -8 | "random locations throughout the left side caves" |
| Nilham the Chef | Iceclad Ocean | 26 | 4550, 1369, 77 | "an igloo at the 'pirate' camp" |

This answers inventory.md's open question: Sergeant Ragus patrolled **East Commonlands** (Bonzz). ProjectEQ has a
Ragus script in both `commonlands` and `ecommons`.

Note: the 2022 waypoints may be in rebuilt zones (Toxxulia, Commonlands, Befallen and Unrest were not all classic in
2022). UNCONFIRMED per zone.

### Treat-line correction (MikuRBD, Oct 8 2012 [V])
"His text is not displayed properly here. When he hands you candy he actually says: 'Here you go. Be careful not to make
yourself sick.' The line that is currently attributed to him: 'Hah! Here's the tastiest treat of them all! Enjoy!' Is
actually the line that ANY of the 10 npcs will say if they 'trick' you (hand you lint instead of candy)."
- So **Sergeant Ragus's treat line** is `Here you go. Be careful not to make yourself sick.` and the **shared "trick"
  line** is `Hah! Here's the tastiest treat of them all! Enjoy!` EQQuests 01-ruins-of-kunark.md:12472 (and ProjectEQ's
  Ragus script) use the trick line as Ragus's treat line.
- Retry after a trick: zone out and back (MikuRBD: "you only must leave the zone and return"), or camp to character select
  and back (dargot 2018: "If you camp to character select and come back, you can ask for another trick or treat."). Atlans
  2014 first thought waiting 5 minutes worked, then corrected himself (he had left the zone).
- Lost candy: missjackie 2010 "I checked every bag and no candy."; warvok 2011: "Only thing i can think is the toon was out
  of food and ate the candy." (the treats are edible snacks).

### Trick items (Bonzz: "Chunk of Coal ..., Broken Twig ..., Pocket Lint ... or Sand"; EQ Resource)
| Item | Live id | Flags |
| --- | --- | --- |
| Sand | **84091** | No Trade, TINY, lore "Definitely not a treat" |
| Chunk of Coal | **84092** | No Trade, TINY, lore "Definitely not a treat" |
| Pocket Lint | **84093** | No Trade, TINY, lore "Definitely not a treat" |
| Broken Twig | not found (no EQ Resource / peq match) | Bonzz only; UNCONFIRMED |

### Treats (live ids, EQ Resource)
| Treat (giver) | Live id | Flags |
| --- | --- | --- |
| Lollipop (Poil Lolp) | **84082** | Magic, Lore, No Trade, snack (4), lore "A tasty treat" |
| Fairy Fizzles (Nate) | **84083** | Magic, Lore, No Trade, lore "Sweet and tangy" |
| Gummie Kobolds (Immug Lashtail) | **84084** | Magic, Lore, No Trade, lore "Better than Gummie Goblins" |
| Candy Jack-o-Lantern (Crabby) | **84085** | Magic, Lore, No Trade, lore "Contains red 5" |
| Caramel Apples (Fuzz Selppa; EQQuests spells it "Carmel Apples") | **84086** | Magic, Lore, No Trade, lore "A rare treat" |
| Jawbreaker (Maelin) | **84087** | Magic, No Trade, lore "Rock solid" |
| Rock Candy (Ragus) | **84088** | Magic, No Trade, lore "Large sugar crystals" |
| Chocolate Coin (Nilham) | **84089** | Magic, No Trade, lore "Hidden beneath a golden shell" |
| Candy Corn (Scary Miller) | **84090** (peq) | peq: Lore, magic, no stats. Not the 2006 Monster Mash Candy Corn 87317 |
| Tasty Candy (Wraps McGee) | UNCONFIRMED: only Tasty Candy **6800** found (Magic, tradeable, stack 20), an older general item | |

Bag and book: **Trick-or-Treat Bag 84095** (Lore, No Trade, 10 slots, GIANT capacity, WT 10.0), **Draykey's Codex 84094**
(Lore, SMALL, WT 0.5), **Full Trick-or-Treat Bag 84096** (Lore, No Trade, Quest, LARGE, WT 10.0, lore "A bag full of
candy"). Bonzz: "Be sure you have a bag slot open!"; the bag has "0% Weight Reduction".

### Reward by level
Bonzz: "He will give you a stack of five (5) stat food items. These items can vary by your level, the best of which is the
Caramel-Coated Candy Apples". Allakhazam's reward list = Ticket + Caramel-Coated Candy Apple, Delicious Pumpkin Bread,
Sweetened Gummy Bears, Tasty Sugar Pop (the Frost Bone spell link on that page belongs to Out With the Old). Live stats:
| Snack | Live id | Stats (Magic, No Trade, snack (5), stack 20) |
| --- | --- | --- |
| Caramel-Coated Candy Apple | 85064 | HP/Mana/End 35, STR 10, STA 5, INT 10, WIS 10, DEX 5, SvMagic 5 |
| Sweetened Gummy Bears | 85065 | Mana 40, End 40, STR 10, STA 5, INT 10, WIS 10, AGI 5 |
| Delicious Pumpkin Bread | 85068 | Mana 30, End 30, STR 8, STA 5, INT 8, WIS 8, AGI 5 |
| Tasty Sugar Pop | 85063 | HP 40, STR 25, STA 25 (as listed) |
Which snack belongs to which level band: UNCONFIRMED.

### Placement conflict (ProjectEQ vs live)
peq spawns Old Man Draykey (npc 20279, race 12 gnome, level 70) at kithicor world x=-777, y=1845 = /loc (1845, -777),
the far Commonlands side. Live is /loc (1915, 4535) near the High Hold Pass line (peq HHP zone line x=4890, y=560).

---

## C. The Hungry Halfling (Allakhazam 4665): additions

- Mippie Diggs: Bonzz level **70**; live /loc (1950, 3800) near the Rivervale line. peq npc 20275 (race 11 halfling,
  female, level 65) at world x=3796, y=1939 (matches). ProjectEQ script `kithicor/Mippie_Diggs.pl` shouts every 10 min:
  `Trick or treat! Smell my feet! Give me something good to eat!` (ProjectEQ text; live UNCONFIRMED).
- Task steps (live text) are not published. peq task **8013**: four optional-style "loot" activities (Pumpkin Pie 36110,
  Pumpkin Bread 36112, Spiced Pumpkin Cider 36113, Pumpkin Shake 36114) then "speak with Mippie Diggs"; its description
  text has "What a tradeskiller you must be! Why don't you go back and speak with Mippie Diggs?" for the last step.
  peq omits Baked Pumpkin Seeds, but live accepts them: LifegiverOfXegony, Nov 1 2011 [V]: "I just completed this quest
  again during Halloween 2011 by doing 5 of the Baked Pumpkin Seeds and ignoring everything else, so I can confirm that
  this method does still work." Stageguy 2017 [P]: Ice of Velious optional; duplicates accepted; keep other food in
  inventory first so you do not eat the turn-ins.
- Turn-in line (Allakhazam [V]): `My, my, this looks good! Thank you!`
- Bonzz's pick: Pumpkin Bread (only 1 Pumpkin Flesh each, Baking 102) - "the other recipes will require at least ten (10)
  drops, where this only requires five (5)". Pumpkin Flesh "can drop off of "scarecrow" type MOB's in the Estate of
  Unrest". Egg Batter = "most any egg type and a Bottle of Milk in a Mixing Bowl"; Bread Tin is player-crafted.
- Live ingredient / food ids (EQ Resource; all tradeable):
  Pumpkin Pie Spice 36106, Handful of Pumpkin Seeds 36107, Pumpkin Cider Spice 36108 (lore "Pumpkin Ale Spice"), Pumpkin
  Flesh 36109 (TINY, 0.1), Pumpkin Pie 36110 (meal 10, MEDIUM 1.5), Baked Pumpkin Seeds 36111 (snack 5), Pumpkin Bread
  36112 (meal 10, MEDIUM 1.5), Spiced Pumpkin Cider 36113 (drink 5), Pumpkin Shake 36114 (drink 5). All Magic, stack 20.
  Book: Mippie's Home Remedies **84097** (Lore, SMALL, 0.5, lore "Full of pumpkin treats").
- Reward: Ticket **85062** + one random 5-dose race illusion. Live ids for the 0.4-weight set (Bonzz: "5 Dose Essence of
  Troll (Weight 0.4)"): Dark Elf 65086, Ogre 65087, Troll 65088, Iksar 65089, Wood Elf 65090, Half Elf 65091, High Elf
  65092, Human 65093, Barbarian 65094, Erudite 65095, Halfling 65096, Gnome 65097, Dwarf 65098, Vah Shir 65099 (EQ Resource
  65088: tradeable, SMALL, 0.4, tribute 300, illusion cast 10 s, 5 charges). Allakhazam also lists Drakkin and Gukta;
  their live ids in this set are UNCONFIRMED (51142 "5 Dose Essence of Gukta" exists but is a different item: 0.1 weight,
  6 s cast). Fanra (old wiki) gives "5 Dose Essence of Dark Elf" as its example. ProjectEQ always gives Halfling (65096)
  and sets qglobal `halloween_hungry` for 30 days.

---

## D. Out With the Old (Allakhazam 5370): additions

### Header (Allakhazam [V])
Level 20-125, repeatable, **success lockout 6:00:00**, group 3-6, monster mission. Quest page added Oct 25, 2011. Zone
page: "Nights of the Dead: Kithicor Forest: Out With the Old" (Allakhazam zone 803): "This is the instanced zone involving
the Halloween group monster mission 'Out With the Old' in which you take part in a battle between the gods and the
would-be gods of the void." Outdoor, instanced, not keyed, level range 20-130.

### NPCs at the start
- **Cathil** (Allakhazam npc 38045): level 35; "+1240, +1065 outside a cabin in the north-central part of Kithicor"
  (ddmurray 2019: "1230, 1060"; Bonzz /waypoint 1228, 1068). Look (screenshot, my read): **Human male**, grey-blond hair,
  long **yellow robe** with brown trim. Screenshot https://zam.zamimg.com/images/1/5/15004a2841008f4dff15abc2489b7cf8.jpg
- **a silly puppet** ("Wenan"): Bonzz level 25. Look (same screenshot): a small **halfling-sized male** figure, dark hair,
  brown vest, bare feet. Exact race UNCONFIRMED.
- Neither is in peq.

### Full dialogue (Allakhazam [V]; EQQuests only has the opening lines)
```
You say, 'Hail, a silly puppet'
a silly puppet says 'Whadda ya want? Can't ya see I'm busy here? Do you think that I just 'hang' around here all day? Hahah, get it? I'm on strings! Bah, you bore me. Go bug the dummy here before I get mad.'
You say, 'Hail, Cathil'
Cathil says 'Why hello there! It seems that we are not alone in our curiosity of these woods. Let me introduce myself, I am Cathil and this here is Wenan. Say 'Hello', Wenan.'
a silly puppet says 'Hello Wenan! Snark! Snark! Snark!'
Cathil says 'You'll have to forgive Wenan here, it has been a long journey for the two of us for you see, for we are [wandering story tellers].'
You say, 'Wandering story tellers?'
Cathil says 'Yes indeed. You see we earn our keep traveling from town to town entertaining all who would listen to the tales of fancy our imaginations can dream up! Why in fact, I bet Wenan here might have a [tale] or two for you now, if you ask him nicely enough!'
You say, 'What tale?'
a silly puppet says 'Tale? Who told you anything about a tale? Well I might have a small story for you if you have something for me. That's right, I gotta eat too, you know. Life isn't all roses and honey for me, bub. So cough up the prize or get lost cuz you're blocking my view.'
(give the puppet a Bristlebane's Ticket of Admission)
a silly puppet says 'Oh. . .ok then. . .I got a [story] for you alright but don't think of this as a history lesson. Naw, this is just something I came up with to entertain wee brains like Cathil here. I'll speak slowly so try to keep up!'
You have been assigned the task 'Out With the Old'.
You say, 'What's your story?'
a silly puppet says 'Sit back and relax as I spin you a yarn about the early days of the universe; when the newly borne stars burned their brightest. Before there was much of anything, [they] strode the lands.'
You say, 'Who is 'they'?'
a silly puppet says 'Their names lost in antiquity, they were from the void. They are the ones that came before. . .before the others whom we now call the gods. For you see, it was they who actually created all that you see before you. . . the sky, the stars, the land, and yes, even the [gods] themselves!'
You say, 'Gods?'
a silly puppet says 'Some say they created the gods to be their servants. Others say it was naught but folly and pride that led them to create such powerful beings. . .beings that would eventually challenge they-of-the-void, for [supremacy] of all reality.'
You say, 'Supremacy?'
a silly puppet says 'Not content to be mere underlings, the gods-of-today conspired to defeat the old ones. In secrecy did the plan form and in fire did it end. For the gods-of-today would not be stopped till each and every one of the void was sent back to it. Yet during the eons long war it seemed as if the new gods had underestimated the power and tenacity of those of the void. Till one fateful battle occurred, just beyond the hills behind us; a battle that would tip the favor of the war towards the gods of today. Why I bet if you close you eyes and quiet your mind, you can [imagine] the terrible battle that must have occured. . .'
You say, 'I can imagine...'
You close your eyes and relax your mind. . .the sounds of battle begin to slowly approach you
```
(Live typos kept: "newly borne", "close you eyes", "occured".) Bonzz: pick templates, then say "Story" and follow along;
the key phrase is "Imagine"; you are moved into the instance.

### Templates (Allakhazam, Bonzz)
Terris Thule (Enchanter), Tunare (Druid), Cazic Thule (Shadow Knight), Rallos Zek (Warrior), Erollisi Marr (Cleric),
Bertoxxulous (Necromancer). Template spell/ability lists: not published anywhere I found (UNCONFIRMED).

### The fight
- Bonzz: "Run over to the entrance to Rivervale, but don't zone! The job here is to protect Rivervale and beat three (3)
  waves ... Each Wave will have higher con MOB than the previous ones, of about 15 MOB's each. The last wave has the named
  MOB, The Legion Commander of the Void. Kill it first."
- Timing (Allakhazam [P]): about 6 minutes from zone-in to the first wave; over 4 minutes between waves 1 and 2; at least
  7 minutes before the final wave engages.
- Wave emotes (Allakhazam [V]):
  - `From deep within the shrouded woods, you can hear the sounds of an army approaching. . .`
  - `The din of their marching echoes through the fog. . .you can now feel the ground rumble as they stride towards you. . .`
  - `The army steps forth from the swirling mist. . .their eyes glowing with the same unholy power that animates them.`
  - `The final army settles into place. . . preparing to charge you at any moment!`
  - Mob shouts quoted on Allakhazam [P/partial]: "The void shall claim you and your kind." (wave 1), "The void hungers for
    you!" (wave 2), "Fools! We, the true gods of this universe, shall not succumb..." (final wave; rest of the line
    UNCONFIRMED).
- Mobs (Allakhazam zone 803; levels as recorded, probably one group-level version):
  | Mob | Allakhazam id | Level | Wave |
  | --- | --- | --- | --- |
  | a lost creature of the void | 38047 | 25 | 1 (x16 with a fragment of spite) |
  | a fragment of spite | 38046 | 40 | 1 leader |
  | a figment of malice | 38049 | 30 | 2 (x12) |
  | a shard of hate | 38048 | 43 | 2 leader |
  | a creature of despair | 38053 | 35 | 3a (x9) |
  | a shard of nothingness | 38052 | 40 | 3a leader |
  | a fragment of malice | (not on the zone list) | ? | 3b (x9) |
  | a sliver of despondency | 38054 | 40 | 3b leader |
  | a wandering soul of the void | 38051 | 25 | 3c (x9) |
  | The Legion Commander of the Void | 38050 | 45 | 3c boss |
  | a fragment of bleakness | 38055 | 35 | listed on the zone page, not in any wave write-up |
- Deaths: "You can die as much as you'd like, unless all the players are dead at the same time." (Oct 26 2012 [V]).
- Mercenaries: allowed; they leave when upkeep runs out while you are in a template; Bayle Marks keep them up past the
  15-minute timer (Wreck 2015, Cylius 2015, markkuss 2016, Rysho 2020 [P]). Smallest reported win: 3 players, no mercs, as
  Rallos, Cazic and Erollisi Marr (Auurbornne 2022 [V]). Wreck's advice: "have at least two healers".

### Reward
- A chest spawns after the Legion Commander dies. "Loot the sh[ield] from the chest that spawns and you'll be booted from
  the zone within two minutes." [P]. Sythik 2016 [V]: "The second task step is to: claim your reward. This step is
  completed by looting the Shield of the Void." Wreck 2015 [V]: "It appears that the shield MUST be looted."
- Bonzz: "The named drops a loot item, in the form of an Artifact, which will transform into a loot item for the player
  who loots it, once they zone out." That artifact is **Shield of the Void 36116** ("Actual statistics may vary based on
  the level of your main character"); it becomes one of the seven tiers (90033-90039, table in section A).
- Tier by level: Merf, Oct 26 2011 [P]: at level 54 he got **Lesser Shield of the Void** (AC 20, STR +10). If the tiers
  follow the Bone Mask bands (under 10, 10-19, ..., 60+), the order would be Splintered < Fractured < Split < Cracked <
  Chipped < Lesser < Shield. That band mapping is an **inference**, UNCONFIRMED.
- The Allakhazam reward list also links **Spell: Illusion: Frost Bone** (live 90047, Enchanter scroll). How it is awarded
  (chest? enchanters only?) is UNCONFIRMED.
- Credit history (patch Nov 1, 2005): "Corrected an issue with character flagging in the Halloween events. Previously only
  the Trick-or-Treat event and the "Out with the Old" mission were giving credit for completion." and "Due to the issues in
  the Halloween events the time they will be available has been increased. The events will now remain available until the
  morning of Monday, November 14th." Same patch: "The weight on all versions of the Mask of Horror for the Halloween event
  has been decreased."

---

## E. "The Rat Bounty" / #Roosevelt (PoK): ProjectEQ custom, no live source

Searched again (Allakhazam, Bonzz, Fanra, EQ Resource NotD page, everquest.com news 2008/2010, patch notes 2005-2022,
web search for "Roosevelt" / "Icarus" / "Norvegicus" / rat names). **No live EverQuest source mentions it.** It is a
ProjectEQ server event:
- `poknowledge/#Roosevelt.pl` in ProjectEQ's quest repo: "Greetings! I am the eldest member of the Rattus faction
  Norvegicus. Standing next to me is our youngest member my apprentice Icarus. Once a year, the three clans get together to
  test their survival skills. For the first time ever, outsiders have been invitied to join in the [hunt]!" It hands out
  item 111901 "Wand of Metacrystalline Teleportation" as a tracker, offers "[PVP on]" / "[PVP off]", and assigns custom
  task **500222** ("Locate Kai", Brutus, Aristotle, Zeus, report to Roosevelt, Sherlock, Ocho, Toby, report, Gustave,
  Napoleon, Sprocket, Mortimer, Paulie, report) plus custom task 500219 "Happy Halloween!".
- The rats (`global/#Kai.pl`, `#Brutus.pl`, ... `#Paulie.pl`, `halloween_event/#Paulie_.pl` etc.) hide in random zones via
  plugins (`plugin::GetRandomIndoorLocation`, `plugin::GetRatLocation`), with PvP rewards (item 124688 "Peace Be With
  You") and qglobals `halloween_ratter_*`. Task ids 5000xx are ProjectEQ's custom range. `halloween_event/README.md`
  enables it with the content flag `peq_halloween`.
- Conclusion: **not live content; no live name found.** Treat it as a ProjectEQ invention.

---

## Sources
- Allakhazam: https://everquest.allakhazam.com/db/quest.html?quest=3254 , ?quest=4665 , ?quest=5370 , ?quest=5371 ;
  zone https://everquest.allakhazam.com/db/zones.html?zstrat=803 ; npc https://everquest.allakhazam.com/db/npc.html?id=38045
- Bonzz: https://www.bonzz.com/bonemask.htm (full 2005 walkthrough, NPC levels) and https://www.bonzz.com/nightsofthedead.htm
- EQ Resource live items: https://items.eqresource.com/items.php?id= 85062, 84082-84089, 84091-84097, 85063-85065, 85068,
  90033-90040, 90046, 90047, 36116, 36106-36114, 65088, 65096, 51142, 6800
- Fanra wiki: https://fanra.fandom.com/wiki/Halloween
- Official news: https://www.everquest.com/news/imported-eq-enus-51169 and -52055 (2005 set listed as "Trick or Treat?")
- Patch notes Nov 1, 2005: https://github.com/nazwadi/patcheq (local `scratchpad\notd\raw\patches\p-2005-2.txt:940-1013`)
- ProjectEQ quests (clone 2124cc0): kithicor/Mippie_Diggs.pl, kithicor/Old_Man_Draykey.pl, commonlands/Sergeant_Ragus.pl,
  poknowledge/#Roosevelt.pl, global/#Kai.pl .. #Paulie.pl, global/items/script_13493.pl, halloween_event/README.md;
  local peq dump (items, npc_types, spawn2, tasks, task_activities)
- Screenshot: https://zam.zamimg.com/images/1/5/15004a2841008f4dff15abc2489b7cf8.jpg (Cathil + puppet)
