# PATCH NOTES
Catch up on updates. 

    - **PLEASE NOTE** these are a snapshot at the time of version release. To get latest patch notes, ensure you are checking latest-version docs.

- - -

<br>

## `3.0.0`

+ Release version
+ Features:
    - temporal optimized animation data by default; second stage "Temporal+" for even tighter movement detection
    - complete animation sequence export or single-frame pose export
    - controllable resolution settings; post-processing to minimize filesize
    - collapsible, easy-to-read UI
    - robust Bone ID parsing for *any* armature, including accessory based armatures
    - enable/disable Subtargets (Bones/Shapekeys) for sampling/export
    - comprehensive documentation and tutorials
+ A moment of appreciation: Thank you my dear patrons, for your support and investment. Thank you for using my software. Thank you to my alpha-testers and feedback group. And thank you to my family and friends for your encouragement, and patience with my ramblings.


<br>
<br>

- - -



<br>
<br>


## **Legacy**

<br>

+ `2.0.0` - 2025
    + A more refined and functional approach to FlexKit, compared to v1.0.0. AI was utilized but the design was human-made.
    + The design was as follows: separating individual "steps" of the export algorithm to specific "modules" that can be generated and edited by AI with good iterative capability due to less contextual requirements. While this greatly improved upon the previous concepts from 1.0.0, this version was also plagued by the same difficulties as the previous version of reliability, maintenance, and expansion. Bone ID's were also still hardcoded. In some cases, the resulting animation did not behave exactly as expected in IMVU either. This was later isolated to the fact that the AI generated script was not parsing Blender data to IMVU parameters adequately, and was inconsistently reporting temporal comparisons to nonsensical decimal places (ie. comparing at 6 decimal places but reporting at 6 *significant figures*). This ultimately cemented the decision to delete everything, start from complete scratch, and revamp FlexKit entirely from the ground-up: completely human-designed, coded and tested without any AI involvement in script generation. I had to learn Blender-Python for this.

<br>

- - -

<br>

+ `1.0.0` - 2024
    + A 'fun' initial proof-of-concept of FlexKit. Exploring use of AI to analyze XML files and generate a script that could sample from Blender and create workable XML files. While functional and an interesting experiment, this version was plagued by difficulty in maintainability, expansion of features, and overall readability. Bone ID's were hardcoded and only worked for IMVU avatar armatures. It just wasnt good enough for something robust and feasible for everyday use.

<br>