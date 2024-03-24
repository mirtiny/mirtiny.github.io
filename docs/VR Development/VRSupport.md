# Adding VR support to Tools

## You may need to do the following to add VR support:
!!! info end ""
    * Use the [`:ListenForVelocity()`](../Module/Server/#listenforvelocitytoolforces-vector3callback) function to activate tools only when the user swings their arm
    * Add additional button listeners to detect button inputs from the VR controller
    * Modify the `:GetNearestPlayersInFront()` function to use the character’s right hand controller instead of HumanoidRootPart (example: Clippers)

## Other important information:
!!! info end ""
    * You cannot use the character’s Root part orientation, it won’t be accurate. Use [`:GetAdjustedRootPartCFrame()`](../Module/Server/#getadjustedrootpartcframeplayer-cframe)