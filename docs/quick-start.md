- - -
# **IMPORTANT**
**FlexKit will only be fully functional within saved Blender files. Please ensure your Blender project is SAVED before any use!**
- - -
<br>
<br>

## Useful Links
* [**Install/Uninstall/Update**](index.md#installation-and-use)
+ [**Panel Guide**](panel-guide.md)
+ [**Terminology and Technical Details**](terminology.md)
+ [**Patch Notes**](patch-notes.md)
+ [Troubleshooting](troubleshooting.md)
+ [Extra Resources](external-links.md)
+ [Site Navigation](index.md#navigation)


<br>
<br>

- - -
## Static Avatar Pose (Quick Export)
- - -

<table style="margin-left: 0; margin-right: auto;">
    <tr>
        <td>
            <a href="../images/auto-detect.jpg" target="_blank">
            <img src="../images/auto-detect.jpg" style="width: 128px;" />
            </a>
        </td>
        <td></td>
        <td>
            <a href="../images/quickexportanim.jpg" target="_blank">
            <img src="../images/quickexportanim.jpg" style="width: 128px;" />
            </a>
        </td>
        <td></td>
        <td>
            <a href="../images/quickexportmorph.jpg" target="_blank">
            <img src="../images/quickexportmorph.jpg" style="width: 128px;" />
            </a>
        </td>
    </tr>
    <tr>
        <td><br>Configure for export<br>See Step 2<br><br></td>
        <td></td>
        <td>Export animation<br><b>(armature)</b><br>See Step 3</td>
        <td></td>
        <td>Export animation<br><b>(morph)</b><br>See Step 3</td>
    </tr>
</table>

#### Prerequisite
+ `IMVU STUDIO TOOLKIT` -> `Animation Tool` -> `APPEND ANIMATION FILE`
+ **SAVED** Blender Project


#### Instructions

1. Create your avatar pose in `Pose-Mode` as you would normally.

2. `FlexKit` -> `Configuration` -> `Click "Auto-Detect IMVU Template"`

3. **EXPORTING**
    + TO EXPORT ARMATURE POSE:
        - `FlexKit` -> `Configuration` -> `Click "Anim" in the list`
        - `FlexKit` -> `"Quick-Export Current Pose"`
    + TO EXPORT FACIAL MORPHS:
        - `FlexKit` -> `Configuration` -> `Click "Morph" in the list`
        - `FlexKit` -> `"Quick-Export Current Pose"`
        <br>

4. Search in the current .blend project folder for the associated Animfxxx.xaf/Morphfxxx.xpf file(s)
    - The xxx denotes a number corresponding to your current frame in Blender, likely 001. so look for Animf001.xaf and Morphf001.xpf respectively.

<br>

#### Common Errors and Warnings
+ Error: **CFEx00**: `Missing Configuration`
+ Error: **SVEx00**: `File Not Saved`
+ Warning: `NO IMVU TEMPLATE CONFIGURATIONS FOUND`
+ Warning: `File Failed Export`
+ [**Troubleshoot**](troubleshooting.md#common-application-errors) for possible resolutions.

<br>
<br>

- - -
## Animated Avatar (Export)
- - -

<table style="margin-left: 0; margin-right: auto;">
    <tr>
        <td>
            <a href="../images/framesettings.jpg" target="_blank">
            <img src="../images/framesettings.jpg" style="width: 128px;" />
            </a>
        </td>
        <td></td>
        <td>
            <a href="../images/auto-detect.jpg" target="_blank">
            <img src="../images/auto-detect.jpg" style="width: 128px;" />
            </a>
        </td>
        <td></td>
        <td>
            <a href="../images/exportanim.jpg" target="_blank">
            <img src="../images/exportanim.jpg" style="width: 128px;" />
            </a>
        </td>
        <td></td>
        <td>
            <a href="../images/exportmorph.jpg" target="_blank">
            <img src="../images/exportmorph.jpg" style="width: 128px;" />
            </a>
        </td>
    </tr>
    <tr>
        <td><br>Check time setting<br>(FPS, frame range)<br>See Prerequisite<br><br></td>
        <td></td>
        <td><br>Configure for export<br>See Step 2<br><br></td>
        <td></td>
        <td>Export animation<br><b>(armature)</b><br>See Step 3</td>
        <td></td>
        <td>Export animation<br><b>(morph)</b><br>See Step 3</td>
    </tr>
</table>

#### Prerequisite
+ `IMVU STUDIO TOOLKIT` -> `Animation Tool` -> `APPEND ANIMATION FILE`
+ **SAVED** Blender Project

+ **FOR BEST RESULTS**:
    - Double check FPS is set to 30 in `Blender Properties Panel -> Output -> Frame Rate`
    - Ensure `Frame Range` starts and ends exactly where you want the animation to start and end
    <br>


#### Instructions

1. Create your avatar animation in `Pose-Mode` as you would normally. 
2. `FlexKit` -> `Configuration` -> `Click "Auto-Detect IMVU Template"`

3. **EXPORTING**
    + TO EXPORT ARMATURE ANIMATION SEQUENCE:
        - `FlexKit` -> `Configuration` -> `Click "Anim" in the list`
        - `FlexKit` -> `"Export"`
    + TO EXPORT FACIAL MORPH ANIMATION SEQUENCE:
        - `FlexKit` -> `Configuration` -> `Click "Morph" in the list`
        - `FlexKit` -> `"Export"`

4. Search in the current .blend project folder for the associated Anim.xaf/Morph.xpf file(s)

<br>

#### Common Errors and Warnings
+ Error: **CFEx00**: `Missing Configuration`
+ Error: **SVEx00**: `File Not Saved`
+ Warning: `NO IMVU TEMPLATE CONFIGURATIONS FOUND`
+ Warning: `File Failed Export`
+ [**Troubleshoot**](troubleshooting.md#common-application-errors) for possible resolutions.

<br>
<br>

- - -
## IMVU Accessories (Custom Armature)
- - -

<table style="margin-left: 0; margin-right: auto;">
    <tr>
        <td>
            <a href="../images/add-config.jpg" target="_blank">
            <img src="../images/add-config.jpg" style="width: 128px;" />
            </a>
        </td>
        <td></td>
        <td>
            <a href="../images/add-config2.jpg" target="_blank">
            <img src="../images/add-config2.jpg" style="width: 256px;" />
            </a>
        </td>
        <td></td>
        <td>
            <a href="../images/enableaccessory.jpg" target="_blank">
            <img src="../images/enableaccessory.jpg" style="width: 128px;" />
            </a>
        </td>
        <td></td>
        <td>
            <a href="../images/accessory-export1.jpg" target="_blank">
            <img src="../images/accessory-export1.jpg" style="width: 128px;" />
            </a>
        </td>
    </tr>
    <tr>
        <td><br>Add new target<br>See Step 2<br><br></td>
        <td></td>
        <td>Select target<br>See Step 3</td>
        <td></td>
        <td>Enable<br><b>Accessory Export</b><br>See Step 4</td>
        <td></td>
        <td>Export<br>Full/Quick<br>See Step 4</td>
    </tr>
</table>

#### Prerequisite
+ `IMVU STUDIO TOOLKIT` -> `Attachment Tool` -> `APPEND ATTACHMENT FILE` (optional)

+ **It is highly recommended to have your custom-made armature adhere to the following guidelines**:
    - One single root bone (no parents)
    - Root bone is named AttachmentRoot (the IMVU STUDIO TOOLKIT names this automatically)
    - It is recommended to build your skeleton from the IMVU STUDIO TOOLKIT templated armature

+ **SAVED** Blender Project

+ **FOR BEST RESULTS in ANIMATIONS (non-static poses)**:
    - Double check FPS is set to 30 in: `Blender Properties Panel` -> `Output` -> `Frame Rate`
    - Ensure `Frame Range` starts and ends exactly where you want the animation to start and end
    - (same as [**animated avatar**](#animated-avatar-export) prerequisite)

<br>

#### Instructions

1. Create your accessory animation/pose in `Pose-Mode` as you would normally. 
2. `FlexKit` -> `Configuration` -> `Click "+"`
3. `Select Target Object` -> Find your accessory ARMATURE (commonly named "Attachment.RIG" if built from IMVU STUDIO TOOLKIT template) -> Click `OK`
    * **IF YOUR ACCESSORY MESH HAS ANIMATED SHAPE-KEYS**:
        - `FlexKit` -> `Configuration` -> `Click "+"`
        - `Select Target Object` -> Find your accessory MESH -> Click `OK`
4. **EXPORTING**
    + `Export Options` -> `Accessory Export` -> **ENABLE**
    + TO EXPORT ARMATURE ANIMATION SEQUENCE:
        - `FlexKit` -> `Configuration` -> `Click ARMATURE object name in the list`
    + TO EXPORT SHAPE-KEY ANIMATION SEQUENCE:
        - `FlexKit` -> `Configuration` -> `Click MESH object name in the list`
    + `FlexKit` -> `"Export"` or `"Quick-Export Current Pose" (for single pose)`
5. Search in the current project folder for the associated XAF/XPF file(s)

<br>

#### Common Errors and Warnings
+ Error: **CFEx00**: `Missing Configuration`
+ Error: **SVEx00**: `File Not Saved`
+ Warning: `Mesh has no shapekeys`
+ Warning: `File Failed Export`
+ [**Troubleshoot**](troubleshooting.md#common-application-errors) for possible resolutions.

<br>
<br>

- - -
## Importing Into IMVU
- - -

### Prerequisite
- Import Mesh and/or Armature. Recommended to use FBX exported from IMVU STUDIO TOOLKIT for Blender. However uncheck or disregard any animations bundled with the package.
- For avatar-derived items or animation-only items (pose packs), you will not need FBX at all.

<br>

### Instructions

* ##### IMVU Studio

    <table style="margin-left: 0; margin-right: auto;">
        <tr>
            <td>
                <a href="../images/imvu-import.jpg" target="_blank">
                <img src="../images/imvu-import.jpg" style="width: 128px;" />
                </a>
            </td>
            <td></td>
            <td>
                <a href="../images/imvu-update.jpg" target="_blank">
                <img src="../images/imvu-update.jpg" style="width: 128px;" />
                </a>
            </td>
        </tr>
        <tr>
            <td><br>Importing xaf/xpf<br>See Step 1<br><br></td>
            <td></td>
            <td>Updating xaf/xpf<br>See Step 2</td>
        </tr>
    </table>

    1. In your project: `Import Icon` -> `Import Asset` -> Search for the XAF/XPF -> `Open`
    2. To reload/update the asset, either import it again or:
        - `Assets` -> Find Asset -> `Options` -> `Update Asset`.

* ##### Classic

    <table style="margin-left: 0; margin-right: auto;">
        <tr>
            <td>
                <a href="../images/showprojectclassic.jpg" target="_blank">
                <img src="../images/showprojectclassic.jpg" style="width: 256px;" />
                </a><br>
                <a href="../images/copyfileover.jpg" target="_blank">
                <img src="../images/copyfileover.jpg" style="width: 256px;" />
                </a>
            </td>
            <td></td>
            <td>
                <a href="../images/changedirectory.jpg" target="_blank">
                <img src="../images/changedirectory.jpg" style="width: 128px;" />
                </a>
            </td>
            <td></td>
            <td>
                <a href="../images/copyaddress.jpg" target="_blank">
                <img src="../images/copyaddress.jpg" style="width: 256px;" />
                </a>
            </td>
        </tr>
        <tr>
            <td><br>Step 1 (top)<br>Step 2 (bottom)<br><br></td>
            <td></td>
            <td>Change export<br>folder<br>See Step 3</td>
            <td></td>
            <td>Copy folder address<br>See Step 3</td>
        </tr>
    </table>

    1. Open the project folder
    2. Copy your XAF/XPF files into the project folder
    3. For seamless integration, copy the project folder path, and change the FlexKit output directory in `Export Options` to the project folder. This way, everytime you export your file, it will automatically update in IMVU (after clicking `Apply Changes`)

<br>
<br>

- - -

<br><br><br>