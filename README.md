# Cataclysm-DDA-Touhou-Mod
**Original by Taberone**

This branch is for new additions that produce non-critical errors when running the mod.

**Read:** the contents are *technically* stable but don't expect proper functionality in-game

----

**Changelog over the master branch (0.9.2.4):**

New spells:
* Aya: custom dash, Deadline day (movement speed buff), Draft blast (low dmg aoe that pushes items far away), Maple fan wind (deals low dmg and stuns an enemy for a duration), Maple fan tornado (improved aoe Maple fan wind), Wind sickle veiling (wind armor that reduces some physical attacks and deals cut dmg)
* Iku: Elekiter Dragon Palace (random lightning strikes), Thundercloud Stickleback (aoe knockback), Veil's like water (damaging cone), Dragon strike (melee-ranged), Thundercloud fish shot (pseudo-chain lightning), Static field (aoe % dmg plus stun for robots, cyborgs, etc)
* Kaenbyou: Immolate (chip dmg with fire dot), Blazing wheel (aoe improved immolate)
* Meiling: Chi heal, Blood flow manipulation (removes bleeding), Mountain breaking cannon (charged punch with huge damage), Red energy release (low dmg punch that breaks terrain), Tiger energy release (aura that increases her melee damage)
* Mokou: Cauterize (deals some and heals for more over time), Spontaneous combustion (self-damaging aoe, applies healing over time)
* Reisen: Entanglement (swap positions with a targeted creature), Optimism (limb dmg balance, small heal and small pain recovery), Probability noise (dodge + dmg reduction + movement reduction effect cleanse), Uncertainty box (unsafe random aoe teleport)
* Remi: Consume blood (regens HP and mana), Demons' dinner fork (repeated aoe attack), Miserable fate (aoe stun with a bit of damage), Vampiric aura (improved melee and on hit heal, reduced defense)
* Sakuya: custom dash, Temporal contraction (aoe slow), Time Paradox (summons a copy that throws knives), Jack the Knife (spawns temporary knife), a custom dash
* Seiga: Charm, Chi drain (dmg dot on target and healing over time on her), Hermit walk (speed boost and LEVITATE effect). Also a missing basic dash
* Tenshi: Earthquake signs (aoe + down), Sky of Scarlet perception (laser), Unletting soil (cone + test push), Keystone crash, pillar and dismiss spells
* Udonge: Wavelength manipulation (buff/aura-like, one for stealth, another for INT, another for PER), Illusionary blast (laser attack)
* Youmu: Double wheel (summons a copy that slashes nearby enemies), Half-body (summons Myon to shoots enemies), Reflection slash (bullet-protecting barrier), Slash of the eternal future (random number of slashes, dmg scales with level), Slash of nether meditation (heavy, long sword attack)
* Changed how mana ammo works: now it creates a stack of caseless ammo lasting 24 h


New monsters:
* A bunch of extinct fauna (Aegirocassis, Agoniatites, Anatosuchus, Andrewsarchus, Arthropleura, Castoroides, Chasmataspis, Cleoniceras, Cotylorhynchus, Dimetrodon, Dipterus, Ectopistes, Endoceras, Eryops, Glossotherium, Glyptodont, Herpetotherium, Hesperosuchus, Icadyptes, Lystrosaurus, Meganeura, Megatherium, Michelinoceras, Moschorhinus, Nochnitsa, Pambdelurion, Paracoroniceras, Parapuzosia, Parastylonurus, Platyoposaurus, Pederpes, Prionosuchus, Saurichthys, Scutosaurus, Sidneyia, Smilosuchus, Taeniolabis, Viatkogorgon, Weigeltisaurus), including reproductive fields, harvests and eggs, if any
* All non-youkai monsters should now spawn properly


New items:
* A bunch of weapons (ARES FMG, CEAM Mòdele 1950, Kar98k, OTs-48 and OTs-48K, PGM Hécate II, Pieper M1893, Spanish M1893, SR-3MP, Thompson Contender, TKB-022P No 2, TKB-022PM No 2, WA2000), including ammo, magazines, weapon attachments if needed, plus some variants
* Two extra gunmods (7.92x33mm conversion for the FN FAL and a vertical grip)
* All previously added weapons and related items should now spawn properly
* A bunch of food (anko [sweet bean paste], bayou style fried shrimp[like meat], bird-based burgers, roasted bird leg, oyakodon, bird pie, bird pot pie, bird soup, caesar salad, dango, dorayaki, karaage, manju, milanesa, paella, sweet buns, sweet potato pie, taiyaki)
* Clothing for the MIB, cheongsam dresses


Misc changes and additions (not fully implemented):
* Greatly expanded the use of the extend field (helping with mod cross-compatibility), except for monstergroups
* Some spells now use field effects, mostly for flavor
* TERA Type 2, Lunarian scouting rifle (can be assembled and broken down into [future] interchangeable parts for different effects), Lunar riot shotgun (featuring an ammo-free blast mode), four more Lunar experimental weapons
* Lampad torch (should work as a torch except it emits hellish light)
* Three types of Gyokuto ear accessories, lunar canteen
* Added several appearance mutations for future NPCs, including a new mutation type for Gyokuto ears
* Generic poltergeist-ish enemies (simple tsukumogami)
* Generic oni enemies that wield kanabo
* Added a experimental drug, addiction and the EOCs
* Most bionics were removed, effects implemented as spells
* A floating keystone vehicle for Tenko


Fixed bugs:
* Aya's, Meiling and Mokou's push components from their spells
* MIB drops
* Mokou's clothes now should be more fire-proof
* Sakuya's knife holders not being able to hold her knives
* Sakuya's knives being too fragile
* Seiga's hair stick encumbrance detriment
* Tenko's sword being super fragile


**Note:** seems that dash spells are all bugged: they don't do damage at the location, and randomly either not cast secondary effects, or do it at double the designated distance. See issues #53511 and #53532 from the C:DDA repo
