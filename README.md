# Cataclysm-DDA-Touhou-Mod
This is a fork of Taberone's [Touhou Professions](https://github.com/Taberone/Cataclysm-DDA-Touhou-Mod) mod.

**This mod goes in /data/mods**.  Last updated for game version: 2022-12-08 experimental.

This branch is for new additions that produce non-critical errors when running the mod.  **Read:** the contents are *technically* stable but don't expect proper functionality in-game

----

**Changelog over the master branch (0.9.3.14c):**

New characters:
* (WIP) Yamame. Currently has clothing and traits, including changing into her (partial) youkai form.  I'm working on her spells, so she's not playable yet


New items:
* Magical items: based on different Touhou characters abilities and skills
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
    * Wind priesess charm: grants you random positive buffs
    * (WIP) Gap generator: would create gaps to shorten distances
* Monster drops: MIB now may drop their Neuralysers and Standard Series pistol, rifle or smg.  Also their fancy glasses
* Fluff: Aya has her reporter stuff


New locations:
* Shrine: a simple Shinto-style shrine.  Magical items should spawn here, for the moment being.
* (WIP) UFO crash


New mechanics:
* Blood thirst.  Remi now has to eat blood (or human flesh, with less effectiveness) in any shape or form, in order to keep the thirst at bay
* Impurity (WIP).  Currently a dummy mechanic, it naturally increases over time and also by consuming "impure" stuff (which is everything edible so far).  Has no effect, except for Reisen who starts with the LUNARDIET trait and loses it after acquiring enough impurity
* Kaenbyou can now toggle between her human or youkai forms.  Cat form is smaller, slightly more nimble, and less loud, but carries less weight and deals reduced melee damage
* Mokou is now immortal.  She resurrects after dying, immediately restoring her body.  She can die as many times as she wants, but there's a soft cap relative to how many times she has died in a period of time, plus a small-ish pain debuff that ramps up, to discourage savescumming


New monsters:
* Jackalope: a horned hare
* Skinwalkers: various (in)famous, dangerous wilderness beasts that mimmick humans, with varying degrees of intelligence and cunning
* Female ghosts: banshee, La Llorona, white lady
* Squonk: a warty entity that cries all the time
* Tsukumogami: of the armchair and table variety


New spells:
* Aya, Remi and Utsuho now have "wings". While active (View/active mutations key), it enables them to fly over ledges and open spaces, consuming stamina until they're tired enough
* Sakuya has a new spell, "Maid's secret", which is a toggle-able aura that increases her movement speed and stamina regeneration as long as she is focused.  Becoming tired or hostiles getting close automatically toggle it off
* Udonge's Wavelength manipulation spells were changed into "auras", toggled ON or OFF by casting each spell.  Additionally, there's a new wavelength manipulation: Mental fortitude, which renders her immune to mental debuffs as long as it's active


New weather:
* Scarlet mist and fog. Should happen randomly, and reduce sun intensity
* (WIP) Night parade and Silence hour: random events


Other changes:
* Mokou is now immune to smoke
* Lunar weapons were changed (again), now automatically regen ammo over time, and can't be unloaded or reloaded
* Increased youkai presence around the region, and fixed the spawn chance (it was either too low or too high)


Fixes and minor changes:
* Temporary fix for dashes over open air not working (cdda issues #53511 and #53532).
* Fixed Tenko's keystone dismissal not dismissing pillar keystones
* Fixed Tenko's keystone pillar not being castable on top of enemies
* Reduced loudness of Lunar weapons
* Fixed and tweaked some character mutations values. Also fixed a bug where mutation stat modifiers increased cost while on character selection
* MIB now actually shoot and die properly (heh)
* Changed how previous buffs from spells work (instead of creating wearable item -> enchantment, they now grant a visible buff -> enchantment)
* Touhou scenario now starts at day 1
* Skinwalkers, banshee and White Lady demoralizing spell components are now working properly


Known bugs:
* Mokou's resurrection moves her 3 tiles to the right, every time she revives. I have no idea how or why this happens; this is potentially very very bad for the player
* The increased youkai presence may be higher than intended
