# Cataclysm-DDA-Touhou-Mod
This is a fork of Taberone's [Touhou Professions](https://github.com/Taberone/Cataclysm-DDA-Touhou-Mod) mod.

**This mod goes in /data/mods**.  Last updated for game version: 2022-12-24 experimental.

To pick any of the characters, you have to select the **Touhou Mod** scenario when creating a new character.


## About the mod
This mod is intended to be some sort of Touhou-flavored conversion for CDDA, inspired by the following questions:
  1) How would your [insert your favorite Touhou] survive during the apocalypse?
  2) What would the Sages do if there was an Outside World "End of the World" scenario, stacked several times upon itself, simultaneously?
  3) What would each faction (Lunarians, Tengu, Underground youkai, SDM, etc.) do, after realizing that there's no status quo anymore?

and more, but those are the most important now.

It greatly expands upon the original mod, primarily by further developing each existing character with custom spells, abilities, clothing, martial arts, special items, etc.

It also adds a lot of stuff from the Touhou series, going from the relatively simple stuff like generic youkai enemies, to more obscure tidbits of lore such as extinct fauna, to stuff that would be fun to have expanding Touhou lore on a CDDA setting, like forgotten firearms and magical items.


## Contents
The mods includes so far:
- [13 characters](#characters) from several Touhou games and works, each with new spells and abilities
- [New mechanics](#new-mechanics)
- [New weapons](#new-weapons), including new ammo types, magazines, gunmods, etc.
- New monsters
  - [Extinct fauna](#extinct-fauna), to hunt or be hunted by
  - [Youkai](#youkai), to be haunted by
- [Custom clothing](#clothing)
- [New food and recipes](#food-and-recipes)
- [New weather](#weather)
and more minor additions or changes

Additionally, there's the
- [Small planned features](#wip), and
- [Big planned features](#milestones)

Sadly, there's also the
- [Known bugs](#known-bugs)


### Characters
* **Aya Shameimaru:** Uses wind spells.  The earnest, most pure, fastest Tengu reporter is always on the look of interesting news.
* **Fujiwara no Mokou:** Uses fire spells.  Fights with a custom martial art that increases her damage over time, while also making her more vulnerable.  Death has no meaning to her.
* **Hong Meiling:** Uses qi.  Fights using a special form of Tai Chi focused on defense, with windows of opportunity after blocking attacks.  Nap time can't come soon enough.
* **Iku Nagae:** Uses electric spells.  Fights by whipping and shocking enemies to death, while dancing on the battlefield.
* **Reisen:** Uses a mysterious ability.  Recently conscripted into the Lunarian Defence Corps, fights aided by her service Lunarian rifle and basic military training.  She's trying her best!
* **Reisen Udongein Inaba:** Uses wavelength manipulation.  Former member of the Elite Lunarian Defence Corps, proficient with firearms with a touch of medicine at the side.  Starts with a Lunarian tech pistol.
* **Remilia Scarlet:** Uses Red Magic.  The charismatic vampire leader of the Scarlet Devil Mansion, nothing can oppose her when she's serious.
* **Rin Kaenbyou :** Uses destructive fire spells and calls forth Vengeful spirits to assist her in battle.  Collects corpses with her wooden wheelbarrow.
* **Sakuya Izayoi:** Uses time manipulation.  Fights by elegantly throwing knives, then cleaning it all perfectly afterwards.
* **Seiga Kaku:** Uses wicked spells and can pass through walls.  Fights without care for human life or norms, all while forcing "collateral damage" victims back to life to fight for her.
* **Tenshi Hinanawi:** Uses earth spells.  Very resistant to physical damage, very susceptible to boredom, she wields the Sword of Hisou and fights with a martial art focused on critical attacks over anything else.
* **Utsuho Reiuji:** Uses nuclear spells.  She's half Hell Raven, half sun god, half pet, wholly awesome.
* **Youmu Konpaku:** Uses sword techniques.  Also trained in gardening, she wields Roukanken and Hakurouken, two Youkai katana capable of cutting anything!


### New mechanics
* Auras.  Sakuya and Udongein have "aura" type abilities, each with different passive effects as long as they're active.  These are toggled by casting specific spells.
* Blood thirst.  Remi now has to consume blood (or human flesh, with less effectiveness) in any shape or form, in order to keep the thirst at bay.
* Immortality (for Mokou).  She resurrects after dying, immediately restoring her body.  She can die as many times as she wants, but there's a soft cap relative to how many times she has died in a period of time, plus a small-ish pain debuff that ramps up, to discourage savescumming.
* Impurity (WIP).  Currently a dummy mechanic, it naturally increases over time and also by consuming "impure" stuff (which is everything edible so far).  Has no effect, except for Reisen who starts with the LUNARDIET trait and loses it after acquiring enough impurity, making her tolerant to Earthly foodstuff.
* Wings.  Aya, Remi and Utsuho can now "fly" (read: hover) over over ledges and open spaces, consuming stamina until they're tired enough.  This is done by activating a mutation (View/active mutations key).
* Youkai form toggle.  Kaenbyou and Remi can now switch between their human and youkai forms, each having different effects.  This is done by activating a mutation (View/active mutations key).


### New weapons
* Prototype weapons.  Firearms that were never sold, or even fully developed, and were forgotten over time but are very interesting anyways: ARES FMG, CEAM Mòdele 1, IDW, TKB-022P and TKB-022PM No 2.
* Old weapons.  Firearms that became obsolete (?): Kar98k, Pieper M1893, SIG 550 and 550-1, Spanish Model 1983, StG 44, SVD-63.
* Cool weapons.  Because why not, other than not being intended for civilian use?: M76 Zastava, OTs-48 and OTs-48K, PGM Hécate II, SR-3MP, VSS Vintorez, Walther WA 2000.
* MIB weapons.  MIB agents are equipped with the Standard Series Sidearm, Series 7 de-Scatterer and Series 4 re-Diffuser, plus their Neuralysers.
* Misc.  The humble Thompson Contender.


### New monsters

#### Extinct fauna
* Amphibians: Eryops, Pederpes, Platyoposaurus, Prionosuchus.
* Arthropods: Aegirocassis, Anomalocaris, Arthropleura, Chasmataspis, Eusarcana, Hurdia, Jaekelopterus, Megalograptus, Meganeura, Opabinia, Pambdelurion, Parastylonurus, Sidneyia.
* Birds: Dodo, Ectopistes, Icadyptes, Moa.
* Fish: Coccosteus, Dipterus, Dunkleosteus, Holoptychius, lampreys (not actually extinct), Megamastax, Saurichthys.
* Mammals: Amphicyon, Andrewsarchus, Castoroides, Daedon, Glossotherium, Glyptodont, Herpetotherium, Megatherium, Pakicetus, Taeniolabis, Thylacine.
* Mollusks: Agoniatites, Cleoniceras, Endoceras, Michelinoceras, Paracoroniceras, Parapuzosia.
* Reptiles: Anatosuchus, Carnufex, Hesperosuchus, Ichthyosaurus, Plesiosaurus, Scutosaurus, Smilosuchus, Weigeltisaurus.
* Stem-mammals: Cotylorhynchus, Dimetrodon, Lystrosaurus.
* Theriodontia: Inostrancevia, Moschorhinus, Nochnitsa, Pristerognathus, Viatkogorgon.


#### Youkai
* Cryptids and urban legends: Chupacabra, Enfield horror, Jackalope, nightcrawler, Mongolian death worm, Sasquatch, skinwalkers, squonk, Yeti, MIBs.
* Ghosts: three different female ghosts.
* Oni: lesser oni, generic oni, humanoid oni.
* Tsukumogami: animated dolls, chairs.
* Youkai: Chupacabra, Beast of Gévaudan, jinmenken, kunekune.


### Clothing
* Every playable character has their own custom set of clothing.  Not all are just cosmetics.
* Generic clothing includes so far: bloomers, cheongsam dresses, Tang shirts, tai chi pants, long socks.
* Some monsters also drop wearable items.


### Food and recipes
* New kinds of meat were added: arthropod meat, bird meat, lamprey meat, and shrimplike meat.  These are harvested from the extinct fauna, including chickends dropping bird meat.
* Vegetables: Satsumaimo (sweet potatoes).
* Each of the new items have their own basic crafting, like roasted bird meat, or boiled arthropod.
* New dishes were also developed, like chicken pie, chicken soup, or paella, among several others.


### Weather
* Scarlet mist and fog.  Should happen randomly, and reduce sun intensity.


## WIP
Relatively easy things to add, not in order:
* Professions: Nitori and Yamame are still not playable.  I want to add Kasen and maybe Flandre too.
* Monsters: a lot more.  Fairies, rocs, banshees, more tsukumogami, etc.
* Events: Night parade and Silence hour.  Future weather/events that happen randomly.
* Items: 16 new items that grant various special abilities or passive bonuses were already designed but not fully implemented (see Known Bugs).
* Locations: Power spots, basically small zones of interest for the player to explore/search, where forgotten items reappear and certain monsters gather, depending on the spot type or surroundings.  A small Shinto-style shrine has been added, but it's unfinished.
* Visual effects: Can it be done with fields? For example, when Youmu dashes, cherry petals appear on the path.
* Vehicles: Make an engine that can use corpses as fuel.
* Balance: CDDA is a roguelike, but the mod feels RPG-ish at times.


## Milestones
Relatively hard or complex things to add, not in order:
* Even MORE Touhou characters.
* NPCs: generic and important, this includes quests and some story.
* Quests: to give short-medium term goals for the player.
* Story: an overarching story.
* Locations: Reverse-spirited away places from Gensokyo, like an abandoned Hakurei shrine.  These would go from small dungeons (say, a power spot or a haunted house), to city-sized zones (say, an underground city).
* True modding: things that seems currently hardcoded, like new damage types, new resources, spell shapes, more mechanics, etc.
* A species system for both the characters and youkai.  For example, species-restricted traits like flying, percentual resistance (or weakness) to different kinds of damage, etc.
* Spellcards?


## Known bugs
* Mokou's resurrection moves her 3 tiles to the right, every time she revives. I have no idea how or why this happens; this is potentially very very bad for the player.
* Youkai and ancient fauna presence may be (slightly) higher than intended, may not.
* Seems enchantments are broken: anything inside the `passive_effects` field from items is not working properly (e.g. a mutation is applied but the bonus from that mutation aren't).  This seems to be an issue with base CDDA.


## Spoilers

<details>
    <summary>Spoiler (1/2)</summary>
    Current profession descriptions give a initial glimpse of an underlying story. So far, a tl;dr is that certain mastermind youkai is related in some way or another to the Cataclysm, so she played her hand accordingly.  Each character would meet Gensokyan NPCs, or find items, structures or clues in the world, and continue the story from that point.  This is a long term goal after I finish adding and fixing most of the "core" mod.
    <details>
        <summary>Spoiler (2/2)</summary>
        Certain 2hu fan work matches the first D of CDDA almost perfectly
            </details>
</details>
