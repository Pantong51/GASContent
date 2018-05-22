## **GASContent**
Repo to gather all GAS content for UE4

- [Gameplay Ability System(GAS)](#gameplay-ability-system)
  - [GAS Intro](#gas-intro)
  - [GAS General Resources](#gas-general-resources)
  - [GAS Community](#gas-community)
  - [GAS Tutorials](#gas-tutorials)
  - [GAS Examples](#gas-examples)
  - [GAS Videos](#gas-videos)

## Gameplay Ability System

### GAS Intro (Taken from "Gameplay Abilities and You")
So, what's a GameplayAbility?

Basically, they're like the abilities you have in Dota or equivalent games. You can cast a fireball, and this fireball hits a player, explodes (doing a set amount of damage), and sets everyone in the radius of the explosion on fire (doing damage over time). Meanwhile, the player who cast the fireball loses some mana and is put on cooldown.

You could use Epic's GameplayAbility plugin to do all of those things. The module is hard to wrap your head around, but once you learn how powerful they can be and how to properly make use of them, they can make your life much, much easier.

But why use this over rolling your own system?

GameplayAbilities can come in handy if your game is in need of a powerful skill, buff and attribute system that is both easy to extend and crazy-efficient to replicate. This can do wonders for people working on a multiplayer RPG with a lot of skills/classes or perhaps even a MOBA, but you can use this system for pretty much any game you want. The main problem is that it isn't the easiest to comprehend, quite big and may get a little in your way the further you stray too far away from this multiplayer RPG ideal, so not every game will get the same mileage out of it.

Well, that sounds like a dream, but where do I get it?

Well, first of all, GameplayAbilities is a code module that used to be integrated into UE4's source, but since this current version (4.15, that is, people from the future) has been moved into a separate plugin that is delivered alongside the Unreal Engine, so that it may not take away space in your games if they do not make use of the system. This system does not actually originate as a built-in engine feature, but has, in fact, been kindly left in there from the developers of Paragon and Fortnite for third parties to enjoy. Unfortunately, due to these unique circumstances, the module as a whole is quite messy, poorly (read: barely at all, your best bet are code comments and even those are only there like half the time) documented, and rarely updated and cleaned up.

It is also not 100% exposed to blueprints, partially, but not entirely, due to a lot of the system abusing a lot of engine trickery and magic to work as well as they do, so if you never worked with C++ in the context of UE4, you may want to turn back and maybe do a little tutorial on that now, because this tutorial will make for a poor first learning experience.

In other words, it is a total flippin' pain in the buttocks to wrap your head around, but that's where this guide comes in to help ya. Epic Developer Dave Ratti has an example GitHub project which goes through some basic examples to get you started, but ignores the fine lines and goes for broad strokes. The project itself has been pretty hidden, however, and (at the time) doesn't really show up on Google or any real search about the GameplayAbilities plugin, so it hasn't been as helpful as a full-fledged guide. Moreover, now that GameplayTags are properly integrated into the editor by default (a system GameplayAbilities itself uses at every corner of the way, acting as GameplayAbilities' backbone), setup has never been any easier!

With all that said, let's get started, finally.

### GAS General Resources
##### External Wiki's
* [Gameplay Abilities and you](https://wiki.unrealengine.com/GameplayAbilities_and_You)
##### Slide Shows
* [Woppin's Slide Show](https://docs.google.com/presentation/d/1GeuDO2as1b12ei5OHh6jyfxczVYymXJQDBWoRLDMpOI/edit#slide=id.g38b84aa984_0_32Videos)
##### Forums
* [DamirH's Forum Post](https://forums.unrealengine.com/showthread.php?143688-Comprehensive-GameplayAbilities-Analysis-Series&p=702209)
* [KZJ's Forum Post](https://forums.unrealengine.com/community/community-content-tools-and-tutorials/110113-gameplayabilities-and-you)
##### Blogs
* [jcilla](http://jcilla.github.io/ue4/2017/05/18/intro-to-gameplay-abilities.html)
### GAS Community
* [Unreal Slackers](http://unrealslackers.org/)
### GAS Tutorials

### GAS Examples
* [Woppin's Code](https://github.com/daveratti/GameplayAbilitiesSamplehttps://github.com/michaeltchapman/MCGameplayAbilitiesForums)
* [daveratti's Code](https://github.com/daveratti/GameplayAbilitiesSample)

### GAS Videos
* [Intro to Gameplay Abilities in Unreal Engine 4 by SabreDartStudios](https://www.youtube.com/watch?v=Ev2P6BTUxN0)

