## **GASContent**
Repo to gather all GAS content for UE4
Note: I accept PR's for this repro, but i not longer actively seek out new content for it. Note, look for Dan's link thats the good shit.

![Beta](https://img.shields.io/badge/Gameplay%20Ability%20System-Released-green) ![API](https://img.shields.io/badge/Documentation%20-A%20lot-green)

- [Gameplay Ability System(GAS)](#gameplay-ability-system)
  - [GAS Intro](#gas-intro)
  - [GAS General Resources](#gas-general-resources)
  - [GAS Community](#gas-community)
  - [GAS Tutorials](#gas-tutorials)
  - [GAS Examples](#gas-examples)
  - [GAS Templates](#gas-templates)
  - [GAS Discussions](#gas-discussions)
  - [GAS Videos](#gas-videos)
  - [GAS Training](#gas-training)

## Gameplay Ability System

### GAS Intro
(Taken from "Gameplay Abilities and You")

#### So, what's a GameplayAbility?

Basically, they're like the abilities you have in Dota or equivalent games. You can cast a fireball, and this fireball hits a player, explodes (doing a set amount of damage), and sets everyone in the radius of the explosion on fire (doing damage over time). Meanwhile, the player who cast the fireball loses some mana and is put on cooldown.

You could use Epic's GameplayAbility plugin to do all of those things. The module is hard to wrap your head around, but once you learn how powerful they can be and how to properly make use of them, they can make your life much, much easier.

#### But why use this over rolling your own system?

GameplayAbilities can come in handy if your game is in need of a powerful skill, buff and attribute system that is both easy to extend and crazy-efficient to replicate. This can do wonders for people working on a multiplayer RPG with a lot of skills/classes or perhaps even a MOBA, but you can use this system for pretty much any game you want. The main problem is that it isn't the easiest to comprehend, quite big and may get a little in your way the further you stray too far away from this multiplayer RPG ideal, so not every game will get the same mileage out of it.

#### Well, that sounds like a dream, but where do I get it?

Well, first of all, GameplayAbilities is a code module that used to be integrated into UE4's source, but since this current version (4.15, that is, people from the future) has been moved into a separate plugin that is delivered alongside the Unreal Engine, so that it may not take away space in your games if they do not make use of the system. This system does not actually originate as a built-in engine feature, but has, in fact, been kindly left in there from the developers of Paragon and Fortnite for third parties to enjoy. Unfortunately, due to these unique circumstances, the module as a whole is quite messy, poorly (read: barely at all, your best bet are code comments and even those are only there like half the time) documented, and rarely updated and cleaned up.

It is also not 100% exposed to blueprints, partially, but not entirely, due to a lot of the system abusing a lot of engine trickery and magic to work as well as they do, so if you never worked with C++ in the context of UE4, you may want to turn back and maybe do a little tutorial on that now, because this tutorial will make for a poor first learning experience.

In other words, it is a total flippin' pain in the buttocks to wrap your head around, but that's where this guide comes in to help ya. Epic Developer Dave Ratti has an example GitHub project which goes through some basic examples to get you started, but ignores the fine lines and goes for broad strokes. The project itself has been pretty hidden, however, and (at the time) doesn't really show up on Google or any real search about the GameplayAbilities plugin, so it hasn't been as helpful as a full-fledged guide. Moreover, now that GameplayTags are properly integrated into the editor by default (a system GameplayAbilities itself uses at every corner of the way, acting as GameplayAbilities' backbone), setup has never been any easier!

With all that said, let's get started, finally.

### GAS General Resources
#### Epic's Official Documentation
* [Documentation](https://docs.unrealengine.com/en-us/Gameplay/GameplayAbilitySystem)
* [API Documentation](https://docs.unrealengine.com/en-US/API/Plugins/GameplayAbilities/index.html)
##### Epic's Action RPG Documentation
* [Action RPG](https://docs.unrealengine.com/en-us/Resources/SampleGames/ARPG)
note - You can download the learning example from the Epic Games Launcher under the Learn tab.



##### External Wiki's
* [Gameplay Abilities and you](https://nerivec.github.io/old-ue4-wiki/pages/gameplayabilities-and-you.html)
##### Slide Shows
* [Woppin's Slide Show](https://docs.google.com/presentation/d/1GeuDO2as1b12ei5OHh6jyfxczVYymXJQDBWoRLDMpOI/edit#slide=id.g38b84aa984_0_32Videos)
##### Forums
* [DamirH's Forum Post](https://forums.unrealengine.com/showthread.php?143688-Comprehensive-GameplayAbilities-Analysis-Series&p=702209)
* [KZJ's Forum Post](https://forums.unrealengine.com/community/community-content-tools-and-tutorials/110113-gameplayabilities-and-you)
##### Blogs
* [jcilla](http://jcilla.github.io/ue4/2017/05/18/intro-to-gameplay-abilities.html)
* [KaosSpectrum](https://www.thegames.dev/2019/07/25/gameplay-ability-system-creating-your-own-gameplayabilityactorinfo/)
##### User Made UML
* [Congurent's UML](https://github.com/FuzzySockets/GAS-Resources/blob/master/images/GAS-UML-WIP.jpg)
##### Q&A
* [Epic's Q&A](https://epicgames.app.box.com/s/m1egifkxv3he3u3xezb9hzbgroxyhx89)
##### Misc Lists
* [Congurent's GAS List](https://github.com/FuzzySockets/GAS-Resources)
### GAS Community
* [Unreal Slackers](http://unrealslackers.org/)
### GAS Tutorials
* [Community Tutorial by Narxim](https://github.com/Narxim/Narxim-GAS-Tutorial)
* [Tom Loomans RAGE Potion](https://www.youtube.com/watch?v=Tu5AJKNe1Ok)
* [Binding to Gameplay Attributes For UI Updates](Tutorial_Attribute_Delegates.md)

### GAS Examples
* [Dan's Knowledge and Gameplay Example](https://github.com/tranek/GASDocumentation)
* [Woppin's Code](https://github.com/michaeltchapman/MCGameplayAbilities)
* [daveratti's Code](https://github.com/daveratti/GameplayAbilitiesSample)
* [David E. Nishball](https://github.com/DavidENishball/Unreal_GameplayAbilities_FirstPerson)
* [aa1000](https://github.com/aa1000/GASTanksVsZombies)
* [KaosSpectrum's Task_RepeactAction](https://gist.github.com/KaosSpectrum/c602c6d57c315b7fa787420cfa89abfb)
* [Client side prediction with single projectile](https://github.com/roidanton/ue_gas_prediction)
* [MODriscoll's GameplayEffectExecutionCalculation Example](https://gitlab.com/MODriscoll/project-eden/blob/master/Source/EdensGarden/Private/SpecOp/Calculations/BreathDamageCalculation.cpp)
* [Gameplay Abilities Meet Behavior Trees @ Daedalic Entertainment](https://github.com/DaedalicEntertainment/ue4-orders-abilities)
* [GASShooter by Dan(tranek)](https://github.com/tranek/GASShooter)
* [fpwong](https://github.com/fpwong/FPGameplayAbilities)
* [MichaeltChapman](https://gist.github.com/michaeltchapman/e305f6468f302f52a85ca767935afb08)

### GAS Templates

### GAS Discussions
* [Dave Ratti on Weapons & RPC Batcher](https://forums.unrealengine.com/development-discussion/c-gameplay-programming/1660211-gameplay-abilities-and-weapon-firing)

### GAS Videos
* [Intro to Gameplay Abilities in Unreal Engine 4 by SabreDartStudios](https://www.youtube.com/watch?v=Ev2P6BTUxN0)
* [Sydney Unreal Meetup](https://www.youtube.com/watch?v=OyiweL2nPac)
* [AI with Behavioral Trees](https://www.unrealengine.com/en-US/events/unreal-fest-europe-2019/hero-ai---gameplay-abilities-meet-behavior-trees)

### GAS Training
* [Dan's Knowledge and Gameplay Example](https://github.com/tranek/GASDocumentation)
This is here on the list twice because it is a very extensive analysys that has a lot of information.
#### Please try to learn on your own rather than paying for videos. Ask questions in the Unreal Slackers Discord for help!
* [Introduction to Unreal Engine 4 Ability System -UE4](https://www.udemy.com/introduction-to-unreal-engine-4-ability-system/)
