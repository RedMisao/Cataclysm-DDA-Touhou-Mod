# Design (last updated 2024-03-17)

An attempt to explain how balance is done, or rather why is missing, from the mod and the Expansion.  I'm assuming the reader is acquainted with Touhou, so I'm skipping Touhou's setting and common jargon.  Check the [glossary](#glossary) if you need to understand the terminology I use for convenience
**WARNING**: contains spoilers


## Character balance 
    
Lore-wise, 2hus can be considered "broken" in one way or another.  Usually it's either due their ability or another of their traits.  Transforming their abilities or traits from qualitative (2hu can manipulate wavelengths) to quantitative power (Udonge's aura spells) is not simple, if it can be done at all (2hu can manipulate fate… and cdda has no LCK stat)
    
Thus, translating the characters into cdda is going to be a nerf more often than not.  At the same time this has to be done in such a way each 2hu feels stronger than the average human, and is able to feel stronger with in-game progression, while having some depth in how to play, so to speak.  Some reference points about how to do this are explained below


### Species

The initial component for a 2hu's power is her species.  In Touhou there is a large number of species, each 2hu being her own is a good estimate.  This would be the basis of a 2hu's raw stats, and may add extra abilities:
* Youkai: (more of a Genus, or even Family) would gain or lose no raw stats by itself, so this is more of a tag for gameplay purposes
* Human: the standard
* Gyokuto: -STR, +AGI +PER, MANA would cap lower than a human's
* Vampire: Youkai subspecies, increased stats, lots of weaknesses (passives), can do fun vampire stuff like turn into a bat and suck blood (actives), etc


### Character background

The second component is each character's background data.  This is mostly if not fully based on the canon (games + written works) for consistency.  This tweaks the previous layer: 
* Kaenbyou (species Youkai, subspecies Kasha): +AGI due being a feline youkai cosplaying as a human by changing forms (active), and smells like corpses (^)
* Sakuya (human, mysterious): her ability passively grants +AGI.  She is also perfect and elegant (^), dislikes being around humans (^)
* Youmu (half-human half-ghost): -MANA because she's melee/sword oriented, -STR because she's small.  Fully centered around her ability (^).  She also should have below-average INT, but that's mean
* Mokou (former human, Person of Hourai): +MANA and plenty of experience in virtually every field of due living for so long; otherwise average stats due the elixir (^).  She literally cannot die, and has been tired of being alive for the last… 800 years or so (^)
* Udonge (Gyokuto): increased military-oriented skills due being an elite soldier of the Lunarian Defense Force
* Remi (Vampire): *very* strong, even by vampire standards (^), somewhat childish (^)
    
This is the first place where decisions have to be made: every (^) indicates traits that cannot be directly translated into numbers, or that cannot be done in a "fun" way for the player (maxing stats isn't fun).  Some traits, like Youmu being the archetype swordswoman fighter, can be done under the normal cdda modding framework relatively easy.  Others like Mokou not dying or Remi being overpowered are complex to balance.  Added to this layer is the speculation component, which **is** encouraged by ZUN: can Remi just oneshot everything or she's bluffing because her personality?


### Abilities

The third layer consists of what's basically *designed* to not be translated into numbers.  A JoJo reference, if you will, abilities are an independent dimension to a 2hu's total power.  See, Sakuya may be a strong human (capable of fighting against gods and other powerful enemies, helped by the spellcard rules), but now she can also stop time

Thankfully, this is (relatively) easy to port to cdda, in the form of movement speed modifiers and stuns.  In the case of Remi however, how can fate manipulation be translated into anything?  Not only that, but each 2hu is able to use their ability as easy as they breathe, which requires to be toned down
    
Regardless of what the ability is, it's better to make them actives (i.e. spells), so the player can *use* and feel the weight in-game


### Limitations

The fourth is more of a constraint: what I can't, or don't know how to do

One example are Youkai, who naturally prey on humans, specifically their emotions (mostly by causing fear), but also their flesh (perhaps because that's scary).  Thus, applying the `PSYCHOPATH` and `CANNIBAL` mutations is the closest approximation, but not the correct one to make: Youkai should get no bonuses nor demerits from eating human flesh, while getting small demerits *when not* eating human flesh

A second example is Youmu having her phantom half floating around all the time (or even to materialize it as a clone, for a short time), which would be interesting to manage, like duplicate her attacks, or enable new abilities.  While monsters can now replicate spells, their AI is kind of... underwhelming to allow Youmu's phantom half as a "true pet"

Some features, like those examples, are thus present but unfinished


## Combat

The standard combat scenario is when the PC fights a group of enemies over a very short period of time (1 - 5 ingame min).  After that, the player reconsiders if they want to continue, or go away.  Yet in cdda it is the pain mechanic, not HP, what soft-locks players from reentering combat: pain slows the PC down and makes it prone to fail attacks and dodges, which quickly results in a spiral of avatar death
    
Pain is thus, the first element players have to deal with during and after combat.  The mod tries to be balanced around the idea of enabling the different roles/fantasies (2hus and some TH setting) without getting too far away from basic cdda combat.  In other words, the answer to the question of "How would your [insert your favorite Touhou] survive during the apocalypse?".  A major component of this are spells


### Spells

Unlike Magiclysm, where players are able to build the PCs as they want, 2hus already are already fulfill different archetypes.  This means that, when picking Sakuya, the PC automatically knows spells related to time manipulation and traits related to Sakuya's background, but it also locks their spells to that character in order to "be" Sakuya.  Thus, this is a deliberate design choice
    
Another difference is mana recovery time, which is increased x4 - x12.  This enables a PC who can exit the combat with relatively minor wounds to keep going after a short recovery, which encourages the player to play more risky.  Additionally, I think it feels more lore accurate, and more fun


#### The XP system

For me, how the XP system for spells works is less than optimal.  Basically, the PC has to cast spells, **repeatedly**, in order to level up and increase its numbers.  However, this process is **very** repetitive, boring, takes a long time, and allows little customization.  This result are three different outcomes for virtually all spells:
1. The spell starts weak, and becomes strong
2. The spell starts strong, and becomes slightly stronger
3. The spell is at a fixed level (no scaling)


#### Goodbye, XP system

As of the last few experimental updates (and hopefully for 0.I), `math` can now be used in some fields that support number values.  This is a **huge** change regarding modding (you probably have felt it if you play Magiclysm or Xedra Evolved), as this allows not just pulling values from elsewhere, but also combine them in mathematical expressions and formulas.  I cannot put in words the amount of depth this enables

After realizing this could be done I immediately updated **all** character spells to scale with their skill instead of XP.  I believe this is a much more balanced **and** impactful way for the player to control their character's growth, given skills are mostly linked to character progression itself, instead of forcing them to grind for specific spells or schools (the latter doesn't really apply to this mod)

I do realize a few shortcomings, which nonetheless are smaller in comparison to the drawbacks of normal spell leveling

First, which skills to use for each character.  Given characters have different starting stats, a single skill cannot be used as standard for all characters (except `dodge`).  This is also a positive, as they're intended to have different playstyles (which wouldn't be the case by using `dodge` and forcing everyone to go melee everything)

Second, how skill leveling is handled by cdda.  Very straightforward for combat-oriented skills: go fight something.  Others level by performing different activities, which yeah it's how cdda is played, no issues here.  You can also read to increase them, no objections here either.  The problem lies in how much one can train say, dodge to 10, vs computers to 10, if it's even possible under "normal" circumstances, which will result in say, Aya having it easier to max her power relative to Utsuho
Third, it kinda railroads characters into specific playstyles.  In my defense, if you pick a guns-oriented 2hu you should expect to cast less spells than average


#### Spell "balance"

The old system (pre 0.9.6.1) relied on slowly improving spells by leveling them up individually, starting around 50 - 100% HP of the average zombie for dmg-type spells, capping at x2 - x3 that amount, depending if it's AoE or ST, with the ability to cast ~6 or slightly more spells per fight.  These two assumptions translated into the ability to clear a group of 3 - 6 enemies then rest and continue, or dispatch that number of enemies from a larger group, and take the rest with melee

The new system mostly ports the same numbers over, starting at base skill level (adjusted per character), and reaching the old cap at around +8 skill level.  This effectively means that if the player is able to reach skill +9 and +10, they will be rewarded with more numbers.  Ideally this should be more "stuff", but I plan to get there at some point...


#### Enter: Effect on Condition

A fundamental problem with any given system focused on a "flat", simplified view of things, based on only or mostly in numbers, is powercreep.  Why bother casting a weak spell, when it's objectively inferior?  The keyword there is "objectively", enabling three different approaches to alleviate, or even nullify powercreep:

1. Add secondary utility/features to a damage spell.  This is the simplest but also the most boring way to do it
2. Design spells with utility/features alongside damage.  Trickier to do but more rewarding, as each component is independent from the other, the spell doesn't have to be strong for the it to be useful
3. Design spells that add an extra layer of interaction.  The hardest to do but the best one for the player, as these interactions can stack upon each other in unexpected ways

Obviously this is much easier to say than to do.  There is a very limited amount of variation that can be done for 1.; 2. and 3. are limited by what each 2hu is able to do; 3. is further limited by how much stuff can be added via json (plus my own creativity)...

Like a war criminal once said, times change.  Thanks to the introduction of Effect on Conditions (EOCs), which is a framework similar to the old triggers I loved from StarCraft (which I also love), a pseudo-script can be used via json to **greatly** (º) modify how the game behaves.

```md
(º) greatly is an understatment

(rambling ON)
The trigger system allowed stuff close to total conversions in the SC engine, which if you're not aware is *extremely*
archaic to work with. Some funny example is that there was this map, "The Thing", a very rudimentary yet equally hilarious
predecesor to Amongus. A more relevant case is when someone made the map "Aeon of Strife".  Someone else remade that,
in the amazingly powerful Warcraft implementation of triggers, creating DotA. This exploded with League of Legends, back
in S2 - S3.  If you ever had fun in LoL, you can thank the maker(s?) of AoS, and the people implementing triggers in
SC's map editor. There are many, many other examples of custom maps made in either of those games, which ended up creating
not just gamemodes, but entire games, and in some cases genres, started from just allowing the players to fuck around and
find out. I believe EOCs + cdda's modular framework has the potential to trigger (intended) another renaissance of
creativity, and why making them as accesible as possible to the average player is a must to expand the game's influence
and impact beyond it's (hypothetical) maximum potential as a roguelike alone
(rambling OFF)
```

#### EOCs and you (me) (who?): part 2

Combining spells, `math` + EOCs is just a completely different paradigm. Before you had direct target dmg, spawn item, summon monster, change terrain, and move me there spells.  Now any of these can have different results according to certain pre-stablished parameters and/or contexts

We're talking about stuff that seems obvious a given 2hu would be able to do, but was just couldn't be done, such as 
1. Iku recharging batteries, 
2. Tenko summoning a crashing keystone from the sky *only* when she's outdoors, 
3. Mokou's melee combat style having actual fire attacks, 
4. Utsuho requiring her third rod to control her abilities, 
5. Sakuya freezing knifes in space to use them as platforms, 
6. Seiga being a necromancer

We're talking about stuff that I haven't seen anywhere else (in cdda), like 
1. spells dealing different effects on different targets, or in the same target depending if it's *currently* debuffed, 
2. delayed spells, delayed spells at a specific location external to the player, 
3. dealing double damage if the target is undead or reduced damage if it's an extradimensional entity,
4. monsters copying specific spells *you* use, *after* you use them, and *only* a specific number of times, 
5. using monsters you summon as another resource for follow up spells,
6. martial arts techniques using spells on the current target *without* the need to select it mid-combat,
7. the same character having different abilities depending on their current stance, 
8. ***parrying*** at will, 
9. the same spell dealing two different types of damage according to your currently equipped weapon, 
10. a health-draining ability instead hurting the player when using it on something with toxic constitution

We're talking about having *corpse explosion* now, which is very simple in principle but yeah, try to mod that in your game of choice *without* the ability to program hardcode, and tell me how it goes


#### EOCs: Revolutions

Yeah they're pretty cool and stuff that wasn't possible now is

If you mod you *really* should learn how to use them

If you already do, then I'm eager to receive feedback in how to improve my stuff, how to implement stuff I want to but haven't yet, etc.

If you're a player or 2hu fan and think there's something that should be added or changed about your favorite character, tell me and I'll try to add it in some form


## Story (Updated 2024-01-05)

### The story so far

(I haven't played the end-game of C:DDA, probably not even the mid-game, so I'm at a crossroads where I don't want to spoil myself, but also I don't want to misunderstand the story and ruin the vision I have for the mod and put anachronistic stuff)
The Cataclysm happened and everything went to shit, except for Gensokyo.  However, Yukari (and few independent factions such as the Lunarians) knew about it and planned things accordingly


#### The Yukari-side

In the case of Yukari, it's implied she warned faction leaders and generic youkai to either escape Gensokyo, or made them prepare for the Barrier deactivation, *some* time before the Cataclysm.  The faction leaders acted accordingly, without knowing specifics.  In reality, the message was no warning, as 2hus in general would have zero issues surviving outside the Barrier, the real objective was to make them *disperse* after it happened.  The Cataclysm causing the very rapid collapse of society, and the subsequent inability to keep science and technology, would allow the existence of the supernatural and unknown once more.  The reason she exhorted everyone just before the Cataclysm, was to deceive them: make it sound as if it was outside her control, to facilitate them turn feral once again.  At the same time, this façade would give false data to the Lunar Capital (in other words, cause X event instead of Y event which would benefiting Yukari/former Gensokyo inhabitants instead of the Lunarians, regardless of the former's new allegiances)


#### The Lunarian-side

The Lunarians knew about the Blob, but they chosed to not act immediately due what could be better described as 'bureaucracy' and 'still being pissed at humans' in human terms.  Instead, their plan was to let the everyone down in Earth run rampant, then show up later, cleanse everything and take Earth (including any survivors), 'take' here being ambiguous.  They deployed a first wave (the LDC present) as a reconnaissance team.  The second, real invading force would be deployed two-three seasons after the PC making contact with the first wave.  The second wave would go from hostile to neutral depending on the PC's final diplomatic status with the first wave.  All of the LDC forces would retreat some point, shortly before the third, purifying wave.  This happening would be equivalent to a bad ending for the PC


#### The Hecatia-side

Hecatia is mysteriously silent while all of this is happening.  Some Hell factions showed up to wreak havoc after the Cataclysm, without any concrete objective other than to take advantage of the situation.  Bizarrely enough, Hecatia-aligned forces randomly show to protect humans from whatever tries to kill them


#### Reimu and Marisa?

I have no idea how/where Reimu and Marisa would go.  Completely removing them from the picture would imply this is happening some decades after the events from the mainline games, where both are out of comission or protected by Yukari/SDM/their closest friends.  Making them playable characters would be somewhat boring (for me, not for the player), not to mention I feel story potential will be lost if they're playable, instead of NPCs


## Random stuff that occurs to me when I'm inspired

### Lunar Weapons

All Lunar weapons are made from extremely high technology relative to human tech, not excluding actual magical components.  As the Moon is expected to be a peaceful land free of death, some questions immediately arise: What were the Lunarians preparing against?  Why do they need such advanced firepower?  Why are they bringing such advanced firepower here on Earth?
Their firearm tech can be categorized into tiers:
* Tier 1: based on (old) human weaponry and blueprints, remade with Lunarian technology.  Basically amazingly improved versions of what would otherwise be obsolete human weapons, that end up being miles better than modern human counterparts.  Examples: Service rifle, Service smg (?)
* Tier 1.5: sequential iterations of tier 1 weapons, each time less compatible with human specs (like gunmods, tools) but still fully compatible with human handling (after all, these are designed for Gyokuto).  The truly outlandish and alien stuff starts here.  Examples: Service handgun (Udonge's rabbit-eared handgun)
* Tier 2: Weaponized Lunarian tech.  These use tier 1 and 1.5 models as 'containers', retaining a gun-like feeling.  While they can be handled by humans, much of their functionality and potential is lost: think of finding an assembled quantum PC and using the processor to cook eggs.  Asking a Gyokuto to show how to use them is the only way to use a fraction of their potential.  Examples: Time warp rifle (no projectile, instead clips the space where the aim is at where the trigger is pulled).  Around half of the anti-horror weaponry such as the anti-shoggoth 'caltrop gun', the totally not Yithian lightning gun, etc. go here
* Tier 3: True Lunarian tech.  The "indistinguishable from magic" category.  Humans can use, in the same vein as finding an assembled quantum supercomputer and disassembling it to use as building material.  Examples: Anti-impurity mines, singularity storage, the other half of the anti-horror weaponry.
* Tier 4: Peak Lunarian tech (unused).  Beyond human comprehension stuff.  Similar as the previous tier, except this cannot be shown ingame due their effects, such as shooting 'reality crashing' 'bullets'.  Examples: turning the universe *into* a simulation, deleting or creating concepts, trans-dimensional equivalency.


### Disorganized misc stuff

* Two battle types: 'world' combat (the existing one) and 'spellcard duels'
    * Spellcard duels would be similar to how they're in the games/lore: use of large, fancy declared spells to dodge and catch the opponent on your danmaku pattern
    * A new 'instance' for the spellcard duel would have to be created, where everything (except story items) is consumed/destroyed/moved/affected as normal, with the exception there's no 'death' by reaching 0 HP, and after the duel full health and half mana are restored to both sides
    * Spellcard duels would happen when meeting/talking/confronting another 2hu, with the rules automatically triggered by specific dialogue options (such as, the more you piss them off the harder the duel is).  This is obviously a complex task so it's more of a long term goal
    * Several win conditions are possible: health reaching 0, race mode, gain X of certain item, not going OOM, time, etc.
    * There is a story reason why the spellcard rules are now applying outside Gensokyo (spoilers)
        * "We are definitely not in Gensokyo. Why are the rules still applying?"
Currently possible by saving the character and NPC's conditions as variables before the combat, using the `PREVENT_DEATH` event, etc.  Danmaku is still probably not possible, or incredible clunky to implement

* Reisen Alter (heavily based on KKHTA) shows up as hostile NPC when playing any SDM member or any Gyokuto:
    * She would be extremely difficult to fight because she's there to kill, not just fight, the PC.  Normally, she would win 90-95% of cases by using underhanded tactics over the course of the fight (not by granting her immediate victory but by giving her more and more advantage until the player can't keep up).  At some point she would try to deal the killing blow, but the spellcard rules would unexpectedly be active, so she exchanges some dialogue and runs away
        * This would be the only, or the second only time the spellcard rules activate outside of normal conditions
    * She would show up a second time, and do something that implicitly tells the player she overcame the rules, like killing/severely injuring someone during a spellcard duel between two different people, so the player understands they CAN die this time
        * If the player wins, she runs away again

* Yorihime shows up using a patch
    * Not related to Reisen Alter, it would be an unrelated teaser/bait

* Non-humanoid (placeholder) tech: 
    * Yithian: rusted/opaque metal, flat beams and bars, look like faraday cages turn into objects
    * Mi-go: tangible and intangible (looks, but isn't magic)
    * Elder Thing tech: organic/living but isn't disgusting/gory, more like bizarre (Geiger-like?)
    * Shoggoth tech: consists of their modified protoplasm, disgusting, possibly incompatible due physiology(mechanistic)/ergonomics


### Quest ideas
    
* Find random items with messages or signs the PC can recognized (without examining the object!).  Example: Sakuya finding Reimu's discarded ofuda, which enables the quest "Find the Shrine Maiden"
* Find random items that are being tracked by more than one faction.  Example: McGuffin that the LDC and Tengu are interested in, the player has to decide which faction they help, with different consequences
    * If the PC has some connection with either faction, they may get additional benefits by siding with them
    * Additionally, the PC can choose to steal the object, ignore it, or let them fight for it
* Visiting reverse-spirited away locations.  Example: the PC was traveling between cities and sees the Hakurei shrine, goes to visit finds a NPC Sanae
    * This would allow the player to know the 'Sanae' side of the story, potentially opening several other quests
* Meeting a NPC that was just fighting "something".  Example: the PC was exploring a city and meets an NPC Sanae who is finishing a previously unseen enemy.  Sanae stops the PC, exchanges some dialogue saying "these things did not exist in Gensokyo, nor the Outside World.  Where are they coming from?"
    * This would enable the previously unseen enemy to start spawning
    * The unseen enemy are linked to the activity of different factions, for example a horror to the LDC


## Glossary
* Ability: In TH Project each character has a special "ability", which according to the wiki is better translated as "capable of". It can be straightforward like 
* Active: from a gameplay standpoint, any ability or special action the player has to trigger to have an effect
* AoE: area of effect, splash, area effect
* dot (DoT): damage over time
* Gyokuto: moon rabbit
* Passive: from a gameplay standpoint, any ability or trait that doesn't require player action
* PC: player character or avatar
* ST: single target
* Stats: cdda's four main stats (AGIlity/dexterity, INTelligence, PERception, STRength), plus any character values that can be directly modified such as movement speed, armor, etc.  MANA should be self-explanatory, plus any magic capabilities of the caster
* Youkai: the Japanese term for "apparition", basically any supernatural entity that feeds from negative human emotions, usually fear.  Somewhat overlaps with entities belonging to urban legends

