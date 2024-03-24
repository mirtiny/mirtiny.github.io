# Skins
!!! info end
    The Items are stored in ``game.ReplicatedStorage.Assets.Data.Store.Skins``


## Adding a Skin

There's an exported type in the ModuleScript, that aids with the creation.

!!! info end
    ```lua
    export type Rarity = 'Common' | 'Uncommon' | 'Rare' | 'Royalty' | 'Unique' | '???' | "Collectible";


    export type Skin = {
        Display: string;
        Icon: string;
        Rarity: Rarity?;
        ItemType: string;
        Order: number?;
    }
    ```


The table key should match the actual name of the Tool inside ``game.ServerStorage.Assets.Skins[<PARENT>]``.

???+ example end
    Here's an example:

    ```lua
    	["example_skin"] = {
		Display = "Example Skin",
		Icon = 'rbxassetid://10198213112',
	},
    ```

## Setting up a Skin
Skins are re-skins of items.

``Skins = "example_case"`` this needs to be specified in the Item's configuration.

The Item inside of ``game.ServerStorage.Assets.Tools`` needs to have ``SkinConfig`` Attributes specified, set to a ``boolean`` on ``true``, for everything that should be copied onto the skin as well.

Child Instances do not need the attribute. The actual's Tool script, can be tweaked to load different skin things. The Paper Bag can be an example, for the Paper Bag Models. Even if it's not really a good example.

E.g. if you want to keep the script of an Item, in the Skin as well, it needs the ``SkinConfig`` Attribute. Otherwise things do not get inherited.


## Adding a Case
Skins work with Cases.

???+ example end
    ```lua
        ["example_case"] = {
            Description = "An example case",
            Icon = 'rbxassetid://12502279412',
            IconSize = 1,
            Color = Color3.fromRGB(231, 231, 231),
            Parent = "Invisibility Potion",
            Price = 10,
            
            Items = {
                Common = {"example_skin"},
                Uncommon = {},
                Rare = {},
                Royalty = {},
                Unique = {},
                ['???'] = {},
                Collectible = {}
            }
        },
    ```