---
title: "Hellwave Roadkill Devlog 2"
date: 2021-06-30
draft: false
---
### Progress: Slow and Steady
Right now I'm working part-time at Amazon--yes, *that* Amazon. Luckily, I work in an airport warehouse, and it's slightly *less* hellish here than it is in the dreaded Fulfillment Centers, which are exactly as dreary and dystopian as you'd expect. Unluckily, it's still modern capitalism, which means it's still fucked.

The good news is, I'm making steady progress, despite the time I'm having to spend away from development. First of all, I've brightened up the renders significantly, and made the nails out of brass instead of the same gunmetal shade that was in the last post. This is mostly because I'm concerned about visibility, especially once I put together the noir-esque shader I want to use for Bodymode. I'm likely going to use the same nail sprite both for enemy projectiles *and* for the player's current weapon, so I want it to read well in all modes.

More importantly, I have a pretty good low-poly humanoid now:

<blockquote class="twitter-tweet" data-theme="dark"><p lang="en" dir="ltr">Got some animation work done, and now it&#39;s in the game! So far I&#39;ve only done the walk cycle, but I&#39;m pleased with how the model turned out. TODO: pants.<a href="https://twitter.com/hashtag/HellwaveRoadkill?src=hash&amp;ref_src=twsrc%5Etfw">#HellwaveRoadkill</a> <a href="https://t.co/pK0Q0zabEB">pic.twitter.com/pK0Q0zabEB</a></p>&mdash; DanBreez (@dan_breez) <a href="https://twitter.com/dan_breez/status/1410436010069090304?ref_src=twsrc%5Etfw">July 1, 2021</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script> 

This is kind of a big deal. Humans and other living things have always been my biggest weakspot in art--I can do passable inanimate objects, but organic things were always just *awkward*. The fact that this one came out so well is a big deal. Lighting still needs to be adjusted on the render--it's too bright in the front, to be honest--but this will do for the short-term. I need to put together a melee attack animation and some death frames.

### Patreon: Locked and Loaded
I *also* have just started up a [Patreon](https://www.patreon.com/perfectlyspherical?fan_landing=true), to help fund development. I'm looking for funding wherever I can find it, because A) fuck my job and B) if I can do that freaky zombie thing in about four hours of actual work, imagine what I can get done if I'm not wasting three or four days a week dealing with Amazon's bullshit, followed by another day of trying to talk myself down from "quit and go become a hunter-gatherer" to "maybe one more week".

My "quit my job and do this fulltime" goal is 750 a month. I'm not offering anything super fancy on the tiers--I firmly believe that offering private feedback channels is a bad idea, and I don't have merch to sell--but you *will* get your name on the [credits page](https://perfectly-spherical.tk/page/credits). It's gonna be updated on the 2nd of each month, to account for people joining on the end of the month and such. Consider it kind of a social experiment: How much money are people willing to give for the sole purpose of having their name on a page?

### About enemy design
Getting back to the topic of how the game is going, I should talk a bit about what this zombie guy is planned to be in the game.

There's a certain school of monster design that calls for a "popcorn" monster--something easily defeated, that can be used as cheap filler in an encounter. While there are arguments to be made that an enemy that poses no threat is a waste of the player's time, *this* game's mechanics play into it--the time limit, and the need to kill things to *extend* that time limit, mean that a popcorn enemy is *also* a walking healthpack.

This zombie also serves an important role lore-wise--it's the end result of the disease. Demented and in constant pain, it lashes out blindly at whatever it can reach. Sounds familiar, doesn't it? There's also a reason it drops some of the Serum that keeps you alive, but *that* will be explained later in the story.

My plan for its attacks is to have it leap at the player and do damage on impact. It'll be somewhat dangerous in groups, and only if you're *really* bad at shooting them, but it *will* have the ability to hurt you. Technically.

### What's Next
I still need to implement the rest of this guy's behavior. I also have a couple more guns planned, as well as at least two more enemies. I want to get the enemy designs and weapon designs in particular mostly finished before I start building a level, but I already have some idea of what the play area will look like--I'm gonna lean into the dead mall aesthetic, probably have the player start in some kind of incinerator (imagine a budget morgue in a minimall). With the rate things are going right now, I'm expecting something like a 2-3 month dev cycle for the first vertical slice--I'm hoping to have something presentable enough that I can put it on itch.io and get some public feedback and awareness. Part of my plan is to have self-publishing on the table, because I can't guarantee I'll get a publisher deal at all, even with the positive reception I've gotten.