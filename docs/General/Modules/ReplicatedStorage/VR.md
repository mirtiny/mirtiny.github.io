# VR
!!! info end
    ``game.ReplicatedStorage.Modules.VR``

VR utilities.

Has a ``Heartbeat`` Connection that changes data in its own table called ``velocities``.

## ``:GetHandPosition(user_CFrame: Enum.UserCFrame)``
### Returns
* Result from ``VRService:GetUserCFrame(user_CFrame).Position

## ``:GetHandVelocity(user_CFrame: Enum.UserCFrame)``

## ``:GetRelativeVectorToHead(vector: Vector3)``
### Returns
* Result from ``VRService:GetUserCFrame(Enum.UserCFrame.Head):VectorToObjectSpace(vector)``