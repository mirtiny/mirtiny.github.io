# Server
!!! info end
    ``game.ServerStorage.Modules.Server``

Server utility, also for Teleport and Listing.

Utility for Listing would include, operations done to a Memory Store, so that data about the server list can be retrieved across game instances.

A ``Heartbeat`` Connection gets created, that updates Server data of the own server this module is ran in.


## ``:GetTick()``
Gets the server's tick. This is useful for syncinc things to Clients.

### Returns
* ``os.time()`` from the server.


## ``:IsServerExpired(packet, job_id)``

## ``:GenerateUniqueIdentifier()``

## ``:IsCurrentIdentifierUnique()``
### Returns
* ``boolean``

## ``:GetServerInfoFromId(placeId: number)``
### Returns
* A ``tuple``, ``serverInfo, name: string``. Name can be ``VC`` or ``NON_VC``.


## ``:GetMostPlayersCountry()``


## ``:BuildServerPacket()``
This is ran by the Module itself upon ``require()``.


## ``:EncodePacket(packet)``
### Returns
* Encoded packet table data.

## ``:DecodePacket(packet)``
### Returns
* Decoded packet table data.


## ``:FilterServerList(server_list)``
Makes modifications to the provided ``server_list`` argument.

## ``:GetLatestServers()``
Gets something from a Memory Store. But this doesn't return.
### Returns
* Returns ``true`` if succeeded.


## ``:SendServerPacket()``
This could be sending the own server packet, from where this Module is ran.


## ``:BuildServerMap()``
Organized all servers into a map.


## ``:SendPlayerToJobId(player, place_id: number, job_id: string, teleportData: any)``
Runs ``TeleportService:TeleportToPlaceInstance(place_id, job_id, player, nil, teleportData)``.

## ``:SendPlayerToPlace(player, place_id: number, teleportData: any)``
Runs ``TeleportService:Teleport(place_id, player, teleportData)``.