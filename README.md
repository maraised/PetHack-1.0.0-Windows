Introducing PetHack, a NetHack variant for pet lovers!



PREMISE \& NOTES

* PetHack is a simple variant geared towards pet lovers. It makes it easier to obtain and manage pets while still having the classic NetHack feel.
* PetHack is based on NetHack 5.0.0. This will likely be the only release of PetHack unless there are bugs. The goal was not to make extreme changes, but rather to upgrade and serve a specific playstyle.
* There is also an Android port of PetHack! It is based on JodiJodington and gurr’s Android ports for NetHack:
* All tilesets that are compatible with NetHack 5.0.0 should be compatible with PetHack! 
* I am very, *very* new to coding and GitHub. If there are any issues with the game or repository, please let me know and I will do my best to fix them!



CHANGELOG

* Changed Tourist role

  * They now start with 3-5 tripe rations, 3-5 scrolls of taming, a blessed spellbook of charm monster, a blessed magic whistle, a sack, a leash, and a blessed random figurine *in addition* to their original starting equipment

    * The figurine is completely random, meaning it can be any monster (not based on level/depth) while still following normal figurine generation rules
  * They now start with Basic in enchantment spells and can reach Expert
* Changed charm monster back to a level 3 spell
* If you throw an item to an intelligent pet with hands, they will catch it and equip it if applicable. They will prioritize using items you give them over other items. This idea came from FIQHack.
* Intelligent pets will now hoard healing potions even when they're healthy. Be careful to manage this properly!
* Rebalanced figurine BUC effects

  * Blessed: 100% tame
  * Uncursed: 10% tame, 70% peaceful, 20% hostile
  * Cursed: 0% tame, 10% peaceful, 90% hostile
* New store: Toy store

  * This is a shop that only sells figurines. Figurines that generate in toy stores (or shops in general) can also be of any monster regardless of the player’s level and depth. 
  * Figurine base prices now scale with the monster’s difficulty (difficulty x 50). For example, figurines of Archons will be expensive, while figurines of lichens will be cheap.

Good luck, and happy hacking!

