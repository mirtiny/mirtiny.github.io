# Badge
!!! info end
    ``game.ServerStorage.Modules.Badge``

A utility that can gets and award Badges, but also updates the Player's Stats for storage.

## ``:DoesPlayerHaveBadge(ply: Player, badgeId)``
### Returns
* Can return ``boolean``


## ``:AddBadgeRegistry(ply: Player, badgeId)``
Creates a ``BoolValue`` inside the Player's Stats, if they don't already have it.

## ``:AwardBadge(ply: Player, badgeId)``
Awards a Badge if the player doesn't already have it in their Stats.

!!! note end
    This is probably not good if Badges get deleted from the inventory.