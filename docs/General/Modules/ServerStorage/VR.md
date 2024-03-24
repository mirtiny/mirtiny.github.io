# VR
!!! info end
    ``game.ServerStorage.Modules.VR``

If this Module gets required, it stores own data.

!!! warning end
    Eventually incomplete docs.

## ``:DoesPlayerHaveVR(player: Player)``
### Returns
* ``boolean`` from ``:GetAttribute("VR")``


## ``:GetUserCFrame(ply: Player, user_CFrame: Enum.UserCFrame)``
### Returns
* Apparently ``CFrame``

## ``:GetWorldUserCFrame(player: Player, user_cframe : Enum.UserCFrame)``
### Returns
* Result from ``self:GetUserCFrame(player, user_CFrame)``

## ``:GetAdjustedRootPartCFrame(ply: Player)``
### Returns
* A result from a ``CFrame.lookAt``

## ``:GetAdjustedRootPartCFrameWithoutY(ply: Player)``
### Returns
* A result from a ``CFrame.lookAt``

## ``::UpdateUserCFramesFromPacket(ply: Player, packet)``

## ``:ListenForVelocity(tool: Tool, velocity, callback)``
Creates a ``RemoteEvent``. Unsure about the purpose.