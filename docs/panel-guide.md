# Panel Guide
Reference for what each button does.
- - -

<br>
<br>

## Visual Index
- - -

<br>

### Main Panels
<table style="margin-left: 0; margin-right: auto;">
    <tr>
        <td>
            </a>
            <a href="../images/overview-1.jpg" target="_blank">
            <img src="../images/overview-1.jpg" style="width: 256px;" />
            </a><br>
        </td>
        <td></td>
        <td>
            </a>
            <a href="../images/config-panel.jpg" target="_blank">
            <img src="../images/config-panel.jpg" style="width: 256px;" />
            </a>
        </td>
        <td></td>
        <td>
            </a>
            <a href="../images/details-panel.jpg" target="_blank">
            <img src="../images/details-panel.jpg" style="width: 256px;" />
            </a>
        </td>
    </tr>
    <tr>
        <td><br>Collapsed<br>view<br><br></td>
        <td></td>
        <td><a href="/panel-guide/#1-configuration"><b>Configuration<br>Section</b></a></td>
        <td></td>
        <td><a href="/panel-guide/#21-details"><b>Details<br>Section</b></a></td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td>
            </a>
            <a href="../images/export-panel.jpg" target="_blank">
            <img src="../images/export-panel.jpg" style="width: 256px;" />
            </a><br>
        </td>
        <td></td>
        <td>
            </a>
            <a href="../images/export-options-panel.jpg" target="_blank">
            <img src="../images/export-options-panel.jpg" style="width: 256px;" />
            </a>
        </td>
        <td></td>
        <td>
            </a>
            <a href="../images/support-panel.jpg" target="_blank">
            <img src="../images/support-panel.jpg" style="width: 256px;" />
            </a>
        </td>
    </tr>
    <tr>
        <td><br><a href="/panel-guide/#31-export"><b>Export<br>Section</b></a><br><br></td>
        <td></td>
        <td><a href="/panel-guide/#33-export-options"><b>Export Options<br>Section</b></a></td>
        <td></td>
        <td><a href="/panel-guide/#51-support"><b>Export Options<br>Section</b></a></td>
    </tr>
</table>

<br>

### Sub-Panels
<table style="margin-left: 0; margin-right: auto;">
    <tr>
        <td>
            </a>
            <a href="../images/error-info-panel.jpg" target="_blank">
            <img src="../images/error-info-panel.jpg" style="width: 256px;" />
            </a><br>
        </td>
        <td></td>
        <td>
            </a>
            <a href="../images/set-up-config-panel.jpg" target="_blank">
            <img src="../images/set-up-config-panel.jpg" style="width: 256px;" />
            </a>
        </td>
    </tr>
    <tr>
        <td><br>Found in:<br><a href="/panel-guide/#1-configuration"><b>Configuration<br>Section</b></a><br><br></td>
        <td></td>
        <td><br>Found in:<br><a href="/panel-guide/#1-configuration"><b>Configuration<br>Section</b></a><br><br></td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td>
            </a>
            <a href="../images/filter-subsamples-panel.jpg" target="_blank">
            <img src="../images/filter-subsamples-panel.jpg" style="width: 256px;" />
            </a><br>
        </td>
        <td></td>
        <td>
            </a>
            <a href="../images/resolution-settings-panel.jpg" target="_blank">
            <img src="../images/resolution-settings-panel.jpg" style="width: 256px;" />
            </a>
        </td>
    </tr>
    <tr>
        <td><br>Found in:<br><a href="/panel-guide/#21-details"><b>Details<br>Section</b></a><br><br></td>
        <td></td>
        <td><br>Found in:<br><a href="/panel-guide/#33-export-options"><b>Export Options<br>Section</b></a><br><br></td>
    </tr>
</table>

<br>

- - -

<br>
<br>


## `1` - Configuration
- - -
</a>
<a href="../images/overview-2.jpg" target="_blank">
<img src="../images/overview-2.jpg" style="width: 300px;" />
</a>
</a>
<a href="../images/config-panel.jpg" target="_blank">
<img src="../images/config-panel.jpg" style="width: 300px;" />
</a>
</a>
<a href="../images/error-info-panel.jpg" target="_blank">
<img src="../images/error-info-panel.jpg" style="width: 300px;" />
</a>
</a>
<a href="../images/set-up-config-panel.jpg" target="_blank">
<img src="../images/set-up-config-panel.jpg" style="width: 300px;" />
</a>
- - -

+ ##### `2` - ERROR Section
    + `3` - Summary of all errors
    + `4` - Open `Error Information` Panel for more information on the current error state(s)
    <br>

    - - -
    + ##### `5` - Error Information Panel 
        > Lists all currently active error states. Displays suggestions on how to resolve errors.
        + `6` - Error Code
        + `7` - Summary of the error
        + `8` - Description of the error
        + `9` - Suggested actions to resolve the error
    - - -

+ ##### `10` - Configuration List Area
    + `11` - List of all configured armatures and meshes. Clicking or re-clicking an item on the list will refresh its configuration data.
    + `12` - Open a fresh instance of the `Configuration Set-Up` Panel to manually add a target mesh/armature to the configuration list for export.
    <br>

    - - -
    + ##### `13` - Configuration Set-Up Panel
        + `14` - Target selection - the object (Mesh/Armature) getting animated
        + `15` - Driver selection (optional) - if the target is driven by another object
        + `16` - Preliminary validation information - tells you if you can add the object or not
        + `17` - OK/Cancel - executes or aborts the add-operation respectively
    - - -

    + `18` - Remove currently selected configuration
    + `19` - Edit current configuration. Opens `Configuration Set-Up` Panel with fields pre-filled. Can edit currently selected configuration.
    + `20` - Scans Blender scene specifically for IMVU ANIMATION FILE templates. Automatically adds valid targets to the configuration list. Supports multiple actors appended from the IMVU toolkit.
- - -

<br>
<br>

## `21` - Details
- - -
</a>
<a href="../images/overview-3.jpg" target="_blank">
<img src="../images/overview-3.jpg" style="width: 300px;" />
</a>
</a>
<a href="../images/details-panel.jpg" target="_blank">
<img src="../images/details-panel.jpg" style="width: 300px;" />
</a>
</a>
<a href="../images/filter-subsamples-panel.jpg" target="_blank">
<img src="../images/filter-subsamples-panel.jpg" style="width: 300px;" />
</a>
- - -

+ `22` - Target object TYPE (Mesh Type, or Armature Type)
+ `23` - Target object NAME in scene
+ `24` - Open `Filter Subsamples (Bones or Shapekeys)` Panel. Depending on the target type, the panel will either display as "Filter Bones" or "Filter Shapekeys" for mesh or armature types respectively.

- - -
+ ##### `25` - Filter Subsamples (Bones or Shapekeys) Panel
    + `26` - List of all subsamples
    + `27` - Enable/disable subsample for export
    + `28` - Subsample name
    + `29` - Refresh and repopulate the subsample names, preserves enable/disable states for existing subsamples. Only enabled when subsample validation fails, requiring the user to rebuild the list.
- - -

+ `30` - Driver object NAME in scene

- - -

<br>
<br>

- - -
</a>
<a href="../images/overview-4.jpg" target="_blank">
<img src="../images/overview-4.jpg" style="width: 300px;" />
</a>
- - -


+ ## `31` - Export
Samples across a frame range, optimizes, and exports the entire sequence to XML format. See *Export* in **Terminology and Technical Details** for more information.

<br>

+ ### `32` - Quick-Export Current Pose
Samples at the current frame only, omitting temporal comparisons and reporting to specified decimal places only. See *Quick-Export Current Pose* in **Terminology and Technical Details** for more information.

<br>

- - -

<br>


+ ## `33` - Export Options
- - -
</a>
<a href="../images/overview-5.jpg" target="_blank">
<img src="../images/overview-5.jpg" style="width: 300px;" />
</a>
</a>
<a href="../images/export-options-panel.jpg" target="_blank">
<img src="../images/export-options-panel.jpg" style="width: 300px;" />
</a>
</a>
<a href="../images/resolution-settings-panel.jpg" target="_blank">
<img src="../images/resolution-settings-panel.jpg" style="width: 300px;" />
</a>
- - -

+ `34` - Filename field
+ `35` - Directory browser. Defaults to the current .blend file directory
+ `36` - Mode selection for file exporting behaviour
+ `37` - Resolution slider. Higher values incur more sample data being included in the final file, which may inflate filesize kbs. See *Resolution* in **Terminology and Technical Details** for more information.
+ `38` - Opens the `Additional Resolution Settings` popover
- - -

+ #### `39` - **Additional Resolution Settings Pop-over**
    - - -

    + ##### `40` - **Decimal Section**
        + `41` - Override the number of decimal places to report time values at. Defaults to 4 when disabled
        + `42` - Override the number of decimal places to report sample values at. Defaults to the integer portion of Resolution + 1 if disabled. 
        - - -
    + ##### `43` - **Post-Processing Style Section**
        + `44` - Optimization style 1: Rounds to a specified decimal place, and then reports in scientific notation. Works well for all cases. eg. decimals = 4, value = 0.0001234567, reported value will be "1.0e-04"
        + `45` - Optimization style 2: Rounds to a specified decimal place, and then converts to string, and removes any unnecessary 0's in the final string. More performance intensive, but slightly better filesizes than style 1. Performance cost vs Filesize efficiency is at the discretion of the user. Better suited for fine-movement animations. eg. decimals = 3, value = 0.001234567, reported value will be "1e-3"
            + `NOTE` - With neither style 1 or style 2 selected, decimals are locked and reported exactly as such. eg. decimals = 4, value = 0.0001234567, reported value will be "0.0001"
        + `46` - Smart-Round: Further augments the above optimization styles, disabled if neither are selected. Factors in number of digits and resolution to selectively round values to their "convenient" (delta-separated) neighbour. Lossy by nature. Hard-coded distribution of delta-threshold as a function of decimal places, tuned to avoid loss of fidelity as best as possible. Works well in most cases but may interfere with expectations if fine-detailed movement is the priority. The tuning may be subject to change in the future. **Deselect this if you are noticing too many jitters in your animation**. eg. decimals = 4, value = 0.000234567, reported value will be "0" instead of 0.0002. Another example: decimals = 6, value = 1.005005678 will be reported as 1.005. As decimals increase the delta-threshold ceiling for the last digit integer increases, i.e. the last-digit integer value that triggers the enforced rounding also increases.
        - - -
        + `47` - Human readability toggle. When disabled, the outputted XML file does not contain formatting whitespaces thus saving kbs in the project. For troubleshooting purposes, human readability for the final files may be required. Enable this setting if you wish to manually review your XML's. **Expect higher file sizes if enabled.**
        - - -

+ `48` - Enforce deliberately including samples at the first/last frame of an animation sequence when using the *Export* button. Works with *Temporal+* to decide whether to include sample data for ALL enabled subsamples (Temporal+ disabled), or just subsamples with detected movement only (Temporal+ enabled)
+ `49` - Temporal+ mode works to further augment the core temporal algorithm by effectively ignoring subsamples that do not animate or move from rest-pose during the sequence, whether they are enabled for sampling or not. See *Temporal+* in **Terminology and Technical Details** for more information. Not recommended for pose-pack based workflows or animations designed to "replace" instead of "average".
+ `50` - Toggle to alter BONE-ID parsing and sample parsing to ensure smooth operation for Accessory-derived armatures, which have different Bone ID and animation value calculations than most other types of IMVU projects.
- - -

## `51` - Support
- - -
</a>
<a href="../images/overview-6.jpg" target="_blank">
<img src="../images/overview-6.jpg" style="width: 300px;" />
</a>
</a>
<a href="../images/support-panel.jpg" target="_blank">
<img src="../images/support-panel.jpg" style="width: 300px;" />
</a>
- - -
+ `52` - Author: FlexFactor @ IMVU. Feel free to DM me there if need be
+ `53` - Documentation link directly to this resource
+ `54` - Tutorials link to youtube for visual assistance (work in progress)

<br>

+ `55` - Version

<br><br><br>