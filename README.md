# Cataclysm-DDA-Touhou-Mod
This is a fork of Taberone's [Touhou Professions](https://github.com/Taberone/Cataclysm-DDA-Touhou-Mod) mod.

**This mod goes in /data/mods**.  Last updated for game version: 2022-10-14 experimental.

This branch is for new additions that produce non-critical errors when running the mod.  **Read:** the contents are *technically* stable but don't expect proper functionality in-game

----

**Changelog over the master branch (0.9.3.14c):**

New characters:
* (WIP) Yamame. Currently has clothing and traits, but she's missing spells so she's not playable yet


New items:
* Magical items: based on different Touhou characters abilities and skills.
    * Autumn melancholy: reduces hunger rate
    * Cricket pin: grants you insect manipulation
    * Death coin: grants you distance manipulation
    * Esper cloak: improves magic abilities
    * Fan of death: grants you death (life) manipulation
    * Lampad torch: drives you insane
    * Lucky charm: makes you lucky!
    * Mini hakkero replica (electric): cooks, shoots lasers and works as a torch
    * Oni gourd: capable of turning you alcoholic
    * Posessed trumpet: randomly influences morale and stats
    * Prankster shovel: instantly digs pit traps
    * Sphere of darkness: makes you bump into objects
    * Spider charm: grants you disease immunity
    * Strong ice: makes you the strongest
    * Sunflower pin: spams sunflowers
    * Wind priesess charm: grants you positive buffs
    * (WIP) Gap generator: would create gaps to shorten distances


New locations:
* Shrine: a simple Shinto-style shrine.  Magical items should spawn here, for the moment being.


New monsters:
* Jackalope: a horned hare
* Skinwalkers: various (in)famous, dangerous wilderness beasts that mimmick humans, with varying degrees of intelligence and cunning
* Female ghosts: banshee, La Llorona, white lady
* Squonk: a warty entity that cries all the time
* Tsukumogami: of the armchair and table variety


New spells:
* Aya, Remi and Utsuho now have "wings". While active (View/active mutations key), it enables them to fly over ledges and open spaces, consuming stamina until they're tired enough
* Udonge has another Wavelength manipulation spell: Mental fortitude, which renders her immune to mental debuffs


New weather:
* Scarlet mist and fog. Should happen randomly, and reduce sun intensity
* (WIP) Night parade and Silence hour: random events


Other changes:
* Lunar weapons were changed (again), now automatically regen ammo over time, and can't be unloaded or reloaded
* Increased youkai presence around the region, and fixed the spawn chance (it was either too low or too high)


Fixes and minor changes:
* Temporary fix for dashes over open air not working (cdda issues #53511 and #53532).
* Fixed Tenko's keystone dismissal not dismissing pillar keystones
* Fixed Tenko's keystone pillar not being castable on top of enemies
* Reduced loudness of Lunar weapons
* Fixed and tweaked some character mutations values. Also fixed a bug where mutation stat modifiers increased cost while on character selection
* MIB now actually shoot and die properly (heh)
