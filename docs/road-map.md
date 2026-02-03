# Road-Map
Future plans for the development of FlexKit.

- - -

<br>

### Disclaimer

The following road-map is by no means legally binding. I can't tell the future. Blender may change, IMVU may change, or circumstances in my life may arise. I am a solo developer and as such, my operation is sensitive to personal issues and my productivity output cannot absorb the burdens that may come with personal crisis. There is no buffer. I pledge to be honest, transparent, and ethical in all my endeavors and development on FlexKit.

- - -

<br>
<br>

## Current Version : `3.0.0`
    + Release Version!
Versions `3.0.X` reserved for emergency hotfixes if necessary

<br>
<br>

- - -

<br>



### Next Planned Versions: 

<br>

- - -

## `3.1.0` 
*Expected Q2 2026*

+ 3.1.0 will focus primarily on back-end performance, and run-time efficiency tweaks.

+ ##### **Why this hasnt been done yet**
    - Majority of performance tweaking relies on suspending UI updates and making FlexKit run in the background for exports. This can cause interference with other plug-ins that have listeners for UI updates. Back-end tweaks have to be implemented very carefully and may only provide marginal benefits. However, it is absolutely worth putting effort into ensuring a solid foundation for adding functionality to FlexKit by attempting to give it more performance headroom early on its development lifecycle.  

<br>

- - -

## `3.2.0`
*Expected Q4 2026*

+ Quality of life updates specifically aimed to better facilitate powerusers:
#### TENTATIVE
- Intelligent automatic naming of exported files, selective between active animation data-block, target object name, or user-defined name
- Tighter coupling of export options with individual configurations, i.e. making resolution settings per-configuration and not global

+ ##### **Why this hasnt been done yet**
    - The design decisions stated above are "opinionated" and lock users into a particular way of working. Constructive feedback from powerusers would make me feel more comfortable with settling on a design decision.

<br>

- - -

## `3.3.0`
*Expected Q2 2027*

##### New major feature: Batch Exports
- simultaneous sampling and export of multiple configurations of target objects
    
+ ##### Why this hasnt been done yet
    - Simultaneous sampling feature requires tight predictable performance from 3.1.0 as well as the quality of life features in 3.2.0 to be decided upon before implementation.

<br>

- - -

<br>

## Planned Features (Tentative)
1. `Queued Exports`: queue various batch-export jobs and render them all at once. This allows for varying frame range, frame rate, and other dependencies prior to executing renders
2. `XSF Exporter`: Export valid .XSF (Armature XML) files of configured armature objects
3. `Furniture Integration`: Auto-gen furniture node tree from animation template, animate furniture nodes, XSF Exporter support extended to this as well 
4. `Keyframe-only, Quick-Frame based exporting`: sequentially export each keyframe or specified frames as individual quick-exports
5. `Reverse Parse`: Load XAF/XPF data back into blender (keep your expectations low on this one)
6. `Rig Augment`: Modularly add controling bones to the IMVU AVATAR Control_Armature to improve ease of use

<br>

- - -

## GOAL: `5.0.0`
+ Final COMPLETE version of the FlexKit. A result of the implemention of the some or all of the above features and plans.
+ *Estimated 5 Year development cycle: Completion in 2031*
+ `5.0.X` reserved for hot-fixes, and limited compatibility updates up until 2032. No new features added.

+ ##### **IN THE EVENT OF FURTHER DEVELOPMENT**
    - I cannot promise to honor free updates past this point. Blender LTS versions themselves have an advertised 5 year life-cycle, and to continuously provide compatibility updates I will likely begin charging a small ($5-$10) fee for users to upgrade compatibility to whatever the current version of Blender is at the time.
    - `5.X.0` will be reserved for such updated versions

<br>

- - -

<br>
<br>

## **Final Notes**
In the hopes of solving a very real issue in IMVU, I have created a software that caters to outdated and obsolete Cal3D technology. At any given time if IMVU updates, it may render this software unnecessary or downright unusable. That is the risk I take as a developer by putting my time and effort into this and the risk you take as a purchaser.
Some planned features seem quite substantial (eg. Reverse Parse, Rig Augment, and Furniture Armature Animation). Implementation of these features may trigger price increases in the FlexKit or gatekeeping of these features entirely between a standard and an upgraded (Pro) version. Early adopters will not have to pay for price increases, and/or will automatically be given the Pro version license if such an event occurs.
<br><br><br>