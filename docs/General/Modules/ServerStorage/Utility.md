# Utility
!!! info end
    ``game.ServerStorage.Modules.Utility``


## `:ChangeStat(instance: Instance, attrName: string, attrValue, duration)`
Utility to change Attribute values on things.

### Parameters
* ``instance``: What thing should be changed
* ``attrName``: Attribute name
* ``attrValue``: What to set the value to
* ``duration``: How long it should last. Which creates the a string that is "nameTime", "Time" gets additionally added, which tracks the time, that is in os.clock() and duration.

!!! note end
    Why... is it using os.clock()...

## ``:GetRenderCFrame(char: Model)``
Returns an approximate CFrame of where the character actually is in VR.


## ``:GetPlayersInFront(char: Model, range, angle, tool_CFrame)``
Gets players infront of the specified character. Even for VR.

### Returns
* A table with Character Models.

## ``:GetNearestPlayerInFront(char: Model, range, angle, tool_CFrame)``
Similar to before, except the nearest player.

### Returns
* The nearest character model.

## ``:GetNearestPlayerInFrontWithBlacklist(char: Model, range, blacklist, angle, tool_CFrame)``
### Returns
* The nearest character model.


## ``:InSafezone(ply: Player, no_error: boolean)``
Whether a player is in a safezone or not.

### Parameters
* ``no_error``: Whether to display pop-ups _if or if not_ in a safezone.
### Returns
* ``boolean``, whether in a safezone or not


## `:CanPlayerUseTool(ply: Player, targetPlayer: Model, tool)`
Whether a player can use a tool on a specific target player.

This checks things like, if the tool is on a cooldown, or if the target player, is in a safezone.
### Returns
* ``boolean``

## ``:GetPlayerOfTool(tool: Tool)``
Gets the current player of a Tool. From the Backpack or Character Model, for instance.
### Returns
* ``Player``


## ``:GetToolByName(ply: Player, toolName)``
Tries to get a tool from a player, purely based on a string name input.
### Returns
* ``Tool`` or ``nil`` if not found.



## ``:PlayAnimation(char: Model, animation, tween_speed)``
### Returns
* ``AnimationTrack``

## ``:PlayAnimation(sound, part)``
Plays a sound on a part. The sound gets cloned and then returned _(note that it's on a Debris through this function)_.


## `:PickRandomWeighted(chances: {})`

Picks a random weighted value from a given table.

### Returns
Should return the picked **key**.

???+ example end "Example Table"

    ```lua
    local chances = {
        Good = 60,
        Bad = 40
    }
    ```



## ``:JumpscarePlayer(jumpscarer: Player, playerToJumpscare : Player)``
Jumpscares a player.


## ``:SetToolCooldown(ply: Player, Tool, cooldownDuration)``
Sets a cooldown on a tool for the backpack system.


## ``:IsToolCooldown(ply: Player, Tool, no_error)``
Checks if a tool has a cooldown.

### Parameters
* ``no_error`` won't play an error sound if set to ``true``.

### Returns
* A folder. Unsure about its use.


## ``:UnequipVehicleTool(ply: Player)``
!!! info end
    Unsure

## ``:GetStats(ply: Player)``
### Returns
* Something like ``typeof(ServerStorage.Modules.DataStore.Default)`` it's a folder structure. Most likely the Player Stats.