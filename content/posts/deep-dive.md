---
title: "Deep Dives (Or, Why Do I Keep Playing League of Legends?)"
date: 2022-08-11
draft: false
---

### It's been a while.
Not just since my last blog post, though it has *definitely* been some time since the last thing I wrote for this blog. It's *also* been a while since I last left fountain. I'm playing League of Legends, you see--or, rather, I'm *not* playing League of Legends, because of a little thing I like to call "the 5/0 Lux 'support'."

This happens far too often for my liking. If I die early on, the chance that I'm gonna get shut out of the rest of the game is much higher--and the earlier I die, the higher those chances go, outside of really crazy cases where I die before the first minion wave. This is so effective that it has spawned 'kill lanes', team compositions built around getting early kills as easily as possible, and winning the game despite theoretically not having the same scaling potential as your opponent.

Getting pushed this far behind presents me with a bit of a conundrum. 

See, if I *leave*, everyone else on my team suffers for 5-10 minutes and then they (hopefully) surrender, though there's a slight chance that they'll blow the enemy team out of the water. This also inflicts a 5-minute queue timer on me, which grows ever larger if I do this more than once in a row.

But, if I *stay*...what do I even do for the next 30 minutes? I can't go to lane, because once the Lux support has 5 kills and no deaths, I cannot meaningfully contest anything she does. Because I can't go to lane, I don't keep up with the scaling of the rest of the enemy team, and that means...I can't meaningfully participate in teamfights, unless I'm playing someone with some kind of crowd control abilities.

Given the choice between wasting 30 minutes or so of my own time, and wasting 5-10 minutes of *everyone's* time--when 'everyone' means the people on my team who are likely complaining about my performance--the choice is pretty obvious.

### The Current Approach
Right now, Riot tries to keep this situation under control with its moderation tools. That's where that 5 minute queue timer comes from, after all--it's an automated system built by Riot Games for the *specific* purpose of disincentivizing leavers. Repeat offenders are liable to get banned, too.

<aside>For the record: I think you could make this way less of a problem by having the client send a specific message on quit. That way, you can look for that message as proof that the client pressed the quit button.</aside>

But this doesn't really work. For one thing, the 5-minute queue timer is not as punishing as the 30 minutes of having to pretend that I'm still playing. I can go do something else while I'm on a queue timer, for one thing. Meanwhile, if I stay in the game, I have to at least *try* to participate--if I just stand in fountain, I get flagged as AFK and I get the same penalties as I would if I'd alt-F4'd.

More importantly, Riot *can't* make the queue timer more punishing...because Riot apparently cannot tell the difference between a client *crashing* and a client *quitting*. I'm not sure why this is, but for the sake of this article, I'm going to assume this is a difficult technical issue, because I'm here to talk about *game design solutions*, not "learn how to engineer things" solutions. 

The queue timer *does* get big enough to rival the length of a game after 2-3 repeat offenses...but, again, you can just go do something else. Riot cannot meaningfully affect that, full stop--because Riot can't handcuff you to your computer. At the end of the day, 30 minutes of not being in a League game is less awful than 30 minutes of being in a League game that you cannot actually participate in.

Riot has also tried things like the Honor system, where you get rewards if you participate in games and stop getting rewards if you leave too often. But this carrot can't make up for...not being able to play the game.

### I keep saying that I'm "not playing the game".
And this is a serious issue--assuming, of course, that you *want* people to play your game. 

You can get into some fun art-house avant-garde shit if you want, here--hell, Cruelty Squad is one of my favorite games, and it looks like clown vomit, and starts with the main character getting a call from a pig-shaped *thing* in a trucker hat who calls him a loser. You can *absolutely* make a game that does not want you to play it, *unless* you are making a competitive multiplayer game that relies on having a large playerbase.

With that in mind: If you *are* building a competitive multiplayer game, and players feel like they have no impact on the outcome after the first five minutes, *something is deeply wrong*. 

So, now that we know why the top-down enforcement of the queue timer and honor system don't work, let's go over the details of *why* this problem exists.

### Let's talk about farming.
I don't think I've specifically talked about last-hitting in League, which is weird, because once upon a time I *loathed* it. It's been described to me as a very weird, slow rhythm game--and, y'know, if I wanted to play a rhythm game, I'd go play a rhythm game.

The thing is, it serves a purpose, and in the time since [my last League blogpost](https://perfectly-spherical.com/posts/league-part-3), I've started to understand what that purpose is. The need to farm is what drives players to spread out--it's why the game isn't constantly 5v5. If you all group up in one lane, you're splitting the XP and gold 5 ways at *best*, and this means your characters just don't scale up as well.

This is good, because it creates a section of the game where you're able to comfortably duel one-on-one, a thing that I *do* enjoy doing despite being utterly terrible at it 90% of the time.

However, last-hitting is flawed:
1. It demands way too much attention, because it's all too easy to *miss*, and missing a minion often means the difference between success and failure…
2. ...because if you're focusing entirely on farm, the only way for you to keep up in the lategame is to farm better than your opponent…
3. ...because kills are disgustingly powerful.

### But wait, aren't kills worth only 17 minions?
Take, for example, three waves in the earlygame. Before 15 minutes, a cannon minion spawns every 3rd wave, so this would mean 9 casters (worth 14 gold each), 9 warriors (worth 21 gold each), and one cannon (worth somewhere between 60 and 90 gold, depending on how late we are in the game).

This comes out to a total of between 375 and 405 gold, which is worth more than a kill on any enemy who isn't on a killstreak.

Thing is, this is exactly why kills are too powerful--because getting killed means *missing* a lot of farm. A minion wave arrives every 30 seconds--and dies by the time the next wave arrives, if left alone--and it takes just about 30 seconds for a player to reach botlane's first tower from base, without boots. This is *after* the death timer, mind.

In other words, every time you die, you are losing *a third of a kill's worth of gold*, even when the respawn timer is less than 10 seconds, because the walk back to lane takes exactly long enough for a minion wave to pass.

This isn't even getting into the problem of missing farm because you can't contest the opponent. Because I have to be close enough to lane to click on minions--and have to *linger* there long enough to catch them when they're low enough to be one-tapped--I have to be standing in range of things like Lux's Q and E, or Jhin's W, or Miss Fortune's E, or Vel'Koz's entire kit. 

Fundamentally, to last-hit, I must stand in places where some characters can punish me with skillshots. Those characters are *designed* for this! Lux would not be a viable support if she couldn't 'poke' people who are trying to last-hit.

### So how come dying is such a pain in the ass?

The thing is, because a kill puts my opponent 300 gold ahead, and *me* behind an average of 125 in the early game--and because my opponent is free to gather the next wave's average 125 gold--and because the ADC probably got a 150-gold assist on that kill--multiply the kill/assist gold by 2 if my support dies too--for simplicity's sake, we'll assume this isn't First Blood--that gold advantage comes out to:

`600 (support's kills) + 300 (ADC's assists) + 125 (wave) + 125 (the wave I missed) = 1150`

A whopping *1150* gold advantage. That's almost enough for Noonquiver or Lost Chapter, though it *is* split across two players, and 250 of that isn't *real* gold but rather *the amount of gold I fell behind by*. For the purpose of this discussion, though, being behind by 250 gold is essentially the same as the enemy being ahead by 250.

In a vacuum that's bad enough, but depending on how much farm the enemy ADC and Support have gotten while building up to their first kill, that may well put the two of them at the point of *having* Noonquiver and Lost Chapter, which is a dramatic powerspike not only in their ability to wreck my shit, but also in how efficiently they can farm once I've died--especially because I'm also probably behind a level, too, all of which contributes to the chance that I'll die a *second* time. And if me and my Support die a second time, that gives another 1100-ish gold advantage (each consecutive death reduces the gold reward by a small amount). This creates a feedback loop where the more I die, the more likely I am to die, and the more XP and gold I lose while I'm waiting to get back to lane.

In short: ***Dying puts players so far behind, so consistently, and to such a permanent degree, that it dwarfs everything else.*** The gold penalty for repeatedly killing a player doesn't even make up for the lost wave gold--you need to kill a player six times in a row to reach minimum gold reward for them, and by that time--assuming, again, that the enemy support and ADC are both participating in all of these kills, and that my support is getting caught out too--that comes out to `300+274+220+176+140+112+100=1322*2=2644` gold for the kills, `150+137+110+88+70+56+50=661*2=1322` gold for the assists, and at minimum 6 waves of missed farm (remember, each kill basically guarantees one missed wave, because the walk back to lane and respawn timer are practically guaranteed to be longer than one wave lasts). 

By the time the gold from a single kill is less than the gold for a single wave, the enemy laners have developed around a 4000 gold advantage off of *just* the kills and assists, plus the gold advantage from me missing six waves of farm, plus the gold advantage for their ADC being able to farm safely for those six waves. That means that, by the time I'm 0/6, at least one of the enemy laners probably has their mythic--and if all of my deaths were credited to *just* the Support or *just* the ADC, that means that the character who has been the *most* dangerous to me is the one who just got an upgrade!

In theory, this is supposed to be mitigated by me farming better than the opposing ADC. 3 waves is worth more than a fresh kill, remember? But--generally speaking, I'm probably gonna get matched against someone who is at the same skill level as me, meaning I can't rely on being better at farming--at least, not for very long, because if I *can* reliably outfarm an enemy who's repeatedly killing me, that means my MMR is gonna rise until I meet someone whom I *can't* outfarm. And, remember, if the enemy Support is ahead, they can just burst me down whenever I arrive in lane. Once a sufficient lead has been developed--say, a six-kill lead--I am no longer able to meaningfully farm in my own lane, because I can no longer safely remain on the same screen as the enemy laner. I have no lane presence, and that means I *can't* farm. This puts me even further behind on gold, which makes it even harder for me to be present in lane, and we're back to the feedback loop.

### Fixing this is a difficult task.
And it's going to have to be a multi-parter, I think, because there's a bunch of different things to explain:
1. What *can't* we do, and why?
    1. I'm not gonna rework literally everyone.
    2. Getting rid of kill gold would have too many side effects.
    3. We also can't remove or shorten respawn timers, or travel time, because the strategic layer depends on travel time being a thing.
2. So what *can* we do?
    1. We can change the way you get gold and XP.
    2. We can *also* change *how much* gold and XP you get from a wave.
    3. We can even try making it harder to get kills *under tower*, so that there's a clear way to deal with an enemy who's being way too aggressive.
    
In the [next post](perfectly-spherical.com/posts/deep-dive-2), I'll break down how these changes would work, why I think they'd fix things, and what negative side effects they might have.