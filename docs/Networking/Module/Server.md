[UserCFrame]: https://create.roblox.com/docs/reference/engine/enums/UserCFrame
[CFrame]: https://create.roblox.com/docs/reference/engine/datatypes/CFrame 
[Vector3]: https://create.roblox.com/docs/reference/engine/datatypes/Vector3 
[String]: https://create.roblox.com/docs/luau/strings
[nil]: https://create.roblox.com/docs/luau/nil
[Player]: https://create.roblox.com/docs/reference/engine/classes/Player

# Network Server
!!! info end "The Network server module is located in `game.ServerStorage.Modules.Network`"

A Folder inside ``ReplicatedStorage`` gets created, named "Events", the Server sees the original names, while the Client gets those obfuscated.

An event can only be created on the server using ``:create``.


## `:fire(`[`String`][String], [`Player`][Player]`, ...)`
Fires an event to the specified client.

The function triggers ``realRemoteEvent:FireClient(PlayerToFireTo, ...)``.

### Parameters
* EventName [`String`][String]
* PlayerToFireTo [`Player`][Player]
* `...`

### Returns
* [<span style="color:Tomato"> `nil` </span>][nil]

???+ example end "Example Usage"

    ```lua
    local ServerStorage = game:GetService("ServerStorage")
    local Network = require(ServerStorage.Modules.Network)

    Network:fire("ExampleEvent", Player, "ExampleParameter", "AnotherParameter")
    ```


## ``:fireradius(radius: number, _player: Player | {Player}, event_name: string, ...)``

## ``:fireall(event_name: string, ...)``

## ``::fire_all_except(player: Player, event_name: string, ...)``


## ``:invoke(fail_time: number, event_name: string, player: Player, ...)``
Fires an event to the specified client.

The function triggers ``realRemoteFunction:InvokeClient(player, ...)``.


## ``:listen(event_name: string, _type: EventType, callback: (Player, ...any) -> (...any))``

## ``:create(event_name: string, _type: EventType)``