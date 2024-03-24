# Server
!!! info end
    ``game.ReplicatedStorage.Modules.Server``

Server utilities that server and client can use.

## ``:IsTestServer()``
Whether the game is the PlaceId of the TEST game.
### Returns
* ``boolean``


## ``:GetRealServerType()``
Gets the ``RealServerType`` attribute from Workspace. For some reason these can YIELD, if the Attribute doesn't exist, because it waits.

### Returns
* Result from ``workspace:GetAttribute(RealServerType)``

## ``:GetServerType``
Similar, but gets the ``ServerType`` attribute.

## ``:IsVCServer``
Similar, but this doesn't yield and gets the ``ServerIsVC`` attribute.

## ``:IsAdultServer()``
Whether the game is the 17+ Place Id.
### Returns
* ``boolean``