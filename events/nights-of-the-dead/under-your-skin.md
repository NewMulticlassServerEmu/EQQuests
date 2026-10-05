# Nights of the Dead 2010: Under Your Skin (Allakhazam quest 5373)

Gathered 2026-10-05. Read-only web research plus read-only reads of the local peq dump. Nothing under C:\Git\test was
changed. **Out of our era**: the mission zone is Snarlstone Dens (DoD, peq `eastkorlacha` 363) and the level is 85+.
Documented in full anyway so we have it later. The flagging task, Terror of Illis Taberish, is in `2009-2010-quests.md`.

## 0. Read this first
- Quote tags: **[V+]** two sources agree, **[V]** one verbatim-style WebFetch transcript of Allakhazam (Allakhazam blocks
  curl), **[P]** paraphrase by the fetch model. Fanra's wiki, EQ Resource, Bonzz and everquest.com were read raw (exact).
- Coordinates: Allakhazam and Bonzz numbers are **/loc order (Y, X)**.
- Item ids: live ids from EQ Resource; peq has the same rows.

## 1. Year: 2010 (Allakhazam's "Underfoot / 2011" label is the page date)
- Official news **Oct 22, 2010**, "The Haunting of Norrath!" (Oct 24 - Nov 7, 2010), under "Fresh Hauntings!", exact text:
  > **Under Your Skin** Illis Taberish is in despair. He is convinced that something terrible is going to happen. And with
  > the Hallowed Eve coming, he is certain that whatever it is, will happen soon. His dreams are becoming more and more
  > vivid. He sees vile creatures attacking innocent people across the lands and taking their souls. All of this seems to
  > have started when he found the Scroll of the Skinwalker within the property left to him by his recently departed
  > uncle.
  >
  > Illis needs you to destroy the Skinwalker that has taken over Longshadow's den before he gains enough souls to become
  > more powerful by All Hollows Eve!
  >
  > The Skinwalker is a shape shifter who needs his victims to be in complete fear before he traps their souls and feasts
  > on their flesh. You will need to track down this creature and kill it in every form it takes, while also collecting
  > parts of his soul.
  (The article files both 2010 tasks under the single heading "Under Your Skin"; "collecting parts of his soul" is the
  Terror of Illis Taberish half.)
- Allakhazam: Rhaeda Evel NPC added **Oct 21, 2010**; the oldest comments on her page are Oct 25 - Nov 4, 2010. The quest
  page itself was added Oct 26, 2011, hence its "Era: Underfoot".
- Fanra wiki: "a group instanced mission first introduced at Halloween 2010".
- Patch notes Nov 2010 (Previously Updated): "Corrected problems with the Halloween quests involving the Plane of
  Knowledge." and "All task NPCs for Halloween 2010 quest "Terror of Illis Taberish" should now repop after 7.5 minutes".
- Fanra: because of bugs SOE re-ran the 2010 Haunting of Norrath Nov 22 - Nov 30, 2010 ("Haunting of Norrath Halloween
  Events Returning 11/22 - 11/30").

## 2. Header (Allakhazam [V])
- Level **85**, max 125. **Group task, 3-6 players.** Repeatable. **Lockout 17 hours 30 minutes.** Allakhazam marks the
  write-up "Incomplete".
- Average-level gate: DemoriaDereneau, Oct 25 2010 [P]: "Have group of 85 and 86 level players...says my average level is
  too low??" The real minimum average level is UNCONFIRMED (85 per the header, but this report suggests higher).
- Prerequisite: any version of **Nights of the Dead: Terror of Illis Taberish** (Allakhazam 5372). Oct 30 2010 [P]: "It
  appears you have to be flagged for the mission". Nov 2 2010 [P]: "I did the mission for the guy right beside him...Tried
  talking to the werewolf after that and nadda" (later fixed). Allakhazam summary [P]: the flag may need a zone reset to be
  recognised. Fanra: "It is necessary to do the Terror of Illis Taberish mission to request Under Your Skin."
- Achievement: **Nights of the Dead: Altered Beasts** (Allakhazam 8836): "This Halloween achievement is gained upon
  completion of the following tasks and mission" = any one of the nine Terror of Illis Taberish versions (6, 16, 26, 36,
  46, 56, 66, 76, 81+) **and** Under Your Skin "from Rhaeda Eveil" [sic] in the Plane of Knowledge.

## 3. Giver: Rhaeda Evel (Allakhazam npc 36168)
- Plane of Knowledge, **/loc +300, +322** "by a tree near the main bank"; Bonzz "a werewolf by a tree near the main (big)
  bank ( /waypoint 300, 325 )". She stands beside Illis Taberish (Bonzz /waypoint 285, 330). Findable with Ctrl-F.
- Level 80 (Allakhazam). Look (screenshot, my read): a **white werewolf** (the newer werewolf model, standing upright,
  white fur, black claws). Suffix "(Nights of the Dead Mission)". She jokes about her "costume". Screenshot
  https://zam.zamimg.com/images/1/d/1d7d30fde484b9995baa4790199374cd.jpg
- Not in peq (no npc_types row for Rhaeda, Skinwalker or Revealed Skinwalker).

## 4. Dialogue (Allakhazam [V])
```
You say, 'Hail, Rhaeda Evel'
Rhaeda Evel says 'You like my costume?! I did it myself! Okay, okay... I suppose Illis has told you about that nasty [Skinwalker]! You wouldn't be talking to me if he had not! Am I right?! Am I right?! HA!'
You say, 'Yes, he told me about the Skinwalker'
Rhaeda Evel says 'Well okay, let us get on with it. It seems that this Skinwalker has holed up in [snarlstone] den. You will need to go there to kill him, or it, whatever that thing is.'
You say, 'Snarlstone?'
Rhaeda Evel says 'As you can imagine, there are many dangers there normally. I would imagine that the ragepaws and drachnids that live there have been corrupted already. This means they will be even more dangerous! Are you [willing] to take this on?'
You say, 'Of course I'm willing!'
Rhaeda Evel says 'Amazing! I am dumbfounded that you are prepared to put your own life in danger to help someone else! But no guts, no glory I always say! Am I right?! Am I right?! Of course I am right! Let me know when you are [ready] and I will send you to the den directly!'
You have been assigned the task 'Under Your Skin'.
You say, 'Ready!'
Rhaeda Evel says 'Good luck and hold on tight!'
```
- Bonzz shortcut: "Willing" gets the mission; "/say Ready to Rhaeda Evel, to zone into the instance".
- Leaving and re-entering (Fanra): "Tell Rhaeda Evel "ready" to zone into instance. You can leave mission any time by
  clicking on the door next to where you zone in and you will return to Plane of Knowledge. Tell her "ready" again to
  return."

In the den [V]:
```
You say, 'Hail, Skinwalker'
Skinwalker says 'Another soul for the taking? It is so much easier when they come to me!'
```
After the real Skinwalker dies [V]:
```
You killed the Skinwalker! Only Longshadow is strong enough to break the hold of the Skinwalker's corruption and return to normal now that he is dead!
You say, 'Hail, Elder Ritualist Longshadow'
Elder Ritualist Longshadow says 'I do not know who you are, but I am in your debt. I will send you back to where you came when you are [ready].'
Your task 'Under Your Skin' has been updated.
```
Then "/say ready" to Longshadow to leave the instance (Allakhazam: target Longshadow and "/say ready to leave instance").

## 5. Task steps (Allakhazam [V] for 1-2; 3-4 are the walkthrough's wording, exact step text UNCONFIRMED)
1. `Find and speak to the Skinwalker 0/1 (Snarlstone Dens)` (walkthrough: "Find and speak to the Skinwalker somewhere in
   the den.")
2. `Kill the real Revealed Skinwalker 0/1 (Snarlstone Dens)`; task window note: "You must figure out which Skinwalker is
   the true Skinwalker and kill him."
3. Hail Elder Ritualist Longshadow.
4. (Leave) target Longshadow and say "ready".

## 6. The instance: "Snarlstone Dens: Under Your Skin" (Allakhazam zone 804)
- Allakhazam zone text: "This is the instanced zone involving the Halloween group task 'Under Your Skin' in which you're
  sent to kill the Skinwalker who's taken up residence in Longshadow's den." Indoor, instanced, not keyed, level range
  85-90, DoD.
- Route: "The Skinwalker is found at the throne in the main room of the zone (northwestern part of the map where Bloodeye
  spawns in her instances)." Fanra: "You must go to the north west most room in the zone. You can either kill your way
  there or run and feign death (if your class allows)." Trash is densely packed and "most see invis" (Allakhazam [P]),
  mezzable/stunnable [P]. 2022 (OldKnight [P]): mobs spawn inside walls and train.
- **Door bug (2013)**: lovguild, Wreck, dragonarc (Oct 2013 [P]): the north-west door would not open after clearing; Wreck
  got past by shrinking and squeezing along the edge; dragonarc pulled mobs from behind it. Diani (Oct 2014 [P]): no door
  problem in 2014.
- Corrupted Longshadow (Allakhazam npc 38074): level 85, a **black werewolf**, suffix "(Corrupted Soul)" (screenshot
  https://zam.zamimg.com/images/0/d/0dd8d7c3e18273fa3dcc5d1e89a7a245.jpg). Fanra's hint about "the non-attack-able
  werewolf on the stage" probably means him (inference).

### NPCs in the instance (Allakhazam zone 804)
| NPC | Allakhazam id | Level | Notes |
| --- | --- | --- | --- |
| a Drach cursewielder | 38076 | 83-85 | |
| a Drach defiler | 38069 | 83-85 | |
| a Drach flamespinner | 38077 | 83-85 | |
| a Drach guardian | 38071 | 84-86 | listed as the Stout Mottled Mask dropper |
| a Drach invader | 38064 | 83-85 | |
| a Drach looter | 38063 | 83-85 | |
| a Drach mindcatcher | 38072 | 83-85 | |
| a Drach mundunugu | 38075 | 83-85 | |
| a drachind webmender | 38073 | 83-85 | (sic "drachind") |
| a frenzied Ragepaw | 38065 | 83-85 | |
| a Ragepaw earthcaller | 38067 | 83-85 | |
| a Ragepaw hunter | 38068 | 83-85 | |
| a Ragepaw spiritist | 38066 | 83-85 | |
| a Ragepaw warrior | 38070 | 83-85 | |
| Corrupted Longshadow | 38074 | 85 | black werewolf, "(Corrupted Soul)" |
| Skinwalker | 38061 | 88 | quest NPC at the throne |
| Revealed Skinwalker | 38062 | 89 | three spawn on hail |
| Elder Ritualist Longshadow | (no page found) | ? | spawns where the real Skinwalker dies (Allakhazam) / "by the throne" (Bonzz) |

Comment damage numbers [P]: werewolves max hit about 1,700; drachnids up to 2,300 (Nov 4 2010: "drachnids/shadowmanes");
fake Revealed Skinwalkers about 5,000; the real one about 7,000.

### The Skinwalker fight
- **Skinwalker** (npc 38061): level 88. Look (screenshot, my read): a small **blue winged imp/mephit**; Bonzz calls it "a
  mephit". Screenshot https://zam.zamimg.com/images/4/a/4a1a597af060a61082cea27fd3dc0544.jpg
- Hail it: it **despawns** and **three identical "Revealed Skinwalker"** (level 89) spawn (Fanra; Allakhazam: "Three KOS
  mobs (which don't see invis) called 'Revealed Skinwalker' spawn.").
- Kill a fake one: **two more Revealed Skinwalkers spawn** where it died (Fanra, Allakhazam, Bonzz, the zone comment).
- Kill the real one: "the other mobs will despawn. Elder Longshadow will spawn." (Fanra).
- Telling them apart:
  - Bonzz: the real one "hits for as much as 2K more than the other two". Strategy: if you kill the wrong one, focus the
    remaining two originals while controlling the new adds; if wrong again, the last original "has to be the right one".
  - Allakhazam [P]: "the extended target window, it is easy to figure out which is the one" (health bars / damage).
  - reverent, Oct 2011 [P]: have the group watch which one deals the most damage.
  - Fanra: "Either the real one is decided at random, or it is the one standing closest to the non-attack-able werewolf on
    the stage." UNCONFIRMED.
- Crowd control: Nov 4 2010 [P]: the Revealed Skinwalkers "cannot be snared, rooted, or mezzed"; reverent 2011 [P]: they
  cannot be mezzed and hit harder than trash. Diani 2014 [P]: they are **not** aggro-linked (you can pull one).
- Tuning reports: a 3-box (90 SK, Enc, Shaman + healer and two DPS mercs) finished it in 2011 (reverent [P]). OldKnight
  2022 [P] calls the Skinwalker a large difficulty spike (about 3-4x trash damage).

## 7. Rewards
- **Reward choice** (Allakhazam [V]): **Option 1: experience and 105 platinum**; **Option 2: Stambles the Reincarnate**.
  The first fetch summarised option 1 as "Experience (0.5 AA at level 90) + 105 platinum" [P]. Rhaeda's page comment
  summary [P]: "Rewards include experience, platinum, or a pet bunny."
- Fanra: "The reward is a undead rabbit pet for your house."
- Random drops in the instance: **Stout Mottled Mask** (zone-wide rare; Oct 21 2012 comment: it "just dropped off a trash
  mob in Snarlstone Dens during the Halloween Mission 'Under Your Skin'"), **Large Darkhollow Geode** from regular mobs
  (MikuRBD, Oct 8 2012 [P]).

| Item | Live id | Flags / data (EQ Resource live) |
| --- | --- | --- |
| Stambles the Reincarnate | **107106** (Allakhazam 94967) | Lore, Placeable. SMALL, WT 1.5. Item text "Maybe we should have left him buried..."; lore "The lost bunny brother rises!". Placeable in yards, guild yards, houses and guild halls. Allakhazam adds "Some continue bouncing even in undeath!" [P]. Added Oct 31, 2011 on Allakhazam. peq: nodrop 1 (tradeable), icon 3659. |
| Stout Mottled Mask | **86627** (Allakhazam 95416) | Magic, Lore, No Trade. Slot Face. SMALL, WT 0.7. AC 9, HP 75, Mana 75, End 75, STR 11, STA 11, INT 11, WIS 11, AGI 11, SvMagic/Fire/Cold/Disease/Poison 15. Effect **Summon Ale**, any slot, instant (unlimited). Lore "When the gullet needs soothing...". Allakhazam: **Required Level 85** (peq reqlevel 0). Also a reward of "Elder Longshadow #5: Confronting a Traitor" and a drop of "a Drach guardian". |
| Large Darkhollow Geode | **32699** | Quest. MEDIUM, WT 3.5, tribute 188. Lore "Large Geode with multiple colors on the interior". |

## 8. ProjectEQ / our data
- peq has **no** Rhaeda Evel, Skinwalker, Revealed Skinwalker, Corrupted Longshadow or Under Your Skin task. peq's
  `#Elder_Ritualist_Longshadow` (npc 354150, race 454, level 70) belongs to The Hive (drachnidhive 354) DoD missions, not
  to this one.
- peq's `eastkorlacha` zone rows are "Snarlstone Dens", "A Plea for Help", "Bloodeye", "Confronting a Traitor" (versions
  0-3); there is no "Under Your Skin" version.
- Stambles (107106), Stout Mottled Mask (86627) and Large Darkhollow Geode (32699) exist in the peq items table.

## 9. Could NOT find (not guessed)
1. Exact task text of the steps after "Kill the real Revealed Skinwalker".
2. How the real Revealed Skinwalker is chosen (random vs nearest Corrupted Longshadow).
3. Revealed Skinwalker HP, abilities and resist profile; mob counts per room; Elder Ritualist Longshadow's level/look.
4. The real minimum average group level (85 vs higher) and the XP value of option 1.
5. Whether the 17h30m lockout is on success only or also on request/failure.
6. A zone-in /loc for the instance and the Skinwalker throne /loc.

## Sources
- https://everquest.allakhazam.com/db/quest.html?quest=5373 ; achievement ?quest=8836 ; Terror ?quest=5372
- https://everquest.allakhazam.com/db/npc.html?id=36168 (Rhaeda Evel), 38061 (Skinwalker), 38062 (Revealed Skinwalker),
  38074 (Corrupted Longshadow); zone https://everquest.allakhazam.com/db/zones.html?zstrat=804 ; search
  https://everquest.allakhazam.com/search.html?q=Under+Your+Skin
- Items: https://everquest.allakhazam.com/db/item.html?item=94967 , ?item=95416 ; EQ Resource
  https://items.eqresource.com/items.php?id=107106 , 86627 , 32699
- Screenshots: zam.zamimg.com URLs above (local copies in `scratchpad\notd\web\img\` rhaeda.jpg, skinwalker.jpg,
  longshadow.jpg)
- Fanra wiki: https://fanra.fandom.com/wiki/Under_Your_Skin (via the MediaWiki API) and https://fanra.fandom.com/wiki/Halloween
- Bonzz: https://www.bonzz.com/nightsofthedead.htm (UNDER YOUR SKIN (2010 Mission))
- Official news: https://www.everquest.com/news/imported-eq-enus-52055 (Oct 22, 2010)
- Patch notes Nov 2010: https://github.com/nazwadi/patcheq (local `scratchpad\notd\raw\patches\p-2010-2.txt:654,667`)
- Local peq dump (npc_types, items, zone) for the ProjectEQ check
