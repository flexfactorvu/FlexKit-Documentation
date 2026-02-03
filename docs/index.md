# FLEXKIT DOCUMENTATION
- - -

<br>



### Join
<iframe src="https://discord.com/widget?id=1467790361609895948&theme=dark" width="512" height="256" allowtransparency="true" frameborder="0" sandbox="allow-popups allow-popups-to-escape-sandbox allow-same-origin allow-scripts"></iframe>

<br>
<br>

- - -
### Navigation

<br>

- [**OVERVIEW**](/#overview)

<br>

- [**PATCH NOTES**](/patch-notes/)
- [**ROAD MAP**](/road-map/)

<br>

- [**INSTALLATION and use**](/#installation-and-use)
- [**CONTACT**](/#contact)

<br>

- [**QUICK START**](/quick-start/)
    - [**Static Avatar Pose**](/quick-start/#static-avatar-pose-quick-export)
    - [**Animated Avatar Pose**](/quick-start/#animated-avatar-export)
    - [**IMVU Accessories**](/quick-start/#imvu-accessories-custom-armature)
    - [**Importing into IMVU**](/quick-start/#importing-into-imvu)

- [**PANEL GUIDE**](/panel-guide/)
    - [**Configuration Section**](/panel-guide/#1-configuration)
    - [**Details Section**](/panel-guide/#21-details)
    - [**Export**](/panel-guide/#31-export)
    - [**Export Options**](/panel-guide/#33-export-options)

- [**TERMINOLOGY AND TECHNICAL DETAILS**](/terminology/)

- [**TROUBLESHOOTING**](/troubleshooting/)
    - [**Limitations and Known Bugs**](/troubleshooting/#limitations-and-known-bugs)
    - [**Common Application Errors**](/troubleshooting/#common-application-errors)
    - [**Common Animation Errors**](/troubleshooting/#common-animation-errors)
    - **FAQs**(under construction)

<br>

- [**EXTERNAL LINKS**](/external-links/)

<br>

- - -
### Installation and Use
- - -

#### Prerequisite
- Blender 4.2+ (not compatible with older versions) - [Download Blender](https://www.blender.org/download/)
- IMVU STUDIO TOOLKIT for Blender *HIGHLY* recommended - [Download IMVU Studio Toolkit](https://create.imvu.com/articles/studio/toolkit/)
    + FlexKit has a feature to automatically detect the IMVU STUDIO TOOLKIT animation tool template

#### Install
FlexKit is designed as an extension (not an add-on). Although not recommended, it's okay if you install it like an add-on instead.

1. `Edit` -> `Preferences` -> `Get Extensions`
2. `Arrow at top right` -> `Install From Disk`
3. `Locate FlexKit` (zip file | **DO NOT UNZIP**) -> `click and install` -> make sure its enabled after
<br><br>
<a href="/images/install1.jpg" target="_blank">
<img src="/images/install1.jpg" style="width: 256px;" />
</a>
<a href="/images/install2.jpg" target="_blank">
<img src="/images/install2.jpg" style="width: 256px;" />
</a>


#### Uninstall
1. `Edit` -> `Preferences` -> `Get Extensions`
2. Search `FlexKit`
3. `Arrow at top right of FlexKit sub-panel` -> `Uninstall`
<br><br>
<a href="/images/install1.jpg" target="_blank">
<img src="/images/install1.jpg" style="width: 256px;" />
</a>
<a href="/images/uninstall1.jpg" target="_blank">
<img src="/images/uninstall1.jpg" style="width: 256px;" />
</a>

#### Updating FlexKit
1. Download updated version of FlexKit
2. *Uninstall* old version
3. *Install* new version


#### Using FlexKit
- For common use-case scenarios, navigate to [**Quick-Start**](/quick-start/)
- For details on button layout and what each button does, navigate to `Extra` -> [**Panel Guide**](/panel-guide/)
- For more understanding of the terminology and what's going on under-the-hood, navigate to `Extra` -> [**Terminology and Technical Details**](/terminology/)
- Although FlexKit has a built-in troubleshooting feature, if you are still running into difficulties you can navigate to `Extra` -> [**Troubleshooting**](/troubleshooting/) or [**contact me**](/#contact)

<br>

- - -

## Overview

- - -

#### The Problem
+ Currently, in order to get animation data from Blender into IMVU creation engines, the user has to use **FBX** as the import format, usually created by exporting projects with the **IMVU STUDIO TOOLKIT** for Blender.
+ While it is convenient having your mesh, texture, skeleton, and animation assets all in one FBX file format, its common that animations imported this way don't work the way you intend them to. Either it just doesn’t detect the animation at all, the timings don't line up, or fine movements get dropped entirely. 
+ Not to mention, when you have to make changes or test things iteratively then the frequent importing of FBX feels clunky.

- - -
#### The Solution
+ FlexKit is a Blender extension designed to sample armature bones and mesh shape-keys directly from the Blender scene itself. 
    - The resulting animation data is *directly* exported into functional XML (XAF/XPF) files specifically for IMVU. 
    - FlexKit functions best *with* the IMVU STUDIO TOOLKIT for Blender, but it can function as a "stand-alone" (without the toolkit) plug-in entirely.
- - -

#### Why Its Better
- Near real-time updates of your iterations and changes in both Classic Client and IMVU Studio by exporting directly in the XAF/XPF formats into IMVU project folders
- Users choose the resolution for FlexKit's **temporal** based sampling function instead of blindly sampling everything and inflating kbs on filesizes, or relying on IMVU's hardcoded parsing.
- FlexKit has various post-processing algorithms to further improve efficiency of the resulting temporally optimized samples. Users have the ability to pick which one gives better filesizes based on their specific animation! 
- Ability to selectively sample and include only certain bones/shape-keys. Users can now export animations modularly! This is useful for selectively extracting animations that can be used on their own (e.g. a hand-wave from a dancing animation)
- Easily tackle the usual suspects of weird and wacky behaviour: subtle breathing, fine movements, exact timing, and seamless loops. Whatever skeletal or shape-key based animations you can create in Blender, is exactly what you can expect to see in IMVU. 

**Note**
- FlexKit is also under continuous development: optimizations for smoother operation, quality of life implementations to save clicks, and new features entirely. See the [**Road-Map**](/road-map/) and [**Patch Notes**](/patch-notes/) for more details.

<br>

- - -
## Contact
- - -

<br>
<table>
    <tr><td><h2>About Author</h2></td></tr>
    <tr><td><br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;I, FlexFactor, the creator of FlexKit, am a creator on IMVU since 2021; specializing in meshing, texturing, and animating.&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br>I am self-taught in all my creative skills and I mostly take online self-paced courses to increase my skillset.<br>
My favourite genres to create in are cyberpunk/cybercore, fantasy, and gothic.<br>
I aspire to make my own cinematic universe with lore one day, along with video games and shows/animations.<br><br><br></td></tr>
    <tr><td>
    </td></tr>
    <tr><td><br>
    <table>
    <tr>
    <td><br>Email<br><br></td>
    <td>&nbsp;&nbsp;&nbsp;&nbsp;flexfactorvu@gmail.com&nbsp;&nbsp;&nbsp;&nbsp;</td>
    </tr>
    <tr>
    <td><br>IMVU<br><br></td>
    <td>FlexFactor</td>
    </tr>
    <tr>
    <td><br>Discord<br><br></td>
    <td>flexfactor</td>
    </tr>
    <tr>
    <td><br>YouTube<br>&nbsp;&nbsp;&nbsp;&nbsp;Instagram&nbsp;&nbsp;&nbsp;&nbsp;<br><br></td>
    <td>FlexFactorVU
    </tr>
    </table>
    <br>
    </td></tr>
</table>


<br>
- - -
## Disclaimer
- - -
FlexKit Documentation is a resource with recommendations only. Authors are not responsible for any unexpected or erroneous results from you following this guide or by you using any hardware, software, or device.
<br><br><br>