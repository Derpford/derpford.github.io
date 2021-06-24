---
title: "Hellwave Roadkill Dev Log 1"
date: 2021-06-24
draft: false
---
### I'm working on a game, in case you didn't know.
This might not be as surprising as you'd think, depending on how well you know me. I'm basically always working on *something*. That said, a little while ago *THIS* happened:

<blockquote class="twitter-tweet"><p lang="fr" dir="ltr">Combination <a href="https://t.co/21MhdYvSkx">https://t.co/21MhdYvSkx</a></p>&mdash; El Oshcuro (@DaveOshry) <a href="https://twitter.com/DaveOshry/status/1406507248751284224?ref_src=twsrc%5Etfw">June 20, 2021</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script> 

In case you didn't know, that's the guy who runs [New Blood Interactive](https://newblood.games/), which is one of the few publishers I genuinely would love to work with. He's quote-tweeting me.

### This is kind of a big deal.
I have high hopes for this. The fact that Oshry showed interest at all is great to begin with, even if the response was something of a curveball. See, the ideas I'd pitched were already half-complete, and I was trying to figure out what to prioritize, and then Oshry went and said "Combine them" and now I gotta start from scratch.

Don't get me wrong; I'm hype as fuck. This is the biggest moment of my life. No pressure, though.

So, given that I have a barebones game development blog, and a game I'm working on, and nothing in particular to lose, I figured this is a good place to summarize my weekly efforts.

### I'm an asset man
A lot of my less successful projects didn't fall through because they weren't playing right, really. Nor did they fail because they didn't gain traction--in fact I have several things that simply haven't seen the light of day at all. And the reason for this is that I'm not an artist, but I usually have a strong idea of how a game should *look*, and I get frustrated really fast when I realize that I just don't know how to make a game *look* right.

This is one reason why I spend so much time working in [GZDoom](https://zdoom.org/downloads). GZDoom's community have been making and sharing assets for decades. Sure, the attribution gets a bit messy--some of the more popular sprites are the work of three or four artists editing a stock Doom asset--but for mods, this is only a problem if Bethesda starts glaring angrily at you. When I'm working on a Doom mod, I don't *have* to worry about creating art, because I can work with a large library of probably-free assets that are designed with my engine of choice in mind.

Yeah, that doesn't fly in a professional setting. If I build my vertical slice out of assets I found on the ZDoom Forums, I am *at best* gonna have to hire an artist to redo all those assets later, and if there's any public awareness of the older builds at all, I'm gonna disappoint *somebody* when the final release doesn't have that edit of an edit of a kludge of a sprite that--surprise!--has been copyrighted since '94.

And my drawing skills are kinda garbage.

But I haven't really dug into 3D modeling yet. Maybe I'm good at that?

### Apparently I'm good at that
Or at least semicompetent, because look at this shit:

![A scrap-built nailgun.](https://imgur.com/2jRVKbt.gif)
Look at the way the greebly bits on the side rattle when it fires. It looks like it's gonna come apart. How'd a hobo in an alley make something like this? Who fucking knows, that guy's dead, you stole this off his corpse, and frankly it just has to last long enough for you to get a bigger gun.

![The giant rivets this thing fires.](https://imgur.com/AMKfdmS.png)
That glowy bit on the back? That's an inscription that's engraved by the firing pin. What does it say? I'm not telling ya. I should run a contest or something where everyone tries to guess what I wrote on the back of this thing, and if you guess right, you get to have your name in a secret somewhere in one of the levels when I finish it. That can happen when I have a publisher for this thing, though.

I built these over the course of the past two days, from scratch. The gun took longer, mostly because my first three drafts were kind of ass and I lost two of them to Blender crashing on me. But when I got the hang of it, it felt like I'd unlocked the one kind of art I'm actually okay at. Maybe I've been scared of 3D modeling for no good reason.

That said, these are a *little* hard to read in any kind of dark environment. Blender's default settings tend toward very dark ambient lighting, because Blender expects you to either put lights in your scene or export the *model* and not *images of the model*. I, on the other hand, am fucking insane, so I did that bolt sprite by making a ring of orthographic cameras and using a script I grabbed off StackOverflow to render all eight rotations at once:

![HAIL EIGHTCAM, LORD OF DANKNESS](https://imgur.com/jbzSchE.png)

I plan on trying my hand at that whole skeletal animation stuff later. I've always been kind of awful at drawing humanoids, but I suspect that a low-poly plague victim will be relatively easy to do.

### This is really exciting
because getting this shit done over the course of a couple days, in a matter of *hours*, is mindblowing to me. I hadn't touched Blender since an ill-advised experiment with using it as a game engine back before 2.8 came out, so making something that looks okay in a *day* is fantastic. If I can get most of the assets done in 1-2 day jumps, that'll seriously speed up my dev cycle. As of right now, my next goal is getting these into the game, along with copying over my barebones UI from the original Roadkill project and getting the Serum system working. I'm also probably gonna get to work on a basic enemy to play with, because I doubt you guys wanna see gameplay footage featuring the alien freaks from FreeDoom.

I'll try to get a devlog up every Thursday, to complement regular articles on Tuesdays when I can spare the time. There'll probably be an end-of-month summary that I can tweet at Dave, if I can contain my excitement long enough to not tweet at him every week. Let's fucking *go*.