# Troubleshooting
Figure out why you're running into problems.
- - -

<br>

## Customized Support

Use the ticket system on the Discord Server<br>Or voice your issue in flexkit-chat channels.

* ### [**SERVER INVITE**](https://discord.gg/DBJASMe7aZ)

<br>


- - -
## Design Paradigm
- - - 
+ FlexKit is designed with "lazy-loading" for its data linking. This means that Blender data blocks and properties are not directly referenced by FlexKit. There is no instancing when linking data from Blender with FlexKit via Configuration. However, validating the data is done at certain key UI events such as when selecting an item from the Configuration list, or right before export. Any erroneous configurations will be flagged and highlighted in red. Details will appear in the ERROR Section. 

+ FlexKit includes built-in troubleshooting with suggested actions displayed with the error (click "More Info" in the ERROR Section). If applicable to the error, the UI buttons involved with the recommended actions are also highlighted for easy navigation.
Details of the Export operations are logged to console (timestamped). Empty export results, where no animation is detected, will trigger a WARNING to display on the bottom of the Blender UI.

- - -

#### FlexKit's internal workflow is as follows:

1. `Create Configuration` (`Add Target`) ->
2. `Log Target (MESH or ARMATURE)` -> 
3. `Log Driver (optional)` -> 
4. `Scan Target for SUBTARGETS` and `log SUBTARGETS` -> `(standby for user input)` -> 
5. user may: `enable/disable subtargets`, `alter Export Options`, `create more configurations`, `proceed to work normally on their project`, `save and closer blender`
5. LOOP(`Validate that Target and Driver names exist in scene`, `validate Subtargets exist on Target`) at key UX/UI events
6. FOR EXPORTING: 
    - `Log States (eg. framerate, start/end frame, auto-keyframe, etc..)` -> 
    - `Prepare to Export (use Export Options)` -> 
    - `Sample` -> 
    - `Restore States` -> `Render to string` -> `Output to file`

<br>

At any one of these steps something can go wrong. FlexKit should perform self-checks and validations during operation. Errors should display in the `ERROR Section` (see [**panel guide**](panel-guide.md)). Clicking `More Info` will bring up the built-in troubleshooting feature.

During export, FlexKit should output details to console. Display your Blender console to possibly get more insight into your unexpected result.

If your animation doesn't look right or if any python or Blender built-in error message shows up during operation of the FlexKit, please check the [**common application errors**](#common-application-errors) and [**common animation errors**](#common-animation-errors).

<br>

#### **Some Examples:**

+ E.g. If you change the name of a mesh and then try to export it, on validation FlexKit will inform you that the mesh no longer exists. The add and edit buttons will be highlighted. 

+ E.g. If you change the name of a bone in an armature, then on validation, you will be informed that the configured bone is missing, "Filter Bones" will be highlighted and "Refresh Bones" in the popup will be highlighted. 

+ E.g. Your configured target does not animate and your export options do not pad, or include Temporal+ enabled but the target never leaves rest position. The resulting XML file is blank. The exporter does not output a file and triggers a WARNING message that says that the file was not outputted.

<br>

- - -
        
## Limitations and Known Bugs
- Exporting files relative to the Blender project is only possible if the file is saved. Saving the file is mandatory for the operation of FlexKit.
- FlexKit does not support accurate animation of any "root" bones. Try to never pose or animate the "root" bone (top-most level parent bone) of any armature when using FlexKit. This is because location data for animations is done relative to the parent. Since root bones don't have any parents, their animation data does not coordinate relatively to anything besides its attachment point to any external skeleton. The attachment point coordinate systems are unpredictable in IMVU, so animating the root bone will give very unpredictable, and often frustrating, results.
- If you export an avatar animation as FBX using the IMVU STUDIO TOOLKIT for Blender, the head mesh (named "Morph") will alter one of its shape-keys. FlexKit will throw an error during validation and require a refresh of shape-key subtargets, resulting in removing the old (unimportant) shape-key and adding a new (unimportant) shape-key. You may disable the new shapekey to keep your XML optimized. This new shapekey does not actually control any morphs.
- In post-processing optimizations: designed to limit unneccessary characters like '0' in values such as 1e-03, reporting them to 1e-3 instead. However sometimes a 'rogue zero' slips in. This bug does not affect accuracy. It is currently being investigated as its difficult to reproduce. 
- Sometimes, the first frame of the animation will "glitch" into an awkward position, and then resume normal playback. It lasts only one frame. This is because some pole targets for IK-systems don't resolve properly when evaluating depsgraphs for the first frame. Put your frame marker at the start of the animation before export, or export twice in a row. This bug is not present with quick exporting. This bug is being actively investigated. 

<br>

- - -

## Common Application Errors

1. File not saved | **SOLUTION:** Save your project somewhere

2. Changing the name of, or removing, the Target/Driver | **SOLUTION:** Go into edit and reselect the Target OR remove affected Configuration

3. Changing the name of, or removing, or adding Subtargets | **SOLUTION:** Refresh Subtargets, FlexKit repopulates the list automatically

4. If attempting to Auto-Detect an IMVU Animation Tool template, a WARNING may appear saying that the template was not detected. This can occur if the object names of "Anim", "Morph", or "Control_Armature" are changed or don't appear in the scene.

<br>

- For High filesize or long export time | **SOLUTION:** Lower `resolution`, disable `Human Readability`, shorten animation duration.

<br>

FlexKit should **NOT** throw any python built-in errors during operation. If you encounter any such error and suspect that it is because of FlexKit, please [**contact me**](index.md#contact). Your input will be valuable.

<br>

- - -

## Common Animation Errors

1. **Jittery, Unsmooth, or Mildly Inaccurate Animations** - Your animation doesn't look smooth; jitters, moves at a weird speed, or has mild inconsistencies (mildly inaccurate hand/arm placements for example).
    - **Solutions** : 
        1. Try increasing `Resolution` (in the `Export Options` panel) to see if it improves results.
        2. Ensure that your `Frame Rate` is set to 30 fps.
        3. Change, enable or disable settings in `Export Options` -> `Resolution Settings` -> `Post-Processing Styles` (see [**panel guide**](panel-guide.md) or search "post-processing style" in the documentation for more info on this setting)

2. **Messed-up Avatar/Mesh** - Your animation causes heavy distortion of your avatar or mesh, or doesn't line up properly.
    - **Solutions** :
        1. Ensure that `Accessory Export` option matches the desired animation type. If you are exporting from the accessory template, or deriving from an accessory-type parent (pets included), then this should be enabled. Otherwise keep it disabled. 
            - **NOTE**: pose-packs are CLOTHING derived, and avatars are AVATAR derived so keep this disabled for avatar pose animations
        2. Ensure your armature only has 1 root bone (bone with no parent), this is especially important for custom armatures, like with accessories.
        3. Ensure the root bone in your armature is disabled in `Details` -> `Filter Subsamples (Bones/Shapekeys)`.

<br>

- - -

<br>

Do you need help on something that isn't mentioned here? Do you want to report a bug? You may directly [**contact me**](index.md#contact).

<br>
- - -

## FAQs
- FAQs will show here as they accumulate.
<br><br><br>