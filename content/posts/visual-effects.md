---
title: "Visual Effects"
date: 2021-08-10
draft: true
---
### Let's make this simple.
Visual effects--AKA the "look" part of "look and feel", the stuff that flies around the screen to tell you that Things are Happening--should be at least *sort of* obvious. Enemies leak blood when they're shot, rock walls make sparks when your pickaxe hits them, bombs have a big cloud of fire and smoke when they go off, your mage's spell creates a lightshow when it's finished casting.

But there's more to it than that. There's a very subtle, extremely important detail that separates good visual effects from bad visual effects. It's a distinction that might not sink in the first time, so I'm going to be absolutely clear here, because even in the AAA sphere--*ESPECIALLY* in the AAA sphere--people get this wrong all the time.

Ready? Okay.

### VISUAL EFFECTS SHOULD *TELL YOU WHAT'S GOING ON.*
They should *NOT* make it *HARDER* to see what's happening. Are we clear? Good. I shouldn't have to beat anybody over the head with this, but for some godawful reason, VFX tends to fall into two major flaws.

#### The Brown, The Blur, and the Bloomy.
The first major flaw is common among works that are trying to be more realistic, or gritty, or just plain muddy. There's a few common culprits--color palette tends to be a dump stat in these games--but the worst one, in my not-humble-at-all opinion, is motion blur.

<aside>Yeah, it turns out that our eyes construct motion blur for us--but only if you have a 'framerate' approaching the limits of what the human eye can perceive, and no, you aren't capped at 60FPS. You can see a noticeable difference between a 144fps scene with motion blur, and the same scene without it.</aside>
Ye gods, motion blur. Theoretically, motion blur is awesome, because it sells the idea that--y'know, things are moving. It fills in for the details that are lost due to the limits of framerate. It works best when applied to individual fast-moving objects, so that you can pick that smear of motion out as it crosses your screen without losing all the details on things that are standing still. Done right, motion blur imparts information about which objects in a scene are stationary and which ones are zooming across the map.

The problem being that nobody fucking does that. The *only* case I've seen where motion blur was applied selectively is in *Portal 2*, where it was applied in a sort of tube around your character, oriented to how you're moving--meaning that you could tell from the motion blur roughly where you were going and how quickly you'd get there, a really useful piece of info in a physics-based first-person platformer. 

Everyone *else*, on the other hand? Slap that blur all over the screen. Turn it up when the player turns around. Oh, yeah, and the implementation sucks, too--aside from Portal, I haven't seen a motion blur implementation that performed reasonably at all, meaning I'd regularly get both a minor latency spike *and* a smudged screen whenever I turned too fast. It's not like I need to make sudden turns and react quickly in, say, Team Fortress...

...also it's just kinda ugly, in my opinion. I don't like looking at full-screen motion blur, full stop. I've never had a good experience with it.

But, see, there's an empirical issue at the root of my whining: Blurring the entire screen, by definition, reduces the amount of info the player can gather about what's happening. And you're blurring the entire screen right as the player turns around, meaning that they're looking at an entirely new screenful of info and *they have no fucking idea what they're looking at* because *SOMEONE* rubbed vaseline all over their monitor.

#### I Can't See Shit, Cap'n!
On the other side of the coin you have games where there's a billion particle effects going on at once, or where the particle effects are too similar to each other. The two big examples I have *here* are *Super Smash Brothers Brawl*--which suffered from trying to have somewhat photorealistic graphics on the *Wii*--and *DotA 2*, which suffers from a bad case of asset reuse.

Brawl had many problems. One of these problems was that they wanted to make the game nice and pretty, but they had a fairly limited spec sheet. The Wii was still built with pre-widescreen TVs in mind. Its resolution and processing power were...not as good as other stuff on the market. This meant the thing sold like hotcakes compared to its more expensive rivals, but it also meant that Brawl's darker color palette combined with the dev team's desire to show off to create a game where it's just really hard to identify what just happened. Launch someone--or multiple someones--and the screen becomes a mess of smoke as characters go flying. Relatively low resolution, too-large smoke particles, the need to zoom out so that all the characters stay on the screen, and God only knows what kind of particle effects were on the move that launched everyone...

And then there's DotA. I have it on good authority (source: my friend who plays DotA for some reason) that there are many overlapping visual effects--particles and models that aren't visually distinct, but which are attached to entirely different mechanical information. His favorite example was the "giant meatball" visual, a fireball model that's simultaneously used on characters like Invoker (hint: stay away from Invoker's meatball) and characters like the Phoenix (hint: to kill the Phoenix, shoot the meatball until it dies). Almost exactly the same visuals, two entirely different reactions expected.

### So how do we do it right?
There's a bunch of different answers to that question. As much as I dislike Riot's other game design decisions (and their monetization, and their 'anticheat'), *Valorant* has excellent visual design. Not only does the brighter palette make it easier to see bloodsplatter on hit than in *Counter-Strike: Global Offensive*, they also take pains to make the visuals on things like smoke effects as representative of their area of effect as possible. The nice, clean spheres make it obvious whether or not you're covered, even if smoke doesn't work like that IRL.

Another example comes from Dragon Ball FighterZ, where the hitsparks use both color and shape to make it clear whether an attack was blocked: clean hits are orange and spiky, blocked hits are round and blue.

*Team Fortress 2* has another example: Enemies that are on fire will also glow in their team color, ensuring that you don't mistake a BLU merc on fire for a RED merc. Likewise, *Left 4 Dead* and its sequel will highlight allies and interactable objects on most difficulties, so that you can tell where important things are.

You might be wondering--doesn't smoke obscure things? Yes. It does. The trick is that it obscures <i>player intent</i>, not <i>information</i>. The thing that a smoke grenade makes hidden is the position and movements of the players, and the rest of the game is designed around carefully managing how much info you leak to your opponent. It does <i>not</i> obscure anything that should be common knowledge, like where the smoke grenade is. L4D doesn't highlight every single usable thing on the map, nor does setting someone on fire in TF2 highlight them through walls. This *does* mean you have to think about what information the player ought to have, but that should be part of your design process anyway--the player has to act on the information you give them, and a game can feel vastly different with different amounts of info available to the player. That's *why* visual effects should be designed around what information they reveal.