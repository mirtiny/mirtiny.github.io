Roblox [Attributes](https://create.roblox.com/docs/studio/instance-attributes).

# Player
Attributes put inside the Player Instance.

!!! warning end
    **Not all are listed!**


## `AdminSpectating`
**Type:** `boolean`
##### Description
A tweak to unforce your camera to be at places if set to ``true``.<br>
A client-side based attribute.


## `AllowPartyInvitesFromAll`
**Type:** `boolean`
##### Description
Player allows party invites from non-friends.


## `AvatarDeco`
**Type:** ``string``

## `AvatarId`
**Type:** `number`

##### Description
Profile Bio picture image ID.


## `BGDeco`
**Type:** `string`

## `BannerDeco`
**Type:** `string`
##### Description
String ID representation of the Player's selected Banner Decoration.



## `Credits`
**Type:** `number`
##### Description
Player Credits.

## `CurrentInternalMap`
**Type:** `string`

##### Description
Contains the name of the Player's current *Place*. Can be used to find out where a Player's current queued house is at.
<br>If the Player isn't in a house *(e.g. soloqueued, in-queue or other modifications)* it will be ``nil``.

!!! info end
    Changing this value ***only*** for the **Client** will load the props inside a house.<br>
    Changing this value on the **Server** will change the house the player is *supposed* to be in. If the player is not exempt from the anti-cheat, they will be reset.

!!! warning end
    Can be ``nil``, in this case empty string ``""``.


## `DataLoaded`
!!! note end "TODO"
    Wat is this


## `DisableCars`
!!! note end "TODO"
    Wat is this

## `DisableComments`
**Type:** `boolean`

##### Description
If set to ``true``, nobody can submit a comment on that Player's Bio.


## `DisablePartyInvites`
**Type:** `boolean`

##### Description
Whether a Player has Party Invites enabled or not.


## `DisableVRRagdoll`
!!! note end "TODO"
    Wat happens if this is true or something


## `Disabled`
!!! note end "TODO"
    WHAT IS THIS USED FOR<br>
    Someone use CTRL + F in Studio and look for ``"Disabled"`` and lemme know


## `DoubleStar`
**Type:** `boolean`


## `ExemptFromAntiCheat`
**Type:** `boolean`

##### Description
Whether a player's anti-cheat is disabled.


## `ExemptFromGrass`
**Type:** `boolean`

##### Description
Whether a player can walk on grass.


## `EightBitPack`
!!! warning end
    If more Packs are added, the Attributes of the Player will be doomed.<br>
    Someone move this somewhere else 😭😭😭


## `ExtraSlots`
**Type:** `boolean`

##### Description
Gamepass, gives more inventory slots.


## `ExtraSlots2`
**Type:** `boolean`

##### Description
Gamepass.



## `FirstTimeJoining`
**Type:** `boolean`

##### Description
Whether the Player joined for the first time. Probably for the tutorial on the buttons.



## `Friend`
**Type:** `boolean`



## `HideGraffiti`
**Type:** `boolean`

!!! note end "TODO"
    Does this hide ALL Graffiti, with no issues?


## `HideHours`
**Type:** `boolean`

##### Description
Whether a Player's house should be hidden from the Profile Bio.


## `IdlePosition`
**Type:** `Vector3`

##### Description
The Player's Idle Position, that is usually very high in the Sky, on Y Level: ``4000``



## `InVehicleTool`
!!! note end "TODO"
    wat is this


## `InfiniteSkips`
**Type:** ``boolean``

##### Description
Whether the Player has infinite skips.


## `InfiniteSlots`
**Type:** ``boolean``

!!! note end "TODO"
    is this for party invite slots, or inventory?


## `Intoxication`
**Type:** ``number``
##### Description
Something for the 17+ game. Drunk Effect.

!!! note end
    Expected values are ``0`` up to ``1``.


## `Invisible`
**Type:** ``boolean``
##### Description
If ``true`` hides nametag.

!!! note end
    Unsure.


## `LastReward`
**Type:** `number` (UNIX Timestamp)

##### Description
A Player's last daily reward redeem.

Another attribute with similar purpose would be ``LastSantaVisit``.


## `Loaded`
!!! note end
    wat is this


## `MatchStart`
**Type:** `number`
!!! note end
    it's in some time value, but idk which one????

!!! warning end
    Doesn't always exist. Can be ``nil``.


## `MatchTarget`
**Type:** `string`

##### Description
The player's username that they queued up with.

!!! note end
    If it's *natural soloqueue*, they'd be queued up with themselves.<br>
    NOT to be confused with ``soloqueue`` command.

!!! warning end
    Doesn't always exist. Can be ``nil``.


## `MegaParty`
**Type:** `number`
!!! note end
    unsure


## `MicEnabled`
!!! warning end
    This doesn't do anything...


## `MuteMusic`
**Type:** `boolean`

##### Description
Whether Player has loading screen Music muted. ``true`` means it's muted.


## `MuteToolSounds`
**Type:** `boolean`

##### Description
Whether Tool Sounds are muted.

!!! note end "TODO"
    Technical setup for the tools for this to work


## `MuteWeather`
**Type:** `boolean`

##### Description
Whether Weather is muted.



## `OutfitSelector`
**Type:** `boolean`

##### Description
Whether Player has access to the Outfit Selector Gamepass.



## `PartyId`
**Type:** `number`
#### Description
The PartyId the player is in. Which is someone's UserId, e.g. the Party Leader.<br>
The player doesn't have this if they're not in a party.

## `PlayerInvites`
**Type:** `number`

##### Description
A Player's Roblox game invite count.


## `Points`
**Type:** `number`

##### Description
A Player's Profile Points value.



## `ProfileColors`
**Type:** `boolean`

##### Description
If a Player can modify their Profile Bio Colors.


## `Protected`
**Type:** `number`

##### Description
Whether the Player can be affected by Tools. *(you may find some tools just to work)*

Player's that have this on ``true`` can be identified based on their nametag.

![Protected Name Tag](/neighbors-documentation/assets/dev_docs/protected_value_nametag.png)



## `PushToTalk`
**Type:** `boolean`

##### Description
!!! info end
    Reserved


## `Safezone`
**Type:** `boolean`


## `ShowOwnTag`
**Type:** `boolean`

!!! note end
    I forgor a little bit and unsure if client will make this show only, or if set by server


## `ShowProfileOnSpawn`
**Type:** `boolean`

!!! note end
    Why are all settings in the Player's Attributes

## `ShowTitle`
**Type:** `boolean`

!!! note end
    Does this even work?


## `Special`
**Type:** `boolean`
!!! note end
    No clue what this is

## `Spins`
**Type:** `number`

##### Description
!!! note end "TODO"

## `State`
**Type:** `number`

##### Description
A ***client-side*** based *control* for the Player. This is used to manage the behaviour of the Player.
<br>*e. g. if they should see the loading screen or not.*

!!! info end
    Changes to this value will update behaviour. See the description below.

###### States
<table>
<th>Value</th>
<th>Name</th>
<th>Description</th>
<tr>
    <td>1</td>
    <td>Idle <i>(No Activity)</i></td>
    <td>Player sees the loading screen and is not in any queue.</td>
</tr>
<tr>
    <td>2</td>
    <td>In-Queue</td>
    <td>Player is in the queue and in the loading screen.</td>
</tr>
<tr>
    <td>3</td>
    <td>Queued up</td>
    <td>Player can see their own character and control their camera.</td>
</tr>
</table>


## `Streak`
**Type:** `number`

##### Description
The daily reward Streak. Not claiming a Daily Reward, would reset the daily reward streak.


## `StreamerMode`
**Type:** `boolean`

!!! note end
    I think just hides leaderboard


## `Title`
**Type:** `string`

##### Description
A representation of the current string.

!!! note end
    It's a mystery whether, Titles have an ID or just name.

!!! warning end
    Setting this value does not resolve into Custom Titles, such like "Boogle", which is ``boogle``.


## `UpToDate`
**Type:** `boolean`

!!! note end
    checks your Windows Updates (no)


## `UseMasculineTitles`
**Type:** `boolean`

!!! note end
    have not experimented


## `VCOnly`
**Type:** `boolean`

!!! note end
    ????


## `VCOnly2`
**Type:** `boolean`

!!! note end
    ????


## `Verified`
**Type:** `boolean`

##### Description
Shows a star next to a player if set on ``true``, along with playing a sound when opening their Profile Bio.


## `VoiceChatEnabled`
**Type:** `boolean`

##### Description
An automatic assigned value upon Player join.
This will determine whether in a Profile Bio, it should show a 🔇 icon or not, for Player's that got Mic Suspended or have it turned off.
Player's that have this on ``false`` can't hear others nor use mic.