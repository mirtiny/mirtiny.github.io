# Client
!!! info end
    ``game.ServerStorage.Modules.Client``

Looks like a Module for the specialization of custom Roblox method usages. These contain hookable BindableEvents designed for the Server, for handling data.

!!! info end
    Should eventually be done differently?


There's a StarterPlayerScript that is called ``ClientReady``, which sends a RemoteEvent that is also called ``ClientReady``.

**Once firing to that RemoteEvent**, the server will attempt to retrieve the Player's "Stats" located in the ``ServerStorage.Stats`` folder.

Once the Stats have been loaded, the Player will receive a boolean Attribute called ``Loaded``.

## Provided BindableEvents
### ``module.ClientConnected:Connect(func: (player: Player))``
Fired when the Player's ``Stats`` data has loaded.


### ``module.PlayerAdded:Connect(func: (ply: Player, NeighborStats)``

### ``module.PlayerRemoving:Connect(func: (ply: Player, NeighborStats)``

### ``module.CharacterAdded:Connect(func: (ply: Player, character: Model, NeighborStats)``



## ``:GetPlayers()``

### Returns
* A ``table`` value with the Module's collected players. _(doesn't look reliable)_