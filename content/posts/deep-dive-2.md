---
title: "Deep Dive, Part 2"
date: 2022-08-15
draft: false
---

### In the last post, we established what the problem is.
Because of how farming works, and how travel time works, dying in League of Legends always costs you at least one wave of farm--and by design, minions are worth significantly more than kills early in the game--which paradoxically makes kills extremely valuable, because dying means missing sweet, sweet minion gold.

So let's talk about what we can *do* about that.

### Step 1: What's off-limits?
There are some things we *can't* change, because it's just not practical.

#### 1. Reworking literally everyone is not in scope.
I could, theoretically, throw my hands up and say "We're building a new game from scratch!". This is not in the scope of this blogpost. It would be a monumental effort, and it's frankly kind of amazing that Riot Games themselves were able to do it with Wild Rift.

This solution has to work *without* drastically changing every character. We might need to rework *some* characters, or maybe even add a new animation to everyone, but the answer to this is *not* to rewrite all the characters to be incapable of getting killed under tower.

#### 2. Getting rid of kill gold isn't viable.
Way too many characters are reliant on kill gold or assist gold to function. As much as I hate damage supports, I am not going to propose nerfing them into the ground by getting rid of kill and assist gold; and junglers kind of need kill/assist gold as well. Besides, this would have powerful and unpredictable effects on characters who get stacks or other passive effects on takedowns--would Pyke be *less* powerful because he gets less gold from doing his thing, or *more* powerful because he's now the only damage support who can give his ADC gold as part of a kill?

#### 3. We can't change respawn timers or travel time.
Fundamentally, the strategy of League of Legends *requires* that crossing the map takes time. Even the moment-to-moment objectives, such as towers, require respawn timers and travel time to be viable--if you could just show up at your tower, *taking* your tower would be a lot harder. URF mode has its cannon, sure, but URF mode *also* makes everyone a lot more dangerous, especially mages--and if we just make URF's power balance the standard, we're back at square one, because high-burst-damage characters like mages are the ones doing all of this early-kills stuff.

### What do we actually want?
It's important to set a clear and specific goal for this design change--not just the *what*, but the *why*.

My goal with these proposed changes is to *create an obvious counterplay to being pushed out of lane early on*, such that *a player who is behind early has a clear path to recovering*.

### So what can we do about it?
I have three proposals:
1. Change how you get gold and XP, making it easier to focus on dodging skillshots without falling behind.
2. Grant bonus gold/XP from minions when a player is behind, up to the amount of gold advantage their death generated.
3. Make tower more obviously a safe zone, with defensive buffs that make it harder to die if you stay under tower.

### Proposal 1: Gold Piles
In the MOBA that Blizzard wants to forget, Heroes of the Storm, there is no last-hitting. Instead, minions drop XP, Health, and Mana orbs on death--which are collected by standing near them. In this way, HotS encourages splitting up among different lanes, while *also* not punishing players who aren't able to multitask between last-hitting and dodging skillshots.

What if we implement something similar in League of Legends? Instead of getting gold on last-hit, minions drop gold on death. Since an important part of last-hitting is that attacking makes your character stand still--and thus makes them more vulnerable to skillshots--we can replace the automatic collection with a right-click, similar to Senna's ghosts. The gold piles could expire after a second or two, preserving the threat of *missing* farm--but in effect, we've extended the window in which a character can last-hit.

This has a number of effects. First of all: Gold from farm is going to skyrocket in the lower elos. We're making farm way easier. That's kind of the point--farm has gone from a thing that requires precise timing, to a thing that you can do as long as you're able to click on the thing. This wouldn't just come with a 2-second click window--it would also mean a new visual effect, a gold pile falling to the ground, which doubles as a reminder that this thing needs clicking.

It *also* means that there is a two-second window for *mixups*. Think of things like Sion's W and Q, or the charge window on Xerath's Q, or the retrigger window on Swain's E--there's interesting things to be done with a couple-second gap where a player can *choose* when something happens. We've lost the precise timing requirement on last-hitting, but that *also* means that denying a last-hit is no longer a matter of guaranteed timing. New players are going to rush to activate the gold, which will make it easier to poke them while they're trying to grab gold--but as players get used to the idea that the gold isn't going to go away instantly, they're going to start playing with the timing, and now you've interested a different kind of skill expression.

You could *also* play with different collection distances. If the collection distance is the same as the champion's basic attack range, it's functionally the same as last-hitting with a wider window; if the collection distance is *different* from the basic attack range, that's a new balancing tool. Melee characters could be made more viable in a lane by letting them collect gold from further away than they can attack, letting them farm without playing as aggressively; over-aggressive ranged characters can be reined in by giving them shorter collection ranges, punishing them if they have to back off.

The downside of this is that you *can* still get pushed way out of lane. This doesn't save a lane that's already behind--it just makes it harder to be behind in the first place, by giving players more room to focus on dodging.

### Proposal 2: Catch-Up Gold
We could also try making the farm you get *after* dying worth more, to help you catch up.

What I would do is, essentially, calculate out a character's gold disadvantage--how much farm did they miss while dead? How much did they likely miss while walking back to lane? How many assists has the enemy team gotten off of them? How many kills?

This would be added to a Catch-Up Gold Counter. While your character has a Catch-Up Gold Counter greater than zero, minions are worth extra gold--and any extra gold you get from this effect is subtracted from your Catch-Up Gold Counter.

<aside>If someone got an assist on that kill, the total gold advantage for everyone involved in that takedown would come out to 300 (kill) plus 250 (farm) plus 150 (assist) for a total of 700--I'd have +10 gold per minion for 70 minions.</aside>

For example, if I die to my lane opponent at 5 minutes, they get 300 gold advantage, *plus* an average of 125 gold from the wave they can now farm with impunity, *plus* an average of 125 gold from the wave I'm gonna miss while I'm walking back to lane, for a total advantage of around 550. This would get added to my CUG counter. Each time I kill a minion after that, I'd get an extra 10 gold, and 10 would be subtracted from my CUG counter. Assuming I don't die again in that time period, after killing 55 minions, I'll have recovered from that 550 gold disadvantage, and I'll stop receiving bonus gold on killing minions.

We could *also* make this bonus gold apply when minions die nearby, *regardless of whether I last-hit them or not*--so that I still get the benefits if I'm in lane, regardless of whether or not I'm able to last-hit effectively. This would function similarly to the bonus gold from nearby minion deaths in URF.

This proposal would specifically play into the idea of *late-game scaling characters*, who are usually (but not always!) more reliant on items--and thus are hurt more by losing farm. It would also *specifically* encourage staying in lane, especially if the bonus gold applies even when I'm not able to last-hit, which means it *directly* encourages the behavior we actually want--players continuing to engage with the game even after an early loss.

However, it *also* means that gold advantages from kills will tend to be temporary things. I would argue that this is a good thing, because it means that it's more likely to be a close match than a curbstomp. However, some players--especially those who rely on early gold leads to snowball--are going to complain that I'm effectively rewarding a player for dying early.

It's also really, really important that this catch-up gold mechanic calculates based on the estimated gold advantage of the players who participated in the kill, *not* a flat value--and the bonus gold should *only* trigger on an actual takedown, not an execute, because otherwise players may start running under the enemy tower to get bonus gold from getting executed. There's still a chance that players will start trying to throw the early game so they can get lategame gold, though intentionally dying to the enemy team is already a reportable offense. I'm not sure there's any way to really *stop* this, unfortunately--not without making the catch-up gold mechanic harder to use legitimately.

### Proposal 3: Tower Buffs
What about a different approach entirely? We can't just remove kill gold from the picture--but we *can* make it significantly harder to secure kills against players that aren't extended.

Tower is *supposed* to be a legitimate threat to players on the opposite team. The tutorial eagerly informs you that you are safe within your own tower's range, and that you are *NOT* safe if you wander into enemy tower range. This is...only *partly* true under the current design, as some characters can easily burst down a low-health enemy before the first tower shot lands. This only becomes more of a problem as a gold gap develops. At this point in time, the only threat a tower carries is *damage*, and that damage is only a threat if the fight takes a *lot* longer than the attacker was planning for.

To that end, there's two changes I'd like to make to the way tower works:

#### Safeguard
There's an item called Crown of the Shattered Queen that was really popular for a little while after it came out. Its effect, essentially, gave you 75% damage reduction for the first 1.5 seconds of a fight (as well as a bit of ability power while the DR was active).

This is incredibly powerful.

What if turrets gave you a similar effect?

It would be scaled down, of course, because A) this would end up stacking with the Crown, and B) the Safeguard buff has already been identified as an insanely powerful anti-burst effect. But, making the first second or so of combat significantly less painful would make it much harder to die under turret.

For the sake of argument, we could have "Towerguard" give 50% DR to characters standing under their own tower, lasting 1s after the first instance of damage they take. The effect would reset after--let's say, 10 seconds without being damaged by an enemy champion. This means that characters like Lux or Brand, who have to dump their full combo onto a target to kill, will have to back off for *just* about the same amount of time as the Towerguard buff. Characters with some sustained damage output, or lanes where both players are coordinating to keep damaging the enemy laner, would be able to keep Towerguard offline...but that's okay, because in both of those cases, the attackers are having to spend *more time under tower*, which makes towerdiving inherently riskier.

#### Root
Remember how I said that the only threat towers have is *damage*? Part of the problem is that this damage can't be *too* high on the first hit, because if it were, players who stumble into tower range by accident would be *screwed*. Towers *are* supposed to do more damage over the first three hits--despite the bug in Patch 12.14--but that only matters if the second and third shots are both fired, and most (successful) towerdives are over within two shots (or even before the *first* shot lands!).

What could be both *more* threatening than damage to someone who's committing to the dive--and also *less* threatening than damage to someone who turned around the moment they realized they were in tower range?

Crowd control!

The first tower hit--the one that does base tower shot damage, not the boosted ones--enemy champions would also be *rooted* for a second. This has entirely different effects depending on *where* they're standing when the root lands.

A champion who's going for a *deep* dive is much more likely to eat a second tower shot if they're forced to stand under the tower for another second, and that root also means they're more likely to take damage from the abilities of the champion they're diving. The victim of the dive can also use this brief root to put some distance between themself and the diving champion, making it harder for a melee assassin to ruin your day after jumping on you under tower.

Meanwhile, a champion who goes for a shallow dive--standing near the *edge* of tower range--is going to get rooted near the edge of tower range. If they're thinking quick, they might get rooted *just* outside of tower range--not a great position to be in, but it can still put them in the middle of a minion wave, or make it easier for a ganking jungler to land their own abilities. This is where the *real* difference is made--characters who can drop all of their damage onto a target at the edge of tower range, where they can get a kill without taking more than one tower hit, will now have to worry a lot more about whether their victim's jungler is hiding in the bush.

Finally, the player who wanders a bit too close to tower range is put in an awkward position, but they aren't going to be in any more danger than they would be *without* the root--if they walked too close while the lane was mostly empty, they get out safe; if they walked too close while enemy laners were present, they were already flirting with danger. 

### Which one should we implement first?

Proposal 1 requires a lot more asset work than the others, so it's likely our last priority. Likewise, Proposal 2 requires some finicky math, and while it's something that we can theoretically calculate using only info that's already in the League of Legends codebase, it's something that we'll want to put on an extended beta testing period of some kind--gathering as much data on how it affects the game as possible.

With that in mind: Proposal 3 requires the least work, has the most immediate impact, and has the most obvious balance handles--if Towerguard is too powerful, we can reduce the DR, and if the root is too much--or is throwing players off, making them miss skillshots more often against diving enemies--we can replace it with a slow. I would *start* by implementing Proposal 3.

It's also worth noting that Proposal 1 would make a great candidate for testing with an alternate game mode, which would give it a wider set of test data than League's PBE without risking backlash if it doesn't work like we expected.