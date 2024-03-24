# Proximity
!!! info end
    ``game.ServerStorage.Modules.Proximity``

## ``:OnSafeTriggered(prompt: ProximityPrompt, callback)``
Does some checks, like whether there's a Character, HumanoidRootPart, if they're being carried or are Ragdolled.
<br>Then this hardcoded compares the proximity range...
<br>If successful, will run and return the provided ``callback``.

### Returns
* Result from ``callback`` or nothing if failed.