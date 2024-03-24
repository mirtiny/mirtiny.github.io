[UserCFrame]: https://create.roblox.com/docs/reference/engine/enums/UserCFrame
[CFrame]: https://create.roblox.com/docs/reference/engine/datatypes/CFrame 
[Vector3]: https://create.roblox.com/docs/reference/engine/datatypes/Vector3 
# VR Client
!!! info end "The VR client module is located in `game.ReplicatedStorage.Modules.VR`"

## `:GetHandPosition(`[`UserCFrame`][UserCFrame]`) → `[`Vector3`][Vector3]
Returns the position of a [UserCFrame][UserCFrame]

### Parameters
* [`UserCFrame`][UserCFrame]

### Returns
* [`Vector3`][Vector3]

???+ example end "Example Usage"

    ```lua
    local ReplicatedStorage = game:GetService("ReplicatedStorage")
    local VRModule = require(ReplicatedStorage.Modules.VR)

    local HandPosition = VRModule:GetHandPosition(Enum.UserCFrame.Head)
    ```

## `:GetHandVelocity(`[`UserCFrame`][UserCFrame]`) → `[`Vector3`][Vector3]
Returns the velocity vector of any of the controllers. This function is often used when adding VR support to tools.

### Parameters
* [`UserCFrame`][UserCFrame]

### Returns
* [`Vector3`][Vector3]

???+ example end "Example Usage"
    ```lua
    local ReplicatedStorage = game:GetService("ReplicatedStorage")
    local VRModule = require(ReplicatedStorage.Modules.VR)

    local HandVelocity = VRModule:GetHandVelocity(Enum.UserCFrame.Head)
    ```

## `:GetRelativeVectorToHead(`[`Vector3`][Vector3]`) → `[`CFrame`][CFrame]
Converts a world position to a position relative to the camera (head).

### Parameters
* [`Vector3`][Vector3]

### Returns
* [`CFrame`][CFrame]

???+ example end "Example Usage"
    ```lua
    local ReplicatedStorage = game:GetService("ReplicatedStorage")
    local VRModule = require(ReplicatedStorage.Modules.VR)

    local WorldPosition = Vector3.new(0, 0, 0)
    local HandVelocity = VRModule:GetRelativeVectorToHead(WorldPosition)
    ```