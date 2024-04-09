---
title: "Hold"
date: 2024-04-09
draft: false
---

### What does it mean when you hold down a button?

It's a dumb question, sure, but it's an important one. Knowing what your inputs *mean* is key, and as a game designer, you are *defining* what your inputs mean. It's also worth asking whether the thing you want is something that can be defined with a different input, for accessibility reasons; some people can't hold buttons down for long periods of time, either because of grip strength issues or because it physically hurts to do so. (The same goes for button mashing! Being able to change inputs is a key feature for accessibility.)

### It means you're paying attention.
One way to look at it is that if you're holding a button, you're paying attention to the game. Dark Souls, for instance, is designed with a block button that you are expected to hold down when you need to block something.

One of the functions of this is that you cannot block something unless you are specifically expecting to block it. If you walk around a corner without holding the block button, and an enemy lunges at you, you're going to eat the hit...because you were not *devoting attention to blocking*. When you see an enemy, you generally hold down the block button, to indicate to the game that you are *aware* that you need to defend.

When serving this function, you don't really need the button to be *held*, you just need there to be some action the player takes to indicate that they're paying attention. A toggleable block button serves the same purpose as holding the button, because the important part is that the player has *chosen to block*.

### It means you're controlling the precise length of an action.

This is how holding jump to jump higher works. You tie the length of the input to the *strength* of the input. Charged attacks also fall under this category.

The thing is, this category usually has a much tighter timing window than the others. You *can't* make jump length a toggle the way you can make blocking a toggle; the best you can do is breaking the jump up into a double-jump, which is a good option in its own right, but is *fundamentally different* from having precise jump height control--you need to be taking this into consideration when you build your inputs.

### It means doing something different.

Sometimes, pressing and holding do different things. If I recall correctly, several of the Metal Gear Solid games differentiated between grabbing someone and choking them out by the difference between a press and a hold. The demo for Out of Action--a deeply interesting cyberpunk FPS--uses held inputs to differentiate between diving into a roll, and diving into a *slide*, which have different implications on your ability to aim or to quickly get out of the way. 

A double-tap can work here--and may be faster to input. However, you might have yet more inputs to map to held buttons, and being able to input an action faster has implications on gamefeel and strategy.

### The simple details are important.

This post was pretty straightforward. You could even argue that this stuff is obvious!

I wouldn't argue that it's obvious, though. And even if it was, it's worth writing down somewhere, because for every person who thinks this is *obvious*, there's probably a hundred who never even thought about it (one of whom might even be the guy who thought it was obvious).