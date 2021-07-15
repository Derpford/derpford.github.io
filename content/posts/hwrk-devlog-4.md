---
title: "Hellwave Roadkill Devlog 4"
date: 2021-07-15
draft: false
---

### Schmovement.

It is absolutely essential to me that the movement mechanics feel good to use. More than that--given the time-attack-esque mechanics of serum and serum consumption, it's important that the player *not* be limited by movement. It would absolutely suck if the player got lost in a level, and was unable to make it back to a nearby group of enemies before their Serum runs out, due to not having a quick way to get around. I also want combat to be highly mobile. To that end, I've refined the movement mechanics a bit.

### Bunnyhopping
is one of my favorite movement mechanics, because it rewards a kind of input precision that most people *don't* associate with games like *Quake 3*. Specifically, *strafejumping* is my favoritest thing ever, because it rewards you for making *smooth* inputs.

For those who missed out: Strafejumping involves two inputs: one of the strafing keys (left or right), and a matching turn input. By turning in the same direction you're strafing, due to a physics glitch in *Quake*'s movement code, you'll gain a small amount of forward velocity. This is normally not enough to overcome friction, but if you're in the air, friction doesn't apply--and coincidentally, you can stay in the air near constantly by bunnyhopping. The result is that, if you can keep jumping *and* coordinate your strafing keys with your mouse movements, you can build velocity over time.

The trick is that if you turn too sharply, you *lose* most of your momentum, so strafejumping is only really useful if you can make sustained smooth inputs--typically, you'd see people build up speed using a figure-eight path in a large room, or taking long curving paths through whatever level they're working with. Strafejumping also tends to send you *over* items in *Quake 3*, so there's a tradeoff between speed and resource gathering--not to mention that an astute opponent will hear you going "HUUH--HUUH--HUUH" as you jump around, and pick up on your location.

### I'm not reimplementing all of Q3's movement code.
Fuck that. Not only would it create a messy licensing tangle, it would also carry side effects, and generally be a ton of effort. I'm thinking about releasing my source code *anyway*, because I like iD Software's model of releasing the engine and selling the content--but I'd rather not deal with figuring out which parts GPL would apply to, since wiser folks have struggled with that question for years.

Besides, I don't *want* Q3-accurate bunnyhopping. I do want bunnyhopping, but there are things *Quake 3* did which I don't want. For one thing, you had to hit the jump button with every jump in *Quake*-derived engines, which is a recipe for carpal tunnel when combined with alternating strafe keys. And I don't care about that kind of input precision--I already have the combat to test your twitchy reaction time and button presses. What I want out of this strafejumping mechanic is the smooth-input test, rewarding you for reading your environment and figuring out how to take a smooth racing-game style line through it. To that end: Fake strafejumping.

<blockquote class="twitter-tweet" data-theme="dark"><p lang="en" dir="ltr">Fucking around with jumping physics today. Built me a sort of fake strafejump; you don&#39;t have to match movement keys to turn direction, but you do have to be pressing a movement key. I barely understand what I&#39;ve done here, but it works. <a href="https://twitter.com/hashtag/HellwaveRoadkill?src=hash&amp;ref_src=twsrc%5Etfw">#HellwaveRoadkill</a> <a href="https://t.co/hmbjdTmU4c">pic.twitter.com/hmbjdTmU4c</a></p>&mdash; DanBreez (@dan_breez) <a href="https://twitter.com/dan_breez/status/1415203068254248963?ref_src=twsrc%5Etfw">July 14, 2021</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script> 

### What else?

I still need to fiddle with the slide physics, as I mention later in that thread; I want the slide to be your precise, short-distance movement option for getting out of a web of projectiles, while the bunnyhop is your go-to for longer distances. I also want to have slide-jumping, in the same vein as *Ultrakill*'s momentum-preserving dash jump (though I'm not planning on a stamina system like *Ultrakill* has). My goal is for the player to be able to slide-jump and immediately reach a very high speed.

This also has to tie into the movement-related crowd control options. You can slide into enemies to launch them around, and jump off of them as well, and that has to work well with the slide and bunnyhopping.

Oh, and I'm working on another gun model. I'll be building 3 guns in total for this vertical slice, and--after a burst of inspiration--the Disgusting Meat Railgun is up next.

This was a slow week. The stress of my day job is kinda killing me. It's gonna take some time--and probably a playable demo--before my patreon will actually cover my bills. I have some potential options, thanks to a couple Silicon Valley type people I know, but that's not gonna pan out for at least a couple months--if it pans out at all. This is the catch-22 of low-income gamedev--if I can finish this game, I can finally be free of the stupid bullshit job that's slowly driving me insane; too bad the stupid bullshit job keeps getting in the way.