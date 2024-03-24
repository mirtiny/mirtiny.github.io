# Ragdoll
!!! info end
    ``game.ServerStorage.Modules.Ragdoll``


## `:SetRagdoll(plyChar: Model, enableRagdoll, duration, trip: boolean)`
Ragdolls the player.

### Parameters
* ``plyChar``: The character model.
* ``enableRagdoll``: Could be prevent Re-Ragdolling. If set to ``true``, it won't ragdoll if already ragdolled.
May be for ``Utility:ChangeStat`` to ragdoll the player, if this is set to ``false`` with a duration.
* ``duration``: How long the character should be ragdolled for.
* ``trip``: Whether to trip the character. Enabled ``Humanoid.PlatformStand`` on the client.


## `:RemoveRagdoll(plyChar: Model)`
Unragdolls the player character. The rig is kept, for flexible ragdolling and unragdolling.


## `:Trip(plyChar: Model, duration)`
!!! info end
    Calls :SetRagdoll(), with pre-set parameters.
    No duration will just keep them ragdoll'd


## `:Clear(plyChar: Model, bClearCompletly)`
!!! info end
    Removes the rig created by ``:RigPlayer()``
    It's advised to clear the ``RiggedUser`` on the character's humanoid, or use ``bClearCompletly``.


## `:RigPlayer(plyChar: Model)`
Creates the physic instances required for a ragdoll to even work.

!!! warning end
    Check for the Humanoid's Attribute ``RiggedUser`` of the boolean type first. Because it could already be rigged.
