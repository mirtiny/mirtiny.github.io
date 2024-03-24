# Filter
!!! info end
    ``game.ServerStorage.Modules.Filter``

## ``:FilterText(ply: Player, text: string)``
Runs ``:FilterStringAsync(text, ply.UserId)``
### Returns
* A tuple, ``:GetNonChatStringForBroadcastAsync(), true`` or if failed ``nil, true``