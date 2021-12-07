---
title: "Puzzle Design"
date: 2021-12-07
draft: false
---

### How the hell do you build a puzzle?
I'm working on an entry for [7 Day FPS](https://itch.io/jam/7dfps-2021). What I'm building right now is something of a puzzle game--which means I have to design puzzles.

I had no idea where to start with designing puzzles. But I've come up with a sort of system, and I think it's working okay so far, so I'm gonna share it.

### Step 1: Verbs.

A puzzle's solution is a sequence of actions, right? So you need to know what those actions are. I started by writing down a list of all the different kinds of actions a player could undertake. In the case of my 7DFPS entry, the player has a gun that shoots a big metal bolt, and then magnetizes it to pull it back to you. So, my list of verbs started like this:

1. Shoot (trigger switches)
2. Pull (traversal, trigger switches again)

Then I added a couple of new types of bolts. The sticky bolt, for instance, sticks to certain objects--which lets you pull yourself around. So now the verb list looks like this:

1. Shoot (trigger switches)
2. Pull Normal Bolt (traversal, trigger switches again)
3. Pull Sticky Bolt (traversal across longer gaps)

Then there's the Heavy Bolt, which arcs, and pulls you to it with more force--but it shatters on impact. So now we have another verb:

1. Shoot (trigger switches)
2. Shoot Heavy Bolt (trigger switches past walls)
3. Pull Normal Bolt (traversal, trigger switches again)
4. Pull Heavy Bolt (traversal through areas with high ceilings)
5. Pull Sticky Bolt (traversal to grapple points)

And then I added a barrel, and a button that will trigger when there's something on top of it, and made it so that the normal bolt can move it around when it pulls on it:

1. Shoot (trigger switches)
2. Shoot Heavy Bolt (trigger switches past walls)
3. Pull Normal Bolt (traversal, trigger switches again, move barrels)
4. Pull Heavy Bolt (traversal through areas with high ceilings)
5. Pull Sticky Bolt (traversal to grapple points)
6. Stand on Button
7. Put Barrel on Button

And then on top of *that*, I made each type of bolt only available through a "bolt giver" that sits somewhere in the level. In this way, I can lock off certain verbs behind doors.

### Step 2: Fragments.

Then I started thinking about how these verbs would translate into steps. I can choose which verbs are available to the player, and I can make some verbs result in changes in the level, i.e., shooting a switch might open a door. I call these combinations of verbs and results 'fragments', as in sentence fragments:

1. Shoot switch to open door
2. Shoot switch (across a gap or through a hole) to open door 
3. Cross a pit with one bolt type to get another bolt type
4. Pull a barrel to clear a path
5. Pull a barrel to trigger a switch

These are starting to look like steps in a walkthrough, which means we're almost ready to make levels.

### Step 3: Bringing it all together.

Now we just need to set up the level. For example, the one I just put together features both special bolt types.

You start with access to the Sticky Bolt, and there's two pits to cross--one with a grapple target, and one without.
Crossing the first pit with the grapple target leads you to a switch, which you can trigger--closing the sticky bolt off behind a door, and opening another door that enables access to the Heavy Bolt. 
Using the Heavy Bolt to cross the other pit gives you access to a second switch, which opens the exit.

This is a simple example, but it's got everything necessary to be a puzzle. This verb-fragment-sentence model shows promise, and I think it'll help me a lot with the levels I need to design for this project. I started on the 3rd, so I've got 3 more days to finish up.