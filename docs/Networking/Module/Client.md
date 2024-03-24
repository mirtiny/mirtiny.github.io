[UserCFrame]: https://create.roblox.com/docs/reference/engine/enums/UserCFrame
[CFrame]: https://create.roblox.com/docs/reference/engine/datatypes/CFrame 
[Vector3]: https://create.roblox.com/docs/reference/engine/datatypes/Vector3 
[string]: https://create.roblox.com/docs/luau/strings
[nil]: https://create.roblox.com/docs/luau/nil

# Network Client
!!! info end "The Network client module is located in `game.ReplicatedStorage.Modules.Network`"

Unlike on the Server's Module. This one doesn't have a Folder.

## `:fire(`[`string`][string]`...)`
Fires an event to the server

### Parameters
* EventName [`string`][string]
* `...`

### Returns
* [<span style="color:Tomato"> `nil` </span>][nil]

???+ example end "Example Usage"

    ```lua
    local ReplicatedStorage = game:GetService("ReplicatedStorage")
    local Network = require(ReplicatedStorage.Modules.Network)

    Network:fire("ExampleEvent", "ExampleParameter", "AnotherParameter")
    ```

## `:invoke(`[`string`][string]`...)`
Invokes an event on the server

### Parameters
* EventName [`string`][string]
* `...`

### Returns
* `any`

???+ example end "Example Usage"

    ```lua
    local ReplicatedStorage = game:GetService("ReplicatedStorage")
    local Network = require(ReplicatedStorage.Modules.Network)

    local Result = Network:invoke("ExampleEvent", "ExampleParameter", "AnotherParameter")
    ```


## ``:listen(event_name: string, callback: (...any) -> ...any)``