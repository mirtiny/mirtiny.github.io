# Prompt
!!! info end
    ``game.ServerStorage.Modules.Prompt``

This Module uses a Network event named ``Prompt``.

All of the prompts might just be purple though...

## ``:Prompt(ply: Player, title, msg, duration, autoshow: boolean)``
Sends one of those prompts at the top of someone's screen, e.g. Party Invites.

The target player receives a prompt. The player can then click on the notification which opens a window where they can click on "Yes" or "No". If the duration expires the RemoteFunction will return ``false``, same as if they click on "No".

If they click on "Yes", it will return ``true``.

### Returns
* Result from ``Network:invoke`` which triggers a ``RemoteFunction``.