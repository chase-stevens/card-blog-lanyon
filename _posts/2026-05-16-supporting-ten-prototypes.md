---
layout: post
title: "Supporting Ten Prototypes - A Framework for Organizing Game Designs"
published: true
image: /assets/images/2026-05-16-supporting-ten-prototypes/open-folder.svg
---

I was at a playtesting meetup in Brooklyn, where I had the chance to chat with a veteran game designer that I admire and respect.

He had a few different games with him, so I asked him how many game prototypes he had in the works.

"Oh, about thirty," he said.

Internally, I had a meltdown in my frontal cortex. Thirty prototypes? Thirty?? Here I was, playtesting my second prototype, and feeling guilty for not testing my first.

I asked, "How do you keep track of all of those prototypes?"

He said, "That's a very good question."

That conversation got me thinking about the possibility of being able to talk to a publisher, reaching into a grab bag of ten different games, and being able to pitch whichever one was the best fit for what they're looking for. (Thirty prototypes can come later.)

I've leveled up my prototyping, design, and printing processes. Why not level up my organization and create a framework that would allow me to support ten prototypes?

![Folder Icon](/assets/images/2026-05-16-supporting-ten-prototypes/open-folder.svg){:.my-class}

<!--more-->

### Why Do We Need Ten Prototypes?

Before we get into the requirements and game plan, let's talk about why we want to be able to support and keep organized ten different game designs.

We're not out here trying to roll the dice on getting a game published and increasing our number of rolls. It's better to have one fully polished game that is fun and easy to understand over ten rough prototypes that are clunky and unwieldy. I'm not making this framework for supporting ten prototypes to do a buckshot approach, but rather to be able to make well-designed prototypes one by one and keep them organized.

One reason for this approach is that designing games starts off in a huge possibility space, then tapers off into tweaking and small adjustments. When you're first designing a game, the world is your oyster. Your game can be anything! You start by defining a win condition and game play loop. Maybe it works, maybe it doesn't. You refine, edit, put more rules in place, and before you know it, you have a fun game in front of you. Sure, all the rules aren't fully written down, and maybe you can make some changes. But before you know it, your game has a definition and shape. Your time of throwing ideas against the wall and seeing what sticks is over. Now, you're measuring, tweaking, and changing values to optimize the fun.

Congrats! You've designed a game. However, if you're bringing this game to market, you still have a long road ahead of you. You either have to pitch the game to a publisher, who then will make changes, market, and produce the game, or you'll self-publish and have to do all this yourself.

That's all well and good, but your brain doesn't stop thinking of new game ideas just because this game is done!

You can take that creative energy and make a new game prototype.

Another benefit of having multiple prototypes is that you get to explore new game areas, player motivations, and design space that you wouldn't get to explore with just one prototype.

There's the often cited story of two groups of students in a pottery class. One group was tasked with making just a single pot over the course of the semester. The other group made a different pot every single class. It turns out that the group that was focused on quantity actually made better pots than the group made on quality.

Being able to make multiple prototypes could be a logistical nightmare. However, over time, I've been able to level up my prototyping abilities and printing and cutting. I could go from having a game idea at 9am on a Saturday to having a fully playable prototype in my hands by 5pm (if you want to read more about how I make game prototypes, [check out my post on Squib here](/2026/04/04/card-design-squib/)). Since we've removed the physical barrier, let's remove the mental barrier as well!

### The Gameplan

Before we get into our game plan, let's focus on what exactly we need for a game.
- A prototype. This is the most key part of the process. This will be generated using Squib.
- A rulebook. Helps people play the game when I'm not around (also very important). I use a free set of creative tools called Affinity.
- Marketing materials. We want a publisher to be able to understand, play, and hopefully sell this game on our behalf. To that end, we will want a Sellsheet and a Pitch video
- Versioning. When you make a game prototype, you don't just make one -- you're going to make tweaks and edits and see new things and fix broken parts. To help organize all of the different iterations of the game, organizing prototypes by version keeps our head together.
- A README.md file. This helps us come back to a previous prototype that might have been in the backlog or not had our eyes on it.

What we don't need
- Finished game pieces. We aren't making game files to go to the printer for a 10,000 unit print run.
- Mass market marketing materials. We aren't making kickstarters

For our requirements, we can store each game in its own directory in the file system.

We can also use the software Git to version our game, or at least have backups. We can also store this Git repository on Github as well. This gives us backups and the ability to work on our game across different computers.


The directory would look something like this:

```
game/
├── prototype/
│   └── YYYY-MM-DD-name/
├── rulebook/
│   └── YYYY-MM-DD-name/
├── marketing/
│   ├── sellsheet.pdf
│   └── pitch.mp4
└── README.md
```

In the prototype directory, we will initialize a new Squib project. This will be where we generate our prototypes.

Versioning our prototypes will be the most important, as this is where we iterate the most. I have written a command in my Squib projects to make new version files.

In the rulebook directory, this is where we'll keep our rulebook files. Like in the Squib folder, we'll want to organize materials by version.

Why don't we use git branches as versions? Well, Git is mainly used to track versions of one project over time, and to organize the efforts of multiple people. I work alone, and also I want to be able to track progress over time and easily see past versions, and print them at a moment's notice. With Git, I find it hard to go back in the past, as things may change.

By keeping versions explicit, I can easily jump between different prototypes of the same game and compare and contrast.

Our marketing folder has our materials to help publishers learn about our game. This will mainly consist of sell sheets, one page documents describing our game at a glance, and pitch videos that demonstrate the game in 2-3 minutes.

Lastly, we have our README.md file. This is a document that we can read to get ourselves up to speed quickly for a project that has been in the backlog.

### What Is Most Likely To Change?

I'm not pushing this framework as a finished piece of work that will solve all my problems. I think it's a step beyond an iterative step towards leveling up organization of game ideas and prototypes.

The area that I'm most interested in, and what is most likely to change, will be the versioning system. Right now, it's manually tracked by directory names across different folders. It would be great to be able to create a new version from the game directory and have that propagate across the different folders.

We might also make a simple directory of scripts to help support versioning as well. It would most likely be in Ruby, since Squib is in Ruby and that's what I have the most experience with, but it wouldn't be a big deal for the language of choice here.

I might also make a shared assets folder for art and icons as well. This way, the prototype and the rulebook can have access to the same images without having to duplicate them.

I've taken the first steps towards using this new framework for a new game prototype. It's possibly my spookiest yet. Keep an eye out if you want to playtest, or stay away if you're scared by ghouls and goblins!

<div class="triple-double-wrapper">
  <img class="my-class" src="/assets/images/2026-05-16-supporting-ten-prototypes/energy_00.png" alt="Abaddon Energy">
  <img class="my-class" src="/assets/images/2026-05-16-supporting-ten-prototypes/summons_00.png" alt="Hell Raiser">
  <img class="my-class" src="/assets/images/2026-05-16-supporting-ten-prototypes/summons_01.png" alt="Fire Lord">
</div>