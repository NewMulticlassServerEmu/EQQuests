# EverQuest live Halloween / Nights of the Dead: full quest inventory (1999-2025)

Gathered 2026-10-05. Read-only research; nothing under C:\Git\test was changed.

## How this was built

- **Allakhazam search "nights of the dead"** returned 48 quest entries (35 actual quests/tasks/missions; the rest are
  achievements, the Hero's Forge hats ornament and the Overseer achievement). I opened every quest page (WebFetch),
  plus every achievement page so the component lists could catch quests whose names do not start with
  "Nights of the Dead" (that is how Missing / Carving / Squashing Pumpkins were confirmed: they sit under
  Magnificent Winter Squash, quest=10521). Searches for "halloween" and "hallow" found no other quests.
- **EQ Resource** Nights of the Dead page (special.eqresource.com/nightsofthedead.php) lists only 2021, 2022 and 2025.
  I read the per-quest pages for those years.
- **Bonzz's NotD page** (bonzz.com/nightsofthedead.htm) lists 2005-2025 by year with waypoints. It agrees with
  Allakhazam except where noted under "Year conflicts".
- **Allakhazam wiki EQ:Halloween** (year-by-year list 2005-2014).
- **Official news**: everquest.com 2023, 2024 and 2025 NotD announcements. **2023 and 2024 added no quests**, only
  Marketplace items: bags in 2023; Sinister Dark furniture, two Metamorph familiars and Visage of a Sarnak Skeleton
  in 2024. 2025 added the four Toxxulia quests, and the Visage of the Restless Cadaver was sold in the Marketplace.
- **Patch notes**: github.com/nazwadi/patcheq (1999 to mid-2022) were grepped for halloween / nights of the dead /
  hallow / pumpkin / haunt. Relevant hits: 1999-11-03 (Halloween GM event, PoH opened), 2005-11-01 (Halloween events
  fixes), 2006-10-30 (zombie uprising, lycanthropy in Kithicor; refuge in PoK and Crescent Reach; Haunted Jack and
  Spooky Sally in hometowns), 2008-10-29 (scarecrow pathing in West Karana), 2009 (Frightening Writ / Gravedigger),
  2010 (Terror of Illis Taberish repop), 2014 (Digging Their Graves above 100), 2015 (Haunted Jack/Spooky Sally only
  during NotD), 2017 (NotD runs 4 weeks), 2021-2 (Cikdew "has found her voice", Arlien Browch).
- Local: C:\Git\test\EQQuests\events\nights-of-the-dead.md and expansions\01-ruins-of-kunark.md (Digging Their
  Graves, Terror of Illis Taberish, The Bone Collector, The Dragon Ring) and 03-shadows-of-luclin.md (Missing Costume
  Pieces).

### Zone to expansion (from the local peq `zone.expansion` column, read-only query)

0 classic, 1 Kunark, 2 Velious, 3 Luclin, 4 PoP, 5 LoY, 6 LDoN, 7 GoD, then 8 OoW, 10 DoD, 11 PoR, 12 TSS, 13 TBS,
14 SoF, 15 SoD, 16 UF, 17 HoT, 19 RoF.

| Zone (live name) | peq short_name (id) | peq expansion | GoD or lower? |
| --- | --- | --- | --- |
| Kithicor Forest | kithicor (20) | 0 classic | yes (live also has the TSS rebuild kithforest 410; see note A) |
| Plane of Knowledge | poknowledge (202) | 4 PoP | yes |
| Estate of Unrest, Befallen, Castle Mistmoore, Rivervale, Rathe Mtns, Qeynos Hills, Surefall Glade, Greater/Lesser Faydark, West/South Karana, Everfrost, The Feerrott, Erudin, Erudin Palace, Shadowrest, Butcherblock, Plane of Hate (old), The Hole (= "Ruins of Old Paineel") | classic ids | 0 | yes |
| Nektulos Forest | nektulos (25) | 1 (peq quirk; it is a classic zone) | yes |
| Field of Bone, Kurn's Tower, Lake of Ill Omen, Firiona Vie, Emerald Jungle, Ruins of Sebilis, Swamp of No Hope | Kunark ids | 1 | yes |
| Iceclad Ocean, Tower of Frozen Shadow, Dragon Necropolis, The Warrens | Velious ids | 2 | yes |
| Netherbian Lair, Tenebrous Mountains, Katta Castellum, The Maiden's Eye, Shar Vahl | Luclin ids | 3 | yes |
| Plane of Nightmare | ponightmare (204) | 4 | yes |
| Wall of Slaughter | wallofslaughter (300) | 8 OoW | **no** |
| Snarlstone Dens | eastkorlacha (363) | 10 DoD | **no** |
| West Freeport "2.0" | freeportwest (383) | 11 PoR | no (classic freportw 9 exists; note A) |
| Crescent Reach | crescent (394) | 12 TSS | **no** |
| Blightfire Moors | moors (395) | 12 TSS | **no** |
| Goru`kar Mesa | mesa (397) | 12 TSS | **no** |
| The Steppes | steppes (399) | 12 TSS | **no** |
| Icefall Glacier | icefall (400) | 12 TSS | **no** |
| The Commonlands (merged) | commonlands (408) | 12 TSS | no (classic commons 21 / ecommons 22 exist; note A) |
| Toxxulia Forest "2.0" | toxxulia (414) | 12 TSS | no (classic tox 38 exists; note A) |
| Misty Thicket "2.0" | mistythicket (415) | 12 TSS | no (classic misty 33 exists; note A) |
| Barren Coast | barren (422) | 13 TBS | **no** |
| The Buried Sea | buriedsea (423) | 13 TBS | **no** |
| Loping Plains | lopingplains (443) | 14 SoF | **no** |
| Steamfont Mountains "2.0" | steamfontmts (448) | 14 SoF | no (classic steamfont 56 exists; note A) |
| Field of Scale | oldfieldofbone (452) | 15 SoD | **no** |
| The Underquarry | underquarry (482) | 16 UF | **no** |
| House of Thule | thulehouse1/2 (701/702) | 17 HoT | **no** |
| Valley of King Xorbb | xorbb (753) | 19 RoF | **no** |

**Note A, rebuilt zones.** Live moved several Antonica/Odus zones to rebuilt versions (Toxxulia 2.0, Misty Thicket
2.0, The Commonlands, West Freeport 2.0, Steamfont 2.0, and probably Kithicor). The NPCs and spawns sit in those
rebuilt zones, which are TSS/SoF/PoR zones. Each one has a classic zone with the same name in peq. The
"ERA (classic stand-in)" column below means: GoD-or-lower **if** the NPC/spawn is placed in the classic zone. Live
coordinates will not carry over 1:1. The 2005 quests (Kithicor set, Trick or Treat) were made before the rebuilds, so
they used the classic zones in the first place.

---

## Master table

Legend for "Era": the newest expansion among the zones that version needs, by live zone, then by classic stand-in
(note A) when they differ. **GoD?** = GoD-or-lower by the classic stand-in.

| # | Quest (exact name) | Start NPC, zone | All zones needed (per version) | Type | Levels | Year | Source | Era | GoD? |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | Nights of the Dead: Trick or Treat for the Old Man | Old Man Draykey, Kithicor Forest (1915, 4535) | Kithicor, Estate of Unrest, PoK, Commonlands, Field of Bone, Iceclad Ocean, Toxxulia Forest, Castle Mistmoore, Netherbian Lair, West Karana, Befallen | Quest, solo | 10-90 | 2005 | Alla quest=3254 | Luclin (Netherbian) / PoP (PoK) | **yes** |
| 2 | Nights of the Dead: The Hungry Halfling | Mippie Diggs, Kithicor (near Rivervale line) | Kithicor; pumpkin flesh from scarecrows in Estate of Unrest; rest bought from merchants | Task, solo (baking/brewing) | 10-125 | 2005 | Alla 4665 | classic | **yes** |
| 3a | Nights of the Dead: Missing Costume Pieces [30] | a Dressed-Up halfling, Kithicor (1090, -570) | Kithicor + Castle Mistmoore | Shared task 1-6 | 20+ | 2005 | Alla 4898 | classic | **yes** |
| 3b | same [40] | same | Kithicor + Tenebrous Mountains | shared | | 2005 | Alla 4898 | Luclin | **yes** |
| 3c | same [53] | same | Kithicor + Katta Castellum | shared | | 2005 | Alla 4898 | Luclin | **yes** |
| 3d | same [58] | same | Kithicor + The Maiden's Eye | shared | | 2005 | Alla 4898 | Luclin | **yes** |
| 3e | same [66+] | same | Kithicor + Plane of Hate (old, Innoruuk's room) | shared | | 2005 | Alla 4898 | classic | **yes** |
| 4a | Nights of the Dead: The Bone Collector [20] | Barsin, the Bone Collector, Kithicor (-110, 25) | Kithicor + Befallen, Estate of Unrest, Kurn's Tower | Group task 3-6 | 10+ | 2005 | Alla 5369 | Kunark | **yes** |
| 4b | same [41] | same | Kithicor + Tower of Frozen Shadow, Lower Guk, plaguebone skeletons ("any zone") | group | | 2005 | Alla 5369 | Velious | **yes** |
| 4c | same [60] | same | Kithicor + Plane of Hate, Ruins of Sebilis, Dragon Necropolis | group | | 2005 | Alla 5369 | Velious | **yes** |
| 4d | same [69+] | same | Kithicor + **Wall of Slaughter**, Plane of Nightmare, Dragon Necropolis | group | 69+ | 2005 | Alla 5369 | **OoW** | **no** (Wall of Slaughter) |
| 5 | Nights of the Dead: Out With the Old | a silly puppet / Cathil, Kithicor (1230, 1060) | Kithicor mission instance ("Nights of the Dead: Kithicor Forest: Out With the Old") | Group monster mission 3-6 | 20-125 | 2005 | Alla 5370 | classic | **yes** |
| 6 | Nights of the Dead: Bone Mask of Horror | Zigan Ribshard, PoK (-640, 179) | PoK + the five above | Quest (capstone) | 20+ | 2005 | Alla 5371 | PoP | **yes** (needs 4a-4c at cap 65) |
| 7 | Nights of the Dead: Toadstool Surprise | a wizened hermit, PoK (near main bank) | PoK + Toxxulia Forest (toadstools, /open) | Task, solo | 1-90 | 2006 | Alla 3802 | TSS (Tox 2.0) / classic tox: PoP | **yes** (classic tox) |
| 8 | Nights of the Dead: Making Candy Apples | Wicked Winnie, PoK (180, 275) | PoK (Haunted Jack, free candy apple) + Steamfont Mtns (Finkel Rardobaen, -1235,-1465) **or** Toxxulia Forest (Quana Rainsparkle, good-aligned only) | Task, solo, ~3h repeat timer (2006-extra.md) | 25-90 | 2006 | Alla 3801 | SoF (Steamfont 2.0) / classic steamfont or tox: PoP | **yes** (classic stand-in) |
| 9 | Nights of the Dead: Find the Black Cat | Syxa Jewlborn, Kithicor (Commonlands zone-in) | Kithicor | Task, solo, 3h lockout (2006-extra.md) | 25-125 | 2006 | Alla 3799 | classic | **yes** |
| 10 | Nights of the Dead: Great Zombie Attack | Crazy Charlie, Kithicor (1815, 3790) | Kithicor + Rathe Mountains (zombie troopers); ends on the 10th zombie, no return (2006-extra.md) | Task, solo | 1-125 | 2006 | Alla 3842 | classic | **yes** |
| 11 | Nights of the Dead: Lycanthrope's Cure | Laryen Lycanthrope, Rivervale (-185, -260) | Rivervale + Kithicor (5 fallen werewolves) | Task, solo | 30-125 | 2006 | Alla 3823 | classic | **yes** |
| 12 | Nights of the Dead: Monster Mash | Lurgh, Kithicor (Rivervale zone-in) | Kithicor (skeleton parts at night) | Task, solo | 35-90 | 2006 | Alla 3800 | classic | **yes** |
| 13 | Nights of the Dead: Skeleton Zapping | any "<name> the Bonecollector" in a home city (list below) | start city + any zone with qualifying skeletons; confirmed working: Butcherblock (enraged dwarf skeleton), Field of Bone/Kurn's (undead farmer), Crescent Reach, Blightfire Moors | Task, solo | 10-125 | 2006 | Alla 3803 | mixed; a classic city + Butcherblock is all classic | **yes** (classic Bonecollectors + Butcherblock / Field of Bone); the Crescent Reach Bonecollector and CR/Moors skeletons are TSS |
| 14 | Nights of the Dead: Aragol's Seance | Aragol Gloomflow, Crescent Reach (Nokk cave) | Crescent Reach | Task, solo | 15-125 | 2006 (Alla page says 2007) | Alla 4623 | **TSS** | **no** (Crescent Reach) |
| 15 | Nights of the Dead: Haunted Cave | Jilian Florantine, Crescent Reach (314, -2119) | Crescent Reach (Nokk undead cave) | Task, solo | 20-90 | 2006 or 2009 (conflict) | Alla 4904 | **TSS** | **no** (Crescent Reach) |
| 16 | Nights of the Dead: Toxxulia Pie Fling | Marta Stalwart, Toxxulia (1987, -739, S of Erudin line) | Toxxulia Forest | Task, solo | 2-90 | 2007 | Alla 4319 | TSS (Tox 2.0) / classic tox | **yes** (classic tox) |
| 17 | Nights of the Dead: Troublemakers in Faydark | Silas Lightweaver, Greater Faydark (490, 395) | Greater Faydark (catch) + Lesser Faydark (release) | Task, solo | 1-90 | 2007 | Alla 4318 | classic | **yes** |
| 18 | Nights of the Dead: Nektulos Ghost Rider | Grom Shives, Nektulos (-1915, 1200) | Nektulos Forest (10 checkpoints in 4 min on the Abyssal Steed it hands you) | Task, solo | 1-125 | 2007 | Alla 4317 | classic | **yes** |
| 19 | Nights of the Dead: Undead Rising | Corporal Gravlin, Qeynos Hills (-66, 60) | Qeynos Hills + Surefall Glade (escort) | Task, solo | 15-90 | 2007 (Alla page says 2009) | Alla 5068 | classic | **yes** |
| 20 | Nights of the Dead: Rongol #1 - Carry the Torch | Rongol, West Karana (-3695, -9280) | West Karana (torches from Innkeep Danin) | Task, solo | 1-125 | 2008 | Alla 4901 | classic | **yes** |
| 21 | Nights of the Dead: Rongol #2 - Scarecrow Roundup | Rongol, West Karana | West Karana | Task, solo, 18h lockout | 1-125 | 2008 (Alla page says 2009) | Alla 4902 | classic | **yes** |
| 22 | Nights of the Dead: Necromancer's Garden | Leavalin Mossbite, Greater Faydark (-1115, -1930) | Greater Faydark | Shared task 1-6, 10-min limit | **70**-125 (Alla) / 11 (Alla wiki) | 2008 (Alla page says 2007) | Alla 4903 | classic | **yes** zone-wise; min level 70 is above our 65 cap (see notes) |
| 23 | Nights of the Dead: Digging Their Graves [1-22] | Edmund Strangeways, PoK (650, 185) | PoK + Nektulos Forest **or** Lake of Ill Omen | Task, solo, 18h lockout | 1-22 | 2009 | Alla 4899 | Kunark | **yes** |
| 23b | same [23-32] | same | PoK + Emerald Jungle or Firiona Vie | | ~23-32 | 2009 | Alla 4899 | Kunark | **yes** |
| 23c | same [~45] | same | PoK + Goru`kar Mesa **or** Emerald Jungle | | ~45 | 2009 | Alla 4899 | Kunark via EJ (Mesa = TSS) | **yes** only if the EJ option is used |
| 23d | same [~55] | same | PoK + Barren Coast or Goru`kar Mesa | | ~55 | 2009 | Alla 4899 | **TBS/TSS** | **no** (Barren Coast, Mesa) |
| 23e | same [~65] | same | PoK + The Steppes or The Buried Sea | | ~65 | 2009 | Alla 4899 | **TSS/TBS** | **no** |
| 23f | same [~75] | same | PoK + Loping Plains or The Steppes | | ~75 | 2009 | Alla 4899 | **SoF/TSS** | **no** |
| 23g | same [85] | same | PoK + Field of Scale or Loping Plains | | 85 | 2009 | Alla 4899 | **SoD/SoF** | **no** |
| 24 | Nights of the Dead: The Hunt for Tattooed Flesh | auto-assigned after the first Digging Their Graves; Edmund Strangeways, PoK | PoK (5 inspections) + whatever Digging Their Graves version you run | Task (grand task), solo | 1-125 | 2009 | Alla 4900 | follows #23 | **yes** for chars on 23a-23c |
| 25a | Nights of the Dead: Terror of Illis Taberish [6] | Illis Taberish, PoK (~300, 350) | PoK + Nektulos Forest | Shared task 1-3, 18h lockout | 1-10 | 2010 | Alla 5372 | classic / Kunark flag | **yes** |
| 25b | same [16] | same | PoK + Lake of Ill Omen | | 10-20 | 2010 | Alla 5372 | Kunark | **yes** |
| 25c | same [26] | same | PoK + Firiona Vie | | 20-30 | 2010 | Alla 5372 | Kunark | **yes** |
| 25d | same [36] | same | PoK + Emerald Jungle | | 30-40 | 2010 | Alla 5372 | Kunark | **yes** |
| 25e | same [46] | same | PoK + Goru`kar Mesa | | 40-50 | 2010 | Alla 5372 | **TSS** | **no** (Mesa) |
| 25f | same [56] | same | PoK + Barren Coast | | 50-60 | 2010 | Alla 5372 | **TBS** | **no** |
| 25g | same [66] | same | PoK + The Steppes | | 60-70 | 2010 | Alla 5372 | **TSS** | **no** |
| 25h | same [76] | same | PoK + Loping Plains | | 70-80 | 2010 | Alla 5372 | **SoF** | **no** |
| 25i | same [81+] | same | PoK + Field of Scale | | 80+ | 2010 | Alla 5372 | **SoD** | **no** |
| 26 | Nights of the Dead: Under Your Skin | Rhaeda Evel, PoK (/loc 300, 322 - see under-your-skin.md); flag = any Terror of Illis Taberish | PoK + Snarlstone Dens instance | Group task 3-6, 17.5h lockout | 85-125 | 2010 | Alla 5373 | **DoD** | **no** (Snarlstone Dens) |
| 27 | Nights of the Dead: The Witch's Wishes | Cikdew, South Karana (under the north bridge) | South Karana, Erudin (palace entrance), The Feerrott (Mugu outside Oggok), Shadowrest, PoK (Scholar Klaz, Chef Denrun, Devin Traical); spider legs from any spider | Task, solo | 1-130 | 2021 | Alla 9223; EQR thewitchswishes.php | PoP (PoK) | **yes** |
| 28 | Missing Pumpkins | Arlien Browch, The Commonlands (Commonlands tunnel) | Commonlands, Nektulos, Kithicor, Misty Thicket, Everfrost, West Karana (Minda and Tukk's farm), The Feerrott | Task, solo | not stated | 2021 | EQR missingpumpkins.php (no Alla quest page found) | TSS (Commonlands, Misty 2.0) / classic stand-ins | **yes** (classic commons/ecommons + misty) |
| 29 | Carving Pumpkins | Hule C. Zarshcl, West Karana (-3715, -7665) | West Karana | Task, solo | not stated | 2021 | EQR carvingpumpkins.php | classic | **yes** |
| 30 | Squashing Pumpkins | Levy Cullpay, West Karana (-3140, -4445) | West Karana (needs the Carving Pumpkins knife/kit) | Task, solo | not stated | 2021 | EQR squashingpumpkins.php | classic | **yes** |
| 31a | Nights of the Dead: The Rot Within [65] | Tully Alford, Blightfire Moors (-132, 610) | Blightfire Moors | Task, solo, 5h | ~25-? (a level 25 got it) | 2022 | Alla 11150 comments (Gary168) | **TSS** | **no** (Blightfire Moors) |
| 31b | same [85] | same | Blightfire Moors + Icefall Glacier (mammoths) | | ~68 got it | 2022 | Alla 11150 comments | **TSS** | **no** |
| 31c | same [106+] | same | Blightfire Moors + Valley of King Xorbb | | 106-125 | 2022 | Alla 11150; EQR therotwithin106.php | **RoF** | **no** |
| 32 | Nights of the Dead: The Rot's Sporali | Tully Alford, Blightfire Moors | Blightfire Moors | Task, solo, 5h | 25-125 | 2022 | Alla 11151 | **TSS** | **no** |
| 33 | Nights of the Dead: Lurking Beneath the Rot | Tully Alford, Blightfire Moors | Blightfire Moors | Task, solo, 5h | 1-130 | 2022 | Alla 11158 | **TSS** | **no** |
| 34 | Nights of the Dead: Big Trouble in Little Mesa | Astyn the Gray, Blightfire Moors (1755, 420) | Blightfire Moors + Goru`kar Mesa: The Troubled Mesa (instance) | Group mission 1-6 (Alla: 3-6), 5h lockout | 120-130 | 2022 | Alla 11140 (+ challenges 11141) | **TSS** (needs 120+) | **no** |
| 35 | Nights of the Dead: The Lost Handkerchief | Larref, Toxxulia Forest (-357, 1099) | Toxxulia Forest + The Warrens | Task, solo | 1-125 | 2025 | Alla 13375; EQR thelosthandkerchief.php | Velious (classic tox stand-in) | **yes** |
| 36a | Nights of the Dead: Did You Hear That? (low version) | Efferri, Toxxulia Forest (-346, 1089) | Toxxulia + The Warrens | Task, solo | seen at 11-13 | 2025 | Alla 13377 comments (SCindyee) | Velious | **yes** |
| 36b | same (mid version) | same | Toxxulia + Ruins of Old Paineel (= The Hole) | | seen at 54 | 2025 | Alla 13377 comments | classic | **yes** |
| 36c | same (Underquarry version) | same | Toxxulia + The Underquarry | | higher (exact band unknown) | 2025 | Alla 13377; EQR didyouhearthat.php | **UF** | **no** (Underquarry) |
| 37 | Nights of the Dead: Wash It Keener | Sharden, Toxxulia Forest (-365, 1092) | The Buried Sea (3 tide pools) + Toxxulia (fire) | Task, solo | 1-125 (no versions reported) | 2025 | Alla 13376; EQR washitkeener.php | **TBS** | **no** (Buried Sea) |
| 38 | Nights of the Dead: Remove the Troublesome Trick-Or-Treaters | Reeks, Toxxulia Forest (-480, 1063) | House of Thule instance | Group mission 1-6, 3h (Alla) / 6h (EQR) lockout | 1-125 | 2025 | Alla 13378; EQR removethetroublesometrickortreaters.php | **HoT** | **no** (House of Thule) |

### Historic / GM-run Halloween content (no player-startable quest)

| Item | Year | Zone | What it was | Source | Era |
| --- | --- | --- | --- | --- | --- |
| Battle of Bloody Kithicor / PoH opening | Oct 31, 1999 | Kithicor Forest, High Hold Pass, Plane of Hate | GM event. Afterwards Kithicor gets level 35+ undead at night, which is permanent zone content, not a quest | patch note 1999-11-03; Fanra/forum results | classic |
| GM weekend events: "Scavenger Hunts, Attack of the Pixies, Brownies seeking revenge, a shipwrecked gnome, a bear named Fluffy on a rampage" | Oct 26, 2001 | various, not named | GM-hosted, one-off | Allakhazam story=297 | n/a |
| The Dragon Ring (Ithiosar the Fallen, then Ithiosar the Black + black ravengers) | Oct 2002 | Swamp of No Hope (caves toward Trakanon's Teeth) | GM-triggered scripted spawn; Fury belts/crowns/rings drop. Allakhazam keeps it as a removed quest | Alla quest=2138; local 01-ruins-of-kunark.md:8687 | Kunark |
| The Haunting of Kithicor | Oct 2-29, 2012 | Kithicor Forest | Guides/Community Team event | everquest.com/news/imported-eq-enus-524379 | n/a |
| Haunted Jack (free candy) and Spooky Sally (free costumes/illusions) | 2006+ | every hometown + PoK | merchants, not quests (Haunted Jack also supplies the candy apple for #8) | patch 2006-10-30, 2015 | classic/PoP |

### Achievements / collections / other (not quests, listed for completeness)

- Achievements: Pernicious Puppets (8830: #1-#5), The Monster Mash (8832: all of #7-#15 = Toadstool, Aragol,
  Candy Apples, Black Cat, Skeleton Zapping, Haunted Cave, Great Zombie, Lycanthrope, Monster Mash),
  Undead Rising (8833: #16-#19), Garden Variety Ghouls (8834: #20, #21, #22, #27), Strange Ways (8835: #24),
  Altered Beasts (8836: any Terror version + Under Your Skin), Magnificent Winter Squash (10521: #28-#30),
  Investing the Infesting (11139: #31c, #32, #33), Big Trouble in Little Mesa (11140) + Mission Challenges (11141),
  Tales of Tragedy (13372: #35-#37), Remove the Troublesome Trick-Or-Treaters (13373), Hero's Forge - Nights of the
  Dead Hats (6845, 2012: own 5 hat ornaments).
  Note: on a GoD-only server, The Monster Mash cannot be finished (Aragol's Seance and Haunted Cave are in Crescent
  Reach, TSS), and neither can Altered Beasts (Under Your Skin is in Snarlstone Dens, DoD), unless those quests are
  moved. Garden Variety Ghouls, Pernicious Puppets, Undead Rising, Strange Ways (low versions) and Magnificent Winter
  Squash are all-GoD.
- Collections (the RoF2 client probably has no collection UI): Clutch of Fungi (Blightfire Moors, 2022, 11142);
  Dastardly Discarded Deadly Decorations (Toxxulia Forest, 2025).
- Overseer: World Nights of the Dead: Quests (11154): Season of Dread, Tricks and Treats, Ways of the Wicked, Bakes and
  Shakes, Fear Itself, Not Our Festival. These are Overseer quests, not world quests.
- Marketplace only: 2015 items; 2023 bags; 2024 Sinister Dark furniture, Metamorph: Putrid Rotdog / Menacing Samhain,
  Visage of a Sarnak Skeleton; 2025 Metamorph: Rotflesh Scavenger / Burrowing Molerat, Visage of the Restless Cadaver.

---

## Per-quest notes

**#1 Trick or Treat for the Old Man (Alla 3254).** 11 stops: Kithicor (Draykey: bag + codex), Unrest (Crabby the
Rotten in the hedge maze), PoK (Grand Librarian Maelin atop the library), Commonlands (Sergeant Ragus on patrol), Field
of Bone (Immug Lashtail in the pit), Iceclad (Nilham the Chef, gnome igloo), Toxxulia (Fuzz Selppa on the beach),
Mistmoore (Nate behind the graveyard), Netherbian Lair (Poil Lolp in the caves), West Karana (Scary Miller at the
farm), Befallen (key from a shadowknight, then Wraps McGee). Reward: Bristlebane's Ticket of Admission + 5 snacks.
Unknown: which classic Commonlands zone (West or East) Sergeant Ragus patrolled in 2005.

**#2-#6 Kithicor set (2005).** Full walkthroughs are in EQQuests\events\nights-of-the-dead.md, which was checked
against Alla today. Bone Collector [69+] is the only version outside GoD (Splintered Discordling Bone, rare drop in
Wall of Slaughter). The version follows the group's average level and live never published the exact bands, so
[60] covers our level-65 cap. Out With the Old runs in its own Kithicor mission zone (Alla zone "Nights of the Dead:
Kithicor Forest: Out With the Old"); in EQEmu that would be an instance version of kithicor. A 2005-11-01 patch note
says the event flags were fixed and the run was extended to Nov 14.

**#7-#15 (2006).** Patch 2006-10-30: "a strange zombie uprising, an increased bout of lycanthropy, and other creepy
encounters rising up within Kithicor Forest... Folks in need of assistance have been taking refuge within the Plane of
Knowledge and Crescent Reach." That supports 2006 for the Crescent Reach Aragol's Seance. Its Alla page says
"introduced in October 2007"; the Alla wiki and Bonzz say 2006. Haunted Cave: Alla page "October 2009", Alla wiki
2006, Bonzz lists it under 2009. Unresolved.
Skeleton Zapping Bonecollectors (Alla NPC search + quest page): Uzek (Nektulos), Renla (North Qeynos), Rentila
(Surefall Glade), Mynen (Greater Faydark/Kelethin), Filada (Northern Felwithe per the quest page, Greater Faydark per
the NPC search/Bonzz), Bethun (Misty Thicket 2.0), Pralak (Crescent Reach), Aauman (Toxxulia 2.0), Kordulaf
(Butcherblock), Ordun (West Freeport 2.0), Khbantiz (Field of Bone), Jarz (Shar Vahl), Oxrun (Everfrost). The quest
page also names Ak'Anon, Cabilis East, Erudin, Grobb, Halas, Neriak, North Kaladim, Oggok and Paineel as cities with
one, without matching each name to a city. Qualifying skeletons that players confirmed: skeletal ogre and undead
fisherman (Crescent Reach), accursed lookout (Blightfire Moors), enraged dwarf skeleton (Butcherblock haunted tower),
undead farmer (Field of Bone / Kurn's). Reported NOT working: halfling skeleton (Misty), grimling skeleton (Shar
Vahl), decaying skeletons (newbie zones). The full list of valid skeletons is unknown.
Making Candy Apples: Liquid Caramel from Finkel Rardobaen, Steamfont 2.0 (-1235, -1465, "near the three huts"), or
Quana Rainsparkle in Toxxulia (good-aligned only).

**#16-#19 (2007).** Patch 2007-10 notes are generic ("new and old ghoulish tasks"). Undead Rising: Alla page says
"October 2009 | Seeds of Destruction era", Alla wiki and Bonzz say 2007. Unresolved. Nektulos Ghost Rider hands you
"Bridle of the Cursed" (an Abyssal/Nightmare steed) and the "Mask of Eyes"; reward Cloak of Death.

**#20-#22 (2008).** Patch 2008-10-29: "Fixed a pathing bug in West Karana that was causing scarecrows to be far too
scarce", which supports 2008 for the Rongol tasks (the Scarecrow Roundup Alla page says 2009). Necromancer's Garden:
the Alla page says level 70 min and "Secrets of Faydwer era, 2007". Its reward, Floating Skull Potion, needs level
70+. The Alla wiki lists min level 11. Unresolved. If it really is 70+, the quest is out of reach at our 65 cap even
though the zone is classic.

**#23-#24 (2009).** Edmund's Shovel is clicked on "disturbed earth" ground objects, which spawn a disturbed spirit or a
tattooed zombie (only the zombie drops the skin). Five completions, then The Hunt for Tattooed Flesh pays out the
Frightening Writ (scarecrow mercenary + title "the Gravedigger", patch 2009). The bands in the table are from the
Alla/EQQuests text and are approximate ("~45", "~55"). Bonzz gives a slightly different single-zone-per-level list
(Nektulos 10, LoIO 20, EJ 30, FV 30, Mesa 50, Barren 60, Steppes 70, Loping 80, Field of Scale). Exact band edges are
unknown. On a GoD server the 23a-23c zones (Nektulos, LoIO, EJ, FV) cover levels 1 to about 45-50. Characters 50-65
would need a remap. Patch 2014 made it work above level 100.

**#25-#26 (2010).** Version names [6]...[81+] are from the Altered Beasts achievement (Alla 8836). The per-version
mob names (four distorted souls each) are in EQQuests 01-ruins-of-kunark.md:16418-16426. The Under Your Skin
instance is in Snarlstone Dens (DoD). peq has eastkorlacha versions 0-3 but none for this mission.

**#27-#30 (2021).** Patch 2021-2: "Cikdew has found her voice and will be looking for assistance during Nights of the
Dead" and "Arlien Browch has been seen hauling a large shipment of pumpkins. She should reach the Commonlands Tunnel
just in time." Bonzz tags Witch's Wishes "[2008/2021]": Cikdew existed earlier as a silent NPC and the quest is 2021.
Missing Pumpkins ground-spawn waypoints (Bonzz): Nektulos 880,-820; Kithicor 645,2170; Misty -310,-145; Everfrost
1670,250; West Karana 1335,-2035; Feerrott 1010,-1980; Minda/Tukk farm -3605,-7680. These are live coordinates (live
Kithicor/Misty may be the rebuilt zones). Levels for #28-#30 are not stated anywhere I found.

**#31-#34 (2022).** Everything starts in Blightfire Moors (TSS). The Rot Within lower versions come only from two
Allakhazam comments ("Quest name = The Rot Within [65] when I get it at level 25", "[85] when I get it at level 68";
the [85] uses Icefall Glacier mammoths). The summarizer's description of [65] (Blightfire swamp giants/treants,
Ghoulish Grape Juice) looks like The Rot's Sporali and may be mixed up. EQ Resource lists the lower version as "The
Rot Within ???". None of these are GoD.

**#35-#38 (2025).** EQ Resource posted them on Sept 9, 2025. The live start NPCs stand in Toxxulia Forest 2.0 (TSS).
Did You Hear That? scales by zone: The Warrens for a level 11-13 party; "Marta's footprints travel through Paineel
towards the Ruins of Old Paineel" for a level 54; The Underquarry otherwise. The band edges are unknown. Ruins of Old
Paineel is live's name for The Hole (Alla zone "Ruins of Old Paineel (The Hole)"), a classic zone. Wash It Keener
reports no other versions. Remove the Troublesome Trick-Or-Treaters is a House of Thule instance.

---

## Could NOT verify / unknowns

1. **Pre-2005 items in the request:** I found no source for a "Haunted Hunt in Unrest", a "rat bounty", or a
   "Misty Thicket raid" as Halloween quests. The pie fling is the 2007 Toxxulia Pie Fling, the costume merchants are
   Haunted Jack/Spooky Sally (2006), the Kithicor invasion is the 1999 GM event, and Crazy Charlie / Laryen
   Lycanthrope / Grom Shives / Marta Stalwart are the 2006-2007 tasks (#10, #11, #18, #16). Pre-2005 Halloween content
   was GM-run (1999 Kithicor/PoH, 2001 weekend GM events, 2002 Ithiosar). No scripted quest survives from those years
   except Alla's removed "The Dragon Ring". Fanra's wiki (everquest.fanra.info and fanra.fandom.com) returned 403/402
   and web.archive.org was blocked, so its year-by-year history is unchecked.
2. Year conflicts, unresolved: Aragol's Seance (2006 vs 2007), Haunted Cave (2006 vs 2009), Undead Rising (2007 vs
   2009), Scarecrow Roundup (2008 vs 2009), Necromancer's Garden (2007 vs 2008, and min level 70 vs 11).
3. Exact level bands: Bone Collector, Missing Costume Pieces, Digging Their Graves, Did You Hear That?, The Rot
   Within. Live publishes approximate bands only.
4. Levels for Missing / Carving / Squashing Pumpkins: not stated.
5. Whether live NotD Kithicor content now sits in kithforest (TSS rebuild) or classic kithicor. It does not matter for
   EQEmu (classic kithicor exists), but live coordinates may not match classic geometry.
6. Complete list of skeletons that count for Skeleton Zapping, and the city of every Bonecollector.
7. 2026 Nights of the Dead content is out of scope and was not checked.

## Sources

- https://everquest.allakhazam.com/search.html?q=nights+of+the+dead (48 quest entries)
- https://everquest.allakhazam.com/db/quest.html?quest=N for N = 2138, 3254, 3799, 3800, 3801, 3802, 3803, 3823, 3842,
  4317, 4318, 4319, 4623, 4665, 4898, 4899, 4900, 4901, 4902, 4903, 4904, 5068, 5369, 5370, 5371, 5372, 5373, 8830,
  8832, 8833, 8834, 8835, 8836, 9223, 10521, 11139, 11140, 11150, 11151, 11154, 11158, 13372, 13375, 13376, 13377, 13378
- https://everquest.allakhazam.com/wiki/EQ:Halloween ; https://everquest.allakhazam.com/wiki/eq:Nights_of_the_Dead
- https://everquest.allakhazam.com/story.html?story=297 (2001 GM events)
- https://special.eqresource.com/nightsofthedead.php and the per-quest pages: thewitchswishes, missingpumpkins,
  carvingpumpkins, squashingpumpkins, therotwithin, therotwithin106, therotssporali, lurkingbeneaththerot,
  bigtroubleinlittlemesa, thelosthandkerchief, didyouhearthat, washitkeener, removethetroublesometrickortreaters (.php)
- https://www.bonzz.com/nightsofthedead.htm
- https://www.everquest.com/news/eq-notd-2023 ; /eq-nights-of-the-dead-2024 ; /eq-nights-of-the-dead-2025 ;
  /imported-eq-enus-524379 (Haunting of Kithicor 2012)
- https://github.com/nazwadi/patcheq (patches-1999 .. patches-2022-1)
- Local: C:\Git\test\EQQuests\events\nights-of-the-dead.md; EQQuests\expansions\01-ruins-of-kunark.md (8687, 12417,
  15596, 16274, 16370); 03-shadows-of-luclin.md (11502); peq `zone` table (read-only SELECT via peq_sql.py)

## Corrections from the 2026-10-05 follow-up research
See `2005-extra.md`, `2006-extra.md`, `2007-extra.md` and `under-your-skin.md` (each lists its sources). In short:
- Item ids: several ids labelled live in earlier notes were Allakhazam's internal ids; live ids are in `2005-extra.md` section A.
- Nektulos Ghost Rider's checkpoints and Grom fit the rebuilt Nektulos (peq version 1), and the Toadstool Surprise spawn points fit the rebuilt Toxxulia, not the classic zones.
- Sergeant Ragus patrols East Commonlands (Bonzz); his own treat line is "Here you go. Be careful not to make yourself sick." (Allakhazam 2012 comment).
- Under Your Skin is 2010 (official news Oct 22, 2010); Toadstool hermit level: Allakhazam 30, Bonzz 50.
- The Rat Bounty (#Roosevelt, PoK) has no live source: it is a ProjectEQ custom event (task 500222, the "Rattus Norvegicus" hunt).
