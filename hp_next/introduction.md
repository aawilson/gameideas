## HP Next

HP Next is the shitty name I've come up with for my ideas around replacing
hitpoints as a concept. The tl;dr is that I think the concept of HP, while time-
honored and -tested, ultimately fails at being a concept that is versatile
enough to be a good abstraction for representing participation in conflict
systems. This mini-project aims to propose and evaluate a replacement (or
replacements).

## What HP are supposed to do

The concept of HP (i.e., Hit Points) is simple, but here is a compicated
explanation meant to define it in an abstract way:

When participating in any sort of conflict where personal damage is a possible
event, there is a point at which a participant has suffered damage enough times
that they can no longer participate in the conflict.

Hit points aim to represent that through a number. A higher number of hitpoints
means being more able to suffer damaging events without being removed from
conflict. One means by which participants can eliminate other participants is by
decreasing that number. More skilled participants can decrease this number by
larger amounts, either by taking away larger amounts of it at a time ("doing
more damage"), or by succeeding at attempts to take it away more often ("hitting
more").

Depending on how this abstraction is handled, hit points can either be
relatively straightforward ("each time you are hit with a weapon, teh
acculumated damage to your body is represented with hitpoints"), or more
complicated ("a 'hit' in combat may represent taking bodily damage from the
blow, or it may represent being forced into a position where actual bodily
damage is more likely to happen next time"). The former is a very common
interpretation, and even most systems that might not have started with such a
literal interpretation have likely grown that way through time and
solidification of a system's concepts (hitpoints in the first edition of the D&D
miniatures game, for example, can be taken more abstractly than in later
editions, where the exact effects of an action need to be explained to generate
logical consistency with the game's other systems).

In some of the interpretations, incapacitation is more-or-less binary through
the HP subsystem--you are at full capacity until you reach zero hitpoints, after
which you are generally removed from combat. In others, incapacitation is
gradual, and the participants suffer penalties as hp diminishes until they are
fully unable to participate in the conflict at zero.

## What HP represent well

Hitpoints are very simple, and are speedy to implement. Results calculate
quickly, and if your game features combat, they help streamline the commonly
complicated process of resolving combat actions. The binary nature of most
interpretations of the system means calculating state is relatively simple
(alive vs. dead/ko'd), and even more complicated systems rarely do more than add
simple modifiers to player actions. They are great for the typical fantasy trope
of marching through scores of enemies, tirelessly mowing down the BBEG's minions
in an endless chain of battles with nothing but grit and resolve (and,
importantly, little need for recovery). Healing mechanics are simple to
implement and balance, because healing is a simple act of bringing a number back
up toward maximum. Grave injuries that would permanently cripple a real life
character are little more than temporary setbacks while whatever healing
mechanic exists bring the number back up, and once hitpoints are back at
maximum, it's as if the character was never damaged at all.

## What HP do not represent well

The deficiencies of HP lie in verisimilitude: In life, bodily damage has
permanent effects, even after recuperation. Any person who's been in a life-
threatening situation before will be happy to tell you that their objective
isn't to be able to soak enough damage to make it through conflict, but to avoid
getting damaged at all. The above fantasy trope makes for great story-telling,
even in modern settings (the action movie genre is full of it), but other types
of stories are interesting, too. What does it mean for your storytelling if your
system can describe any blow to its participants as a potentially mortal danger?

Also, HP as a concept doesn't map fluidly to other forms of incapacitation. What
does it mean when a rock has fallen on your arm, in the system? What does it
mean when you spent the night before scratching flea bites instead of sleeping?
HP systems can paper over this by handling each case separately, but this can
lead to some unsatisfactory design outcomes (try explaining HD limitations on
Pathfinder's _sleep_ spell to someone who isn't familiar with game design, for
example, or why it's important to have a reliable source of _death ward_ by
level 11). It might be possible to design an abstraction that can model these
other forms of incapacitation in a more generalizable way.

## Here there be dragons!

After this point is where things get less solid and more random. My current
thinking is to split the HP concept in two, into measures of "vulnerability" and
"ability". If you are a participant in a conflict, your goal is to maximize your
ability while minimizing your vulnerability within the contraints of pursuing
your goals. An instant (desirable) tension presents itself from this: Lots of
actions have a trade-off between increasing the capacity for success toward some
goal while simultaneously increasing risk. To focus on fights (a reliably
familiar source of conflict in games), your vulnerability might be represented
by "balance", that is, how much you've allowed your momentum or position to
become disadvantageous. Decreasing "ability" then comes from tiring you out or
injuring you, and increasing vulnerability comes from forcing you into an
unbalanced position. You can give up balance to attempt to force your foes into
some disadvantage (attacks analogous to "charge" or "lunge" abstractions), or
you can try to use superior balance to punish opponents for taking their own
risks ("riposte", "counter" or "attack of opportunity" analogs). The vitality
measure might split into an endurance measure, and a wounds measure, either
where wounds are specific events tied to specific effects, or possibly some
"mortal wound" abstraction that blends together bunches of related effects into
something less fiddly to track.

The roadmap from here is to throw together some scripts to simulate the above,
and try to consolidate some of this into some concrete product that can be
manipulated and iterated on.
