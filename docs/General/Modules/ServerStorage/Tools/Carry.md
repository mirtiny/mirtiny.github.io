# Carry
!!! info end
    ``game.ServerStorage.Modules.Tools.Carry``

## ``:Carry(plyChar: Model, targetChar: Model, carry_type, ignore)``
Tries to make a character carry a target character. This has checks, and carry won't work depending on certain values.

## Parameters
* ``plyChar``: The player character that should carry people (bully).
* ``targetChar``: The target character that should get carried (victim).
* ``carry_type``: Type of carry or ``"Default"``, see Character Attributes.
* ``ignore``: Don't check if already carrying someone. Useful for things like the _Pitchfork_.

The carrying player character would receive a ``Carrying`` attribute.
And the target player character would receive ``Carried`` and ``CarriedType`` attribute.


## `:GetBullyFromCharacter(plyChar: Model)`
If a player is being carried, this function can be used on that player, to find out who is carrying them, aka. who's bullying them.

### Returns
The player's character, that is carrying the player.


## `:GetVictimFromCharacter(plyChar: Model)`
If a player is carrying someone but we don't know who. We can use this function to find out who is being carried, aka. who is the victim of the carry.

### Returns
!!! info end
    The player's character that is being carried.


## ``:GetCarryType(victimChar)``
Returns the value of ``CarriedType`` or ``"Default"`` of a character that is a victim of a carry.




## ``:Drop(targetChar: Model, forced, bullyChar, ...)``
Seems to be responsible for dropping. Each carry type has another ``:Drop`` function which's parameters differ from this one.

# Parameters

* ``targetChar``: The character that is being carried. The Victim.
* ``bullyChar``: The character that is carrying people.
* ``forced``: Force drop.
* ``...``: Seems to have no use.

## ``:FindVictimAndDrop(bullyChar, forced, ...)``
A combined function that uses ``:GetVictimFromCharacter`` and ``:Drop``.

## ``:FindBullyAndDrop(victimChar, forced, ...)``
A combined function that uses ``:GetBullyFromCharacter`` and ``:Drop``.


## ``:StopCarryAnimation(char: Model)``
Stops the carry animation on a character. Ment for the character, that is carrying a player (bully).