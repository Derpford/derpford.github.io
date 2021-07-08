---
title: "Hellwave Roadkill Devlog 3"
date: 2021-07-08
draft: false
---

### Sounds Of Death

This week, I got a couple important things done, but the one you'll probably wanna hear most is the firing sound I added to the gun!

<blockquote class="twitter-tweet" data-theme="dark"><p lang="en" dir="ltr">The gun makes sound now. <a href="https://twitter.com/hashtag/HellwaveRoadkill?src=hash&amp;ref_src=twsrc%5Etfw">#HellwaveRoadkill</a> <a href="https://t.co/IpWx8MQ51n">pic.twitter.com/IpWx8MQ51n</a></p>&mdash; DanBreez (@dan_breez) <a href="https://twitter.com/dan_breez/status/1412941362685779975?ref_src=twsrc%5Etfw">July 8, 2021</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script> 

As mentioned in the tweet, this was synthesized from three CC0 sounds. I wanted to do something similar to what Quake 1's sounds were built out of, and I think this came together nicely.

### Getting the mechanics put together

Another thing that happened this week: I laid the groundwork for Soulmode and Bodymode. The player can now press the "Reload" key (I'll rename it later) to swap between Bodymode and Soulmode. While in Soulmode, you consume Serum 3x as fast. Right now, it just toggles the shader I put together last week, but I'll be adding a unique Soulmode weapon, doing a specific damage type, so that monsters can detect that damage type and not drop Serum when hit with it. The player is gonna spend most of their time in Bodymode by necessity, dipping into Soulmode when they can afford it.

Alongside this, I implemented the Serum timer, as well as causing monsters to drop serum on hit. I'm going to add the Serum drops on kill later, once I've figured out what I want health pickups to look like. I'm still fiddling with the numbers, but as of right now monsters drop 1 point of Serum for every 5 damage they take in one go; in other words, if you have at least 5 DPS, you'll generate more serum than you're losing. Note that, at the moment, this is calculated per-hit. I may leave it like that, or I may build something to account for many small sources of damage at once. It'll depend on how I balance the rest of the arsenal.

### Speaking of the future arsenal

My next gun concept is gonna be a sort of shotgun-crossbow hybrid that fires syringes. Or shattered glass, if you need something with some close-range oomph. Yes, it's edgy as fuck, that's the point.

The syringe shot will be more status-effect than damage--it'll stunlock an enemy for a bit. The idea is that you'll use the syringes as a way of taking a specific enemy out of the picture for a bit. Meanwhile, the shattershot will serve the role of an SSG, giving you a close-range "get off me" tool. I think I'll have the shatter-shot be the primary fire, with the syringe blast being an altfire that you'll get as an upgrade.

After that, I'll start building two more enemies--a dude with a nailgun, kind of like yours, as well as a dude with a syringe gun. The nailgun guy will likely be your first major threat, while the syringe gun dude will likely be how you get the syringe gun in the first place--but his is kind of busted, so it shatters the syringes as it fires them, hence why you need an upgrade to get the proper syringe shot. 

Things are running smoothly, as of right now. Fingers crossed.