---
layout: post
title: "A Balancing Act - Making a Balanced and Fair Game"
published: true
image: /assets/images/2026-04-25-balancing-act/mh3-131-powerbalance.png
---

One hurdle in making a game that every designer must overcome is balancing their game to make sure that there are no grossly overpowered strategies.

How does a designer achieve this? Let's find out!

![Powerbalance](/assets/images/2026-04-25-balancing-act/mh3-131-powerbalance.png){:.my-class}

<!--more-->

### What We Mean When We Talk About Balance
What is balance? Simply put, balance means that any given strategy has a chance at succeeding. 

Balance is important because it allows different gameplay and strategies. If one strategy is imbalanced and wins the most, then the game becomes about playing that strategy or playing against that strategy.

A game being balanced doesn't mean that one strategy can't beat the other. Take Rock Paper Scissors for example. From the perspective of Scissors, Rock is grossly overpowered. It has a 100% win rate against Scissors!

If Rock didn't have Paper to balance it, then yes, the game would be imbalanced. But it does!

As a balance exercise, try playing a Rock Paper Scissors game, but instead of Paper beating Rock, Rock and Paper tie.

Spoiler alert: Rock then becomes the best play. Everyone eventually figures this out, and then everyone picks Rock. Then you tie forever!

### Double or Half -- Don't Inch Your Way to Balance!
When you have a value you know is out of whack and you want to adjust it, you don't want to make small tweaks. Instead, take your value, and double (or half) it. You'll most likely overshoot your target and overcorrect, but then you have a bounds of what value is overpowered, and what value is underpowered.

If you have a card you know is unbalanced, take a value and double or half it. Then do your playtest. Each iteration is valuable, so we want to get to the correct value as quickly as possible. Most likely, you'll find that you've overcorrected. That's good! Note the value you tested with that time, and the value before. You know the correct answer is somewhere between there.

### Levers to Pull
When balancing cards, you need to know which levers to pull. What is making the card so strong? And what surface area do we have?

If we're balancing a Hearthstone card, we have four well defined levels.

Mana Cost, Attack, and Health are all numerical values that we can add or subtract to. And with our formula, we know that Mana is a bigger lever to pull than adjusting the attack and health.

Abilities can also be adjusted, although theirs is a bit fuzzier to measure. What we can do is map each ability to a value. This helps when comparing abilities to more concrete levers.

### Pivot Point
One helpful technique is to have one card be your "pivot point." This is a card that will always stay the same. Don't touch it!

This gives you the ability to have a comparison point for any card you balance. By having one point of comparison, you can see how strong or weak a new design is.

This helps you more easily make balance decisions. Are you comparing a new design against every single other card you've made? Or do you only have to make one comparison to make that call?

Generally, your pivot point card should be simple and easy enough to understand. It should also have a constant power level. If you're balancing against a card that's bad in some situations, but can scale really well, than you can have a hard time.

Let's consider balancing the first set of Hearthstone. I'll take one of my favorite cards, and declare it to be our pivot point. Behold, the Chillwind Yeti!

![Chillwind Yeti](/assets/images/2026-04-25-balancing-act/chillwind-yeti.png){:.my-class}

### Assigning Value Mathematically
Let's take a look at our capstone creature. Mr. Yeti is a vanilla minion (vanilla meaning it has no special abilities) with 4 Attack and 5 Health, and it costs 4 Mana to cast.

Another technique is to take a card and assign it a value. What do we mean? Let's look at Hearthstone's first set.

Funnily enough, we can see that there is a formula for the value of a card.

`Value = 2 * Mana + 1`

Mana here is the mana cost of a card. A 2 mana card should have 5 value, a 3 mana card should have 7 value, a 4 mana card should have 9 value, and so on.

Value here requires more definition. How exactly are we defining value?

Value is equal to the Attack of a card plus the Health of the card, plus the Abilities of the card.

We could rewrite our value equation like so:

`Attack + Health + Abilities = 2 * Mana + 1`

Attack and Health are easy to see. They're printed on the card.

How do we judge abilities? This one is a bit fuzzier, but we can make some assessment based on the cards we see. Divine Shield is worth about one value point, or about 1/2 a mana cost. Drawing a card when entering is worth about 3 value points, or 1.5 mana.

Chillwind Yeti follows this design, as it has 4 Attack, 5 health, and no abilities, and a mana cost of 4.

`4 Attack + 5 Health + 0 Abilities = 2 * 4 Mana + 1`

Now that we have a baseline level of power from our pivot point, we can look at other cards for balance. Let's take a look at Ogre Magi, a card that I relate to closely.

![Ogre Magi](/assets/images/2026-04-25-balancing-act/ogre-magi.png){:.my-class}

Ogre Magi costs 4 mana and is a 4 Attack and 4 Health minion with an ability of *Spell Damage +1*. This means that if you cast a spell like Fireball for 6 damage, and you control an Ogre Magi, its Spell Damage ability will increase the damage from 6 to 7.

We can plug Ogre Magi's information into our value formula and see that it's balanced like the Chillwind Yeti.

`4 Attack + 4 Health + 1 (Spell Damage +1) = 2 * 4 Mana + 1`

Abilities aren't all weighted equally. Let's look at another 4 mana creature, Gnomish Inventor.

![Gnomish Inventor](/assets/images/2026-04-25-balancing-act/gnomish-inventor.png){:.my-class}

Gnomish Inventor costs 4 mana and is a 2 Attack and 4 Health minion with an ability of drawing a card when it enters play. If we weighted drawing a card the same as Spell Damage +1, then this card would be very weak in comparison. However, it turns out drawing a card is pretty good! So good in fact, that we can weight it three value points, as opposed to 1.

`2 Attack + 4 Health + 3 (Draw a Card) = 2 * 4 Mana + 1`

Let's look at a card that combines my favorite mythological animal with my favorite color, Azure Drake.

![Azure Drake](/assets/images/2026-04-25-balancing-act/azure-drake.png){:.my-class}

Azure Drake costs 5 mana and is a 4 Attack and 4 Health minion with an ability of drawing a card when it enters play, and it has Spell Damage +1.

`4 Attack + 4 Health + 3 (Draw on Enter) + 1 (+1 spell damage) > 2 * 5 Mana + 1`

Wait a minute -- this isn't an equal value equation! Azure Drake has 12 value points, but it should only be allotted 11 due to its mana value of 5.

### It's Not Gonna Be Perfectly Balanced
It's okay to have a game that's not totally balanced. It's also probably not possible to have a completely balanced game. Plus, balance can change over time as new strategies develop.

Let's take a look at Sen'jin Shieldguard against Booty Bay Brawler.

<div class="double-line-wrapper">
  <img src="/assets/images/2026-04-25-balancing-act/senjin-shieldmasta.png" alt="Sen'jin Shieldmasta, a Hearthstone Card">
  <img src="/assets/images/2026-04-25-balancing-act/booty-bay-bodyguard.png" alt="Booty Bay Bodyguard, a Hearthstone Card">
</div>

The Sen'jin Shieldguard costs 4 mana, meaning that it can get 9 points of value. It has 3 Attack, 5 Health, and the ability Taunt. We can write its value expression at `2 * 4 + 1 = 8 + Taunt`.

The Booty Boy Bodyguard costs 5 mana for 11 points of value. It has 5 Attack, 4 Health, and the ability Tault. We can write its value expression as `2 * 5 + 1 = 9 + Taunt`.

But wait a minute -- if we take a closer look, these cards are not equally balanced. Sen'jin Shieldguard only uses 1 value point to get Taunt, while Booty Bay Bodyguard uses 2 value points to get Taunt. If Booty Bay Bodyguard were balanced like Sen'jin Shieldmasta, then it would have 5 Attack and 5 Health.

This isn't an oversight. Some cards can simply be better than others. It's okay! In fact, Hearthstone game director Ben Brode specifically said that a game can have bad cards.

![Ben Brode Tweet](/assets/images/2026-04-25-balancing-act/ben-brode-screenshot.png){:.my-class}

The reason for this is that we want players to be rewarded for analyzing cards. If every card is perfectly balanced, then it might not matter what you play. But if you have some cards that are slightly more powerful than others, then players who spend their time thinking and analyzing your game can find better cards, and are rewarded.

To be clear, we don't want to have cards or strategies that are so strong that they blow everything else out of the water. In our example above, Sen'jin Shieldguard only has one extra value point above its comparison, Booty Bay Brawler. If Sen'jin Shieldguard had 5 Attack, 4 Health, and Taunt for 4 mana, then there would never be any reason to play Booty Bay Brawler, and we'd say Sen'jin Shieldguard is overpowered. 

### Your Job Is To Make A Fun Game
Remember, at the end of the day, your job as a game designer is to evoke an emotion or experience in your players. Your game is a tool for your players to interact with to feel that experience that you envisioned.

Balancing your game is a process where you make sure that a player doesn't feel punished or frustrated for not picking the "right choice." Generally, you'll want all strategies to be viable and able to win. It's possible that you do choose to make a faction imbalanced -- maybe your game is heroes versus villains and you want players to experience that crime doesn't pay by making the villain team weaker.

But I think we can all think of a game we've played where there was a clearly superior strategy that made the game not fun for everyone else.

Use the techniques above and avoid that in your games! Best of luck, and happy balancing.