---
title: "Hellwave Roadkill Devlog 6"
date: 2021-08-12
draft: false
---

### All Quiet On The Monstrous Front.

I haven't got anything pretty or graphical to show you this week, because A) I had a lot of cleaning to do this week and B) what I *did* get done was nonvisual. See, part of good programming practices is laying out the groundwork to make the fun parts work well. I *could* just slap together something that works right now, and--well, it'd work right now--but it'd be hard to build off of, like a shack that was built without a foundation and thus struggles to hold much weight. While I love rapid prototyping, and I also love having stuff to show off, I would rather not have egg on my face a year down the line when I have to figure out how to fix my godawful code.

To that end, I haven't got anything to take video of, but I *have* got a few things to talk about. Let's talk about mixins.

### Mixins are cool.

But to explain why they're cool, first I have to explain 'objects' and how programs are structured.

See, you might've heard of a thing called "Object Oriented Programming". It was quite hip for a long while, and to this day OOP is a key part of many programming languages. The concept is simple enough; you create a "class", give it some properties and some code that gets attached to it, and then you can create new classes that "inherit" those properties and behavior. It saves you a lot of copy-pasting (and all the headaches that come with it).

For example, let's say you have a game about ducks, a sort of *Duck Game* if you will. Your ducks need to be able to move around and flap their wings, they need to quack, and they need to occasionally pick up high-powered weaponry with which they can roast other ducks. However, one kind of duck isn't enough for you! You have a grander vision than that.

So, you create a Duck class that contains all the basic things a Duck does: quacking, flapping, murder. And then you create a special Anti-Gravity Duck class for a gamemode where the ducks are in space. And *then* you create a BomberDuck class for your goofy explosives-driven minigame.

And then you say, hey, what if we *combined* Ducks In Space and BomberDuck? Brilliant idea, but you have a problem. See, the BomberDuck and the AntiGravDuck both inherit from the base Duck. This works perfectly fine, because neither duck required behavior from anything other than the base Duck. But *now* you want a duck that combines behavior from AntiGravDuck *AND* BomberDuck. And in most languages, you can't inherit from more than one class! Should you create an AntiGravBomberDuck that inherits from Duck, and thus have to copy and paste everything from BomberDuck and AntiGravDuck, *or* should you inherit from one and copy from the other? Will you remember who's inheriting from whom? And if you have to change something in BomberDuck after AntiGravBomberDuck gets added, will you remember to adjust AntiGravBomberDuck to account for that change?

This is a bit of a contrived example, but the fact remains that OOP works best when you can have most of the behavior in one "parent" class, and only need to adjust a few properties in each "child" class. Once you get into situations where you need a more complex family tree, everything gets messy. Enter the mixin.

You remember how OOP saves you the headaches of copy-pasting code? Mixins--at least, the ones I've used--let you automate the copy-paste process, simultaneously removing the human error that causes the headache while *also* avoiding the question of which object is the parent.

### Let's go over that duck example again.

You still have a Duck that handles some basic behavior. But now, instead of writing a *class* that contains the AntiGravDuck behavior, you write a *mixin* that contains that anti-grav code, and then create an AntiGravDuck that has that mixin. It sounds like more effort up-front, and it is--you have to think ahead far enough to know that you'll want that anti-grav code elsewhere.

After doing the same for the BomberDuck, you now have 3 ducks and 2 mixins--a Duck, a BomberDuck with the Bomber mixin, and an AntiGravDuck with the AntiGrav mixin. But then you go to add the AntiGravBomberDuck, and the magic starts.

You already have the AntiGrav code ready to go, and the Bomber code ready to go, so the AntiGravBomberDuck is just a Duck with *both* of those mixins instead of just one. Boom. Done. None of that complicated waffling about inheritances.

And the kicker is, depending on how you structured those mixins, you may even get to use them on non-Duck objects! Maybe you want some levels to have floating robots in them--the AntiGrav mixin contains just the logic for not having gravity, so you slap it onto the robots and now you have antigrav robots, without having to re-write anything or inherit from anything.

### Enough about ducks--how does this apply to HWRK?

I have a number of neat little behaviors that work really well as mixins. For example, the Serum drops scale up as their value increases. I wanted to do the same for health pickups. Moving that logic to a mixin makes it easy to use that behavior on both kinds of item *without* having to worry about who inherits from whom. And if I need to change how the orbs scale, I have one convenient place to make that change. I'm thinking about moving my monster logic to a mixin as well, so I can rapidly prototype monsters using the stock Doom roster as a base--though I'll have to replace all of Doom's stock content eventually, I might benefit from getting stuff into a testable state faster.

I wanted to give you guys some insight into the programming and software engineering side of things, because...well, I can't *always* be showing off visual stuff. Every part of the project is important. Visuals alone do not create a game; you can't will a screenshot into interactivity.