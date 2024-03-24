# Party
!!! info end
    ``game.ServerStorage.Modules.Party``

A Module that does most of the Party system.


## ``:IsPlayerLeader(ply: Player)``
Whether the player is the party leader.
### Returns
* ``boolean``


## ``:ChangePartyLeader(currentLeader: Player, newLeader: Player)``
Changes the Party Leader. This also changes the ``PartyId`` attribute.<br>
The ``PartyId`` is a Player's UserId.


## ``:GetPartySize(partyId)``
Gets the party size...
### Returns
* ``number``

## ``:DoesPlayerBelongToParty(ply: Player)``
If the Player has not PartyId attribute, it would return ``false``.
### Returns
* ``boolean``


## ``:IsPlayerInParty(ply: Player, partyId)``
Checks if the player is in the provided partyId.
### Returns
* ``boolean``

## ``:GetPartyId(ply: Player)``
Gets the value of the attribute ``PartyId`` from a player.
### Returns
* ``number`` PartyId or ``nil``


## ``:RemovePlayerFromParty(ply: Player, no_notif: boolean)``
Removes a player from a party, which also sets their ``PartyId`` attribute to ``nil``.
### Parameters
* ``no_notif``, whether the player should receive a notification.


## ``:AddPlayerToParty(playerToBeAdded: Player, plyPartyOwner: Player)``
Adds a player to a party.

### Parameters
* ``playerToBeAdded``, target player to be added to someone's party.
* ``plyPartyOwner``, this should be the player, that the target gets added to.

It will set the ``PartyId`` to the UserId from ``plyPartyOwner``.

### Returns
* A something useles...?


## ``:DoesPlayerAcceptInvites(ply: Player)``
Whether the player accepts party invites. Gets the ``DisablePartyInvites`` attribute value, but _inversed_.
### Returns
* ``boolean``

## ``:GetPartyMembers(ply: Player)``
Returns the a table with players that are members of the player's party.
### Returns
* ``table: {Player}``


## ``:GetRawPartyMembers(ply: Player)``
Used for reconstructing parties after teleportation.

### Returns
* ``table: {number}``, a table with UserIds instead of Player.


## ``:GetPartyMembersOfState(ply: Player, state)``
Gets Party Members that match provided state.
### Returns
* ``table: {Player}``


## ``:GetPartyMembers_Matched(ply: Player)``
Preset function that does ``:GetPartyMembersOfState(ply, 3)``

## ``:GetPartyMembers_Queued(ply: Player)``
Preset function that does ``:GetPartyMembersOfState(ply, 2)``


## ``:GetPartyLeader(ply: Player)``
If the player is in a party. It checks the ``PartyId`` to figure out who the leader is. Then returns the value.
### Returns
* ``Player``, which is the Party Leader