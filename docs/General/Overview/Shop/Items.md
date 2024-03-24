# Items
!!! info end
    The Items are stored in ``game.ReplicatedStorage.Assets.Data.Store.Items`` along with other things.


## Adding an Item

There's an exported type in the ModuleScript, that aids in creating a new item.

!!! info end
    ```lua
    export type Item = {
        Display: string,
        Price: number,
        Description: string,
        Icon: string,
        Tags: {string}?,
        LimitedTime: { 
            Start: number,
            End: number 
        }?,
        Group: {
            Name: string,
            Order: number
        },
        Toxic: boolean,
        QuestItem: boolean?,
        Skins: string?,
        Offsale: boolean?,
        VerifiedOnly: boolean?,
        AdultOnly: boolean?,
        Original: number?,
        GroupOnly: boolean?
    }
    ```


The table key should match the actual name of the Tool inside ``game.ServerStorage.Assets.Tools``.

???+ example end
    Here's an example:

    ```lua
    ["Invisibility Potion"] = {
		Display = 'Invisibility Potion',
		Price = math.huge,
		Description = "Makes you invisible.",
		Icon = TEMPICON,
		Offsale = true,
		Group = Type.Item.Normal,
		Toxic = false
	},
    ```