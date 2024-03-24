[UserCFrame]: https://create.roblox.com/docs/reference/engine/enums/UserCFrame
[CFrame]: https://create.roblox.com/docs/reference/engine/datatypes/CFrame 
[Tool]: https://create.roblox.com/docs/reference/engine/classes/Tool
[Player]: https://create.roblox.com/docs/reference/engine/classes/Player
[Function]: https://create.roblox.com/docs/luau/functions
[Table]: https://create.roblox.com/docs/luau/tables
[nil]: https://create.roblox.com/docs/luau/nil

# VR Server
!!! info end "The VR server module is located in `game.ServerStorage.Modules.VR`"


## `:GetUserCFrame(`[`UserCFrame`][UserCFrame]`) → `[`CFrame`][CFrame]

!!! danger end "This function should not be used!"

Returns the controller [`CFrame`][CFrame]. 

### Parameters
* [`UserCFrame`][UserCFrame]

### Returns
* [`CFrame`][CFrame]

???+ example end  "Example Usage"
    ```lua
    local ServerStorage = game:GetService("ServerStorage")
    local ServerVRModule = require(ServerStorage.Modules.VR)

    local UserCFrame = ServerVRModule:GetUserCFrame(Enum.UserCFrame.Head)
    ```

## `:GetWorldUserCFrame(`[`UserCFrame`][UserCFrame]`) → `[`CFrame`][CFrame]

!!! danger end "This function should not be used!"
!!! info end "This function is identical to the one above currently."

Returns the controller [`CFrame`][CFrame]. 

### Parameters
* [`UserCFrame`][UserCFrame]

### Returns
* [`CFrame`][CFrame]

???+ example end  "Example Usage"
    ```lua
    local ServerStorage = game:GetService("ServerStorage")
    local ServerVRModule = require(ServerStorage.Modules.VR)

    local UserCFrame = ServerVRModule:GetWorldUserCFrame(Enum.UserCFrame.Head)
    ```

## `:ListenForVelocity(`[`Tool`][Tool]` `[`Forces <Vector3>`][Table]` `[`Callback`][Function])

Runs the callback function when the user swings their arm or arms in a certain direction or with a certain amount of force.

### Parameters
* [`Tool`][Tool]
* [`Forces`][Table]
* [`Callback`][Function]

### Returns
*  [<span style="color:Tomato"> `nil` </span>][nil]

???+ example end "Check the following tools for examples"
    * Slap
    * Shove

???+ example end "Example Usage"
    ```lua
    local ServerStorage = game:GetService("ServerStorage")
    local ServerVRModule = require(ServerStorage.Modules.VR)

    ServerVRModule:ListenForVelocity(Tool, {Vector3.new()}, function()
        -- Do whatever
    end)
    ```

## `:GetAdjustedRootPartCFrame(`[`Player`][Player]`) →`[`CFrame`][CFrame]

Returns the character’s real root part CFrame adjusted for VR.

### Parameters
* [`Player`][Player]

### Returns
* [`CFrame`][CFrame]

???+ example end "Example Usage"
    ```lua
    local ServerStorage = game:GetService("ServerStorage")
    local ServerVRModule = require(ServerStorage.Modules.VR)

    local AdjustedCFrame = ServerVRModule:GetAdjustedRootPartCFrame(Player)
    ```

## `:GetAdjustedRootPartCFrameWithoutY(`[`Player`][Player]`) →`[`CFrame`][CFrame]

Returns the character’s real root part CFrame adjusted for VR projected onto the XZ plane.

### Parameters
* [`Player`][Player]

### Returns
* [`CFrame`][CFrame]

???+ example end "Example Usage"
    ```lua
    local ServerStorage = game:GetService("ServerStorage")
    local ServerVRModule = require(ServerStorage.Modules.VR)

    local AdjustedCFrameNoY = ServerVRModule:GetAdjustedRootPartCFrameWithoutY(Player)

    ```