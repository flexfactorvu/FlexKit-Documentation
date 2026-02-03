# Terminology and Technical Details
Below are some terms that have specific context with regards to operation of FlexKit.
- - -

<br>
<br>

- - -
## Accessory Export
+ Changes certain internal calculations of IMVU Bone-IDs and rotationary values to match the format specified for accessory-derived products.

<br>

- - -
## Configuration
+ A bundled set of data used to execute sampling and exporting under user specified conditions 
    - `Target Object` (MESH or Armature)
    - `Subsample` (bone or shape-key)
    - `Driver Object` (optional)
    - and certain Export Options (*File Name*, *Location*, `Overwrite/Increment`, `Pad-First/Pad-Last`, `Temporal+`, `Accessory Export`)

<br>

- - -
## Driver Object
+ Object that, when animated, drives the movement of the target object. FlexKit only uses this driving object to calculate rest pose in *Temporal+* mode (see definition below). 
+ Supports ANY object as driver, although armature-type objects work best. Armature-Type drivers will be articulated back to rest pose and reset world co-ordinates. All other object type drivers will only have world co-ordinates reset based on individual origins. This is restored afterwards. The user does not see this front-end. 
+ Armature-type driver objects with bone collections can specify which bone-collections are used for rest-pose calculations from within the visibility toggles in `Properties Panel` -> `Data` -> `Bone Collections`. If collections are nested, parent-collection visibility settings will recursively overwrite all child-collection visibility settings.

<br>

- - -
## Export
+ The core operation of FlexKit. Combines user specified *Configuration* with native Blender settings and information to yield XML (XAF/XPF) files. 
+ For a selected *Target Object*, in a specified frame range set in Blender: at each frame, for each enabled *Subsample*, it will fetch the appropriate value(s) (location/rotation for bones or weights for shape-keys). 
    - The algorithm will compare this value to the value in the previous and next frames to see if any change has been detected based on a certain threshold set by the *Resolution*. 
    - A positive result will include the sample in the final XML export.  

<br>

- - -
## Human Readable
+ A *Resolution* option. 
+ Refers to the formatting of XML files to include whitespaces/tabs/indents/spaces etc to make it easier for a human to read. 
+ Can be toggled on or off. 
    + ##### Please note that file sizes are vastly reduced when Human Readability is disabled, which is the most optimal result.

<br>

- - -
## Overwrite/Increment
+ Specifies whether the user wants subsequent exports to overwrite to the same file if a file with the same file name already exists, or increment by -XXX suffix (ie -001, -002, etc) at the end of the file name on export to prevent loss of data in old exports. 
+ Overwrite is recommended for a more seamless experience with IMVU STUDIO and IMVU CLASSIC.

<br>

- - -
## Pad-First/Pad-Last
+ Refers to the deliberate inclusion of samples in the start/end frames of the animation sequence. 
+ With *Temporal+*, only enabled subsamples that have been detected as animated will have their start/end samples deliberately included as specified, and static subsamples will be omitted. 
+ Without *Temporal+* all enabled subsamples are first/last padded as specified.

<br>

- - -
## Quick-Export Current Pose
+ A secondary, but equally powerful operation similar to *Export*. 
+ For a given *Target Object*, for each enabled *Subsample*, at the CURRENT FRAME, it will fetch the appropriate value(s) (location/rotation for bones or weights for shape-keys). This allows for extracting multiple single poses from an animation sequence. 
+ All enabled subsamples are included in the final XML output, which is suffixed with an -fXXX format, XXX being the frame number. 
+ Note that this respects *Overwrite/Incremement* settings per frame.

<br>

- - -
## Resolution
+ A combined metric merging the *temporal threshold* and *reporting precision* that is used when sampling. 
    - **Temporal threshold** is calculated as a float of 10^(-Resolution)
    - **Reporting precision** is calculated as a floor-rounded integer of (Resolution + 1) decimal places. 
+ Changes in subsample values accross frames that exceed the temporal threshold will register as animated and yield a result that is reported to the specified reporting precision (decimal place), otherwise the subsample will be omitted for the given frame. 
+ Higher resolution -> Lower temporal threshold (likelihood of more yielded samples) -> Higher file-size. 
+ Decimal places, selection of post-processing algorithms, and *Human Readability* of final files can be overriden in the **Additional Resolution Settings** popover (See **Panel Reference**).
+ GLOBAL SETTING (applied to all *Configurations*). 

<br>

- - -
## Subsamples 
##### (also called `Subtargets`)
+ Refers to the individual data source that yields a single sample. 
+ `ARMATURE` targets have `BONES` as subsamples, yielding a location/rotation pair sample. 
+ `MESH` targets have `SHAPE-KEYS` as subsamples, yielding a single value weight sample. 
+ Individual subsamples can be toggled "on/off" in the **Filter Subsamples** pop-up, to specify whether to include them in sampling/exporting or not.

<br>

- - -
## Target Object
+ MESH or ARMATURE type object in blender. MESH type must have shape-keys.

<br>

- - -
## Temporal+
+ A very specific mode designed to tighten the core temporal detection algorithm. 
+ Performs a rest-pose comparison at the first frame of the sequence as well as keeps track of subsamples that registered movement within the sequence. The rest-pose is relative to the driver object (if present) otherwise the target object's world and pose-mode rest position is used instead. 
+ Subsamples that registered movement will be included in Pad-First/Pad-Last settings. 
+ Recommended for detailed single-animation projects (furniture, avatar poses). *Not* recommended for pose-packs or "replacing" animations because different animation sequences will have different set of bones that register as animated: if trying to replace animations with triggers in VU, missing bone data will not be overridden and will remain moving in the old animation.
<br><br><br>