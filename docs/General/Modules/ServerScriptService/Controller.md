# Controller
!!! info end
    ``game.ServerScriptService.Neighborhood.Controller``

This Module controls how things work in the Neighbors gamemode. e.g. setting states and matching people. Keeping track of occupied houses and etc.

!!! note end
    When this Module finished loading. The Workspace's Attribute ``PlaceLoaded`` gets set to ``true``.


## ``:GetControllerPlayersDataTable()``
### Returns
* The players data table stored by the Controller. The data the Controller uses to process things.


## ``:MatchPlayerPairTogether()``
Matches two players together and reserves a house. This is also ran by ``:Run()``.


## ``:SendPlayerGroupPairToPlace(place: Model, group1, group2)``
Sends groups to a House. This doesn't reserve a place or set it active.



## ``:SetState(ply: Player, state, force: boolean)``
Sets a Player's State, which also modifies the Player Attribute ``State``.

!!! note end
    A list of states is found in the "Player Attributes" page.


## ``:GetIdlePosition(ply: Player)``
Retrieves ``.Spawn`` from the local stored data. Same as ``IdlePosition`` attribute.

If the player is in a party, the idle position of the party is returned by this function...
### Returns
* Should return the Idle Position that is located somewhere very high in the sky.


## ``:SetMatchTarget(ply: Player, targetPly: Player)``
Changes data and sets the attribute ``MatchTarget``.

## ``:SetActiveMap(ply: Player, map: Model)``
Changes ``data.Map`` for the player's controller data.


## ``:GetQueue()``
Returns all queued players, aslong their Data is loaded and are in the "Queue" State.
### Returns
* ``table: {Player}`` collection of Players.


## ``:GetAvailableMap()``
Returns an available "Place" map.
### Returns
* ``Model`` of the map


## ``:GetSeatPairs(n)``
### Returns
* ``table`` of results


## ``:AddBlacklist(ply: Player, targetPly: Player)``
!!! info end
    Unsure


## ``:PassesVCCheck(ply: Player, targetPly: Player)``
Checks their Voice-Chat status. It's supposed to match if both have VC or not.<br>
But this functions just returns true.
### Returns
* ``boolean``


## ``:GetFilteredList(ply: Player, queue)``
!!! info end
    Unsure

## ``:GetBlacklistCount(ply: Player)``
Gets the Blacklist count from a player.
### Returns
* ``number`` count


## ``:GetPlayingCount()``
Gets the count of how many are _"in-queue"_ and how many are _"matched"_.
### Returns
* ``number``


## ``:GetMatchDuration(ply: Player)``
Gets the match duration using subtraction based on the ``MatchStart`` attribute.
### Returns
* ``number`` duration

## ``GetPotentialQueueSize()``
!!! info end
    Unsure
### Returns
* ``number``

## ``:HasReachedQueueLimit(ply: Player)``
Checks ``data.QueueStart``. Unsure about the purpose.
### Returns
* ``boolean``


## ``:GetPlayerPair(queue)``
Gets a player pair and also removes them from the queue and then returns them.
### Returns
* A tuple, ``player1, player2``


## ``:ResetTarget(ply: Player)``
Resets a target and puts them back into the "in-queue" State.<br>
Also uses ``:AddBlacklist`` for some reason.
!!! info end
    Unsure

## ``:GetAvailableSeat(place: Model)``
Gets an available seat in a Place.
### Returns
* A random seat from the result.

## ``:MoveToSeat(ply: Player, seat)``
Makes a player sit on the seat.


## ``:Run()``
Anyone that is in-queue will be put together eventually.<br>
The queue match algorithm needs at least two people to function. The only exception is Roblox Studio and the Test Game.

!!! info end
    Unsure


## ``:Skip(ply: Player)``
Makes someone matched skip.<br>
Resets the target and puts them back into the queue.

## ``:GetHouseType()``
Returns the House Type. Seems to be for house re-skins.<br>
This is used by ``:GetHousePreset()``

## ``:GetHousePreset()``
### Returns
* ``Model`` of the house.


## ``:Init()``
This is ran by the module itself.


## ``:GetAvailableSpawn()``
Gets an available spawn. Unsure about the use.<br>
When a player leaves the game, their spawn gets made available.

### Returns
* ``Vector3`` position.

## ``:RegisterCharacter(character: Model)``
Registers a character and puts the player in Idle state.<br>

When ``PlayerAdded`` this function gets called when ``CharacterAdded`` then gets invoked.


## ``:GetPlayersDataTable()``
### Returns
* A table with every player's data about the controller.