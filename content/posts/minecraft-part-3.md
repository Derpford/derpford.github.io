---
title: "Dr. Strangeloot (MLHRWM, Part 3)"
date: 2021-09-16
draft: true
---

### Or, How I Learned To Stop Worrying And Farm The Drops.

So, Minecraft has items, right? And these items drop from certain things, right? Most of these items drop *consistently*. However, there's several items that drop on a *dice roll*. Items which *might* drop, rather than items which *always* drop. And the thing is, in Minecraft, these 'rare drops' have two common qualities: One, they're used to gate a specific mechanic, and they drop so rarely that in some cases you might find one per game. Let's talk about how utterly terrible this is.

### What's the point of randomness?

#### First: Unpredictability.
I dunno if I've said this exact thing before, but it's a through-line in many of my beliefs regarding game design: A good game is one that can be reasoned about. Well-designed games tend to be games that players can step back and *strategize* in, even when the game is too fast-paced to think about in the moment.

However, this comes with a catch: If a game can be *solved*--that is, if there's one strategy that always works--then the game stops being fun. People don't play games to *win* them, as a general rule; they play them to enjoy the path *to* winning them. Even the exemption proves this--people who speedrun games don't do it just to see the ending faster, but rather to push their technical skill and strategy to a new limit. Even people who write cheats for games typically do so because they see the technical challenge of writing an effective aimhack or wallhack as a hill to climb.

This goes the same for games that can be "solved" into a stalemate. Tic-tac-toe is not 'solvable' in the sense of having a winning strategy, because optimal play always results in a tie. All the same, though, because the game always ends the same way, nobody plays tic-tac-toe competitively to the same degree as, say, Street Fighter 3rd Strike. Same goes for Rock Paper Scissors, which cannot be solved, but has no variation between opening moves--because nothing's carried over between rounds and because each move has the same 33%-ish chance of victory, the closest to strategy and counterplay that RPS gets is in multi-round games against the same opponent.

The point of all this is that a game must balance two qualities: The ability to *reason about* the game, and the *unpredictability* of the game. It must simultaneously be possible to look at the game state and understand what's going on, and also not be able to predict with 100% certainty what the game's next state will be.

You can achieve this with deterministic games, but only with a ridiculously complex deterministic system. The cheap way is randomness. Therefore, lots of games use randomness to supplement the game's unpredictability. This goes all the way back into card games and dice games, so there's plenty of precedent.

But that's not what Minecraft uses its randomness for.

#### Second: Discovery.
If you've ever played Diablo or Borderlands, you know what I'm talking about. Random modifiers, used correctly, will create hours upon hours of interesting and exciting loot-grinding. There are many different approaches to this, from taking a few basic weapon types and applying wide variation in stats (as in Diablo), to taking a large number of base designs and applying a couple of random perks to each one (a la Destiny), to tying them directly to the character's skillset (as in Minecraft Dungeons), you can stretch a set of weapons out for hours or days by the careful application of random modifiers. Ideally, each combination of modifiers is viable at whatever level of play the item was found at, so that the players can always choose what they just got--but may instead choose to look for something that suits their playstyle better...

But this is beside the point, because neither of these things are what Minecraft does it for.

### The Wrong Way: Rarity For Rarity's Sake.

In games with dicerolls on things like attacks, you're adding unpredictability. In games with dicerolls on item stats and perks, you're adding discovery. In *Minecraft*, the unpredictability comes *exclusively* in the form of "This thing is rare because it's useful".

Not even *powerful*, just *useful*. Take flint, for instance. Flint drops at about a 10% rate from gravel. Technically, you can break the gravel over and over until you get flint. Practically speaking, this is a pain in the ass. Why does flint drop at only a 10% rate? Why is it not a crafting recipe? Who knows! What's it used for? Arrows and the flint-and-steel. Your basic ranged weapons and your ability to go to the Nether are contingent on an item with a 10% drop rate.

Or, like, take Blaze Rods. I talked about Blaze Rods in my last Minecraft blogpost. Technically, blaze rods drop at a 50% rate. I'm honestly shocked by this, because blaze rods seem to almost never drop. This is partly, of course, because humans don't handle randomness well--they expect the coin to turn up heads way sooner than it sometimes does. However, it's also partly because it's a 50/50 chance to drop *one* rod from a monster that's already tankier and more dangerous than most. As much as I love the Blaze more than most Minecraft enemies, it is something of a slog to fight. And frankly, that just makes it all the more painful when it doesn't drop a blaze rod.

Or endermen! Endermen *also* have the mysterious 50%-but-not-really thing going on. I once joined a server that had this whole quests thing going on, and quest number 1 after the tutorial area was "gather 40 ender pearls". Nope. Fuck that.

And that's not even getting into the crazy stuff. Like tridents! Tridents drop at a rate of 8.5%. *IF* the target spawned with a trident in hand, which only happens 15% of the time. This is, incidentally, the same chance that other mobs have to drop any item they're holding, and it only goes up by *1 percent* per level of Looting you have. And if you're looking for something useful, zombies can drop iron...with a 2.5% chance of a drop, same as carrots and potatoes.

Minecraft seems utterly addicted to the idea that useful things should almost never drop, which is exactly the *opposite* of what should be happening. I should not have to burn through a double chest full of rotten flesh to get *one* iron ingot.

### A better way: Small-but-consistent numbers

I like how Warframe does it. In Warframe, every enemy drops at least *some* stuff when you kill it--usually a small quantity of crafting materials from that planet, as well as some ammunition or energy pickups. You don't *always* get materials, but you usually *do*--and this is balanced out by the fact that most of the weapon crafting recipes require hundreds or thousands of units of each material, meaning that you're still killing hundreds of enemies to craft any one gun.

Ah, but here's the trick: You're making constant, steady progress *towards* that gun. You can *measure* that progress. You are never frustrated by a seemingly-impossible drop rate--rather, you are able to watch and anticipate as the number ticks toward the finish line. And if you're like my new boss, who is the unluckiest man in the fucking world, you'll actually make progress.

### Don't rely on RNG to gate things.

It's bad. It's *really* bad. You end up screwing some percentage of your userbase super hard. If you *really* have to, add some kind of backup method. Otherwise, your players will wander around the world, looking for something that *should* drop at a 50% rate and yet has not dropped once.