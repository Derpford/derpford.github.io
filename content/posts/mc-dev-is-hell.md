---
title: "Minecraft Modpack Dev Is Hell"
date: 2021-09-09
draft: false
---

### So about that modpack thing

DevOps for Minecraft is absolute hell. Let me regale you with some tales of the shit I've gone through in the past day:

### Mob spawn rates are dramatically different on multiplayer servers.

I have a mod in this pack called Scape & Run: Parasites. It adds freaky biological horrors, a la the Flood. It's actually quite well designed and I like the concepts behind it, with the parasites getting stronger as they consume more biomass. However, in my singleplayer playthroughs, they never spawned in large enough quantities to be a problem early on.

In multiplayer, they spawn like *CRAZY*. Our first night was plagued by horrors. We repeatedly died to everything from infested sheep to massive poison-stinger beasts because they just *would not stop spawning*.

~~As a result, I've had to implement a whole freakin' gating mechanic via the Game Stages mod and its addons. Now I have a system where the swarm will go 40 minutes off, 20 minutes on with its spawns, starting from when you read some stained research notes that an unfortunate scientist left behind. It's nice, but it was driven almost entirely by the fact that monster spawns are wildly different in Multiplayer.~~

[EDIT] Guess what doesn't fucking work? The timer mechanic. So that's not happening anymore. Swarm still starts *after* a research book is found, though.

### Also, armor calculation bugs are a thing.

I added Armor Curve shortly before I started playing with my friends. "Why wouldn't I?" I asked myself. "It's a great mod that fixes a real problem with Minecraft's design!"

What is that problem, exactly? It's the fact that iron-to-diamond more than doubles your time to death, even though it's a much smaller jump than leather-to-iron. Ever wondered why leather feels useless compared to iron? It's because they both pale in comparison to diamond, but iron at least is *sort of* useful. Armor Curve rebalances this with diminishing returns--full leather armor provides about 50% protection now, while diamond sits around the same level it used to be.

There's just one problem: TechGuns has its own armor system. And it applies *multiple* armor values to each attack--which are, apparently, overridden by Armor Curve's new calculations. So, effectively, the TechGuns armor applies way more armor than it should.

This would be sort of okay for the players--the TG armor is just generally more powerful thanks to its movement, knockback, and mining speed bonuses--but it turns out many of TechGuns' mobs spawn *equipped* with that armor. Which makes them godawful to fight, especially before you've gotten access to guns.

So I had to turn off the armor curve system for all non-player mobs. Because, frankly, it was absurd. Seven or eight sword swings to deal with *one* armored zombie, and more than one was a death sentence, especially if they had any kind of gun. I don't *like* that. I shouldn't have to drastically change the mechanics for all monsters to make them bearable. But the alternative is having to dig into Java, which brings me to one of the root issues...

### Development on mods is inherently slow.

This is not a complaint against mod developers. They have their hands full. Most of them are dealing with things IRL that are more important than modding, and that's okay. Development takes time and effort, time and effort that we don't always have, and that's okay. In an ideal world, we'd have the freedom to spend that time however we choose, instead of having to spend so much of it on survival--but we do not live in an ideal world, yet.

The downside of this is that bugs regularly get left open for months or years. It's often easier for me to simply swap a mod out than to try and report an error--which only serves to make the problem worse, as bugs go completely unreported because users are trained to look for alternatives instead of hope for a fix.

It does not help at *all* that Java is the language you have to deal with. Java is a pain in the *ass*. You cannot pay me enough to make me deal with it. It's full of horrible design decisions, and Forge is even *worse*. It *also* doesn't help that Forge's leadership is basically convinced that it's not their job to explain how to use the tools they made.

Worse yet, errors from these mods are incomprehensible, and often nearly impossible to reproduce. I had to replace a backpack mod that had only caused occasional crashes on my end, because it caused *constant* crashes for one of the others. Occasionally, a crash happens the first time I launch and *never again*. It is nearly impossible to say which mod is causing a bad interaction--doubly so because it may not even be any of the mods mentioned in the stacktrace. And if it's *not* a crash, it's hard to test, because of the sheer size of a modern modpack. The one I'm working with is nearing 200 mods, with some mods adding dozens of monsters or blocks--how do I know that damage values for a given mob make sense? That *armor* makes sense? If I were developing something on my own, I could build in automated testing, but because it's Java and I refuse to touch Java, I'm stuck with what exists, which is manually testing combat.

### Minecraft modpack development is a special kind of dev-ops hell.

And I cannot *wait* to build something better. Eventually. When I have money to hire other people.
