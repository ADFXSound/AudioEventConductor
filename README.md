## AudioEventConductor
Thanks for your interest in the Audio Event Conductor!

The Audio Event Conductor is an Unreal Engine plugin built in C++, enabling a Wwise-inspired workflow for conducting built-in UE audio with a familiar tree view and inline editor workflow. Easily manipulate Attenuations, Sound Cues, Sound Classes, and Sound Concurrency Settings.

<img width="3439" height="1354" alt="image" src="https://github.com/user-attachments/assets/10806e8e-0cca-4bbe-ba1f-0342ca09ee08" />

## Installation

Get the plugin from Unreal Marketplace. Ensure it is Enabled. If not, enable and restart the editor. 

<img width="531" height="104" alt="image" src="https://github.com/user-attachments/assets/71766307-a37c-417e-b65c-0dd0eb31caf2" />

## Right Click Menu
Accessible from the left panel of the Audio Event Conductor. Right-click to see options.

<img width="294" height="737" alt="image" src="https://github.com/user-attachments/assets/2e3876d9-cc34-4021-8b61-bef840ced2fd" />

<img width="3439" height="1354" alt="image" src="https://github.com/user-attachments/assets/74af7624-fa54-44fe-826d-c1e062095a30" />

## TreeView
A  list of Folders and Events that define values for Sound Classes, Atteunation Profiles, and Concurrency Settings and apply them hierachrically.

## Event / Folder Editor
For each Folder and Event, the following properties are definable and cascade inheritance downward in the tree view.
<img width="502" height="368" alt="image" src="https://github.com/user-attachments/assets/38426e0c-62e2-45e4-a565-4926ebd92ce4" />

## Inline Editor
This section is 

## Usage

Right-click in the Content Broswer and Create an Audio Event Conductor

<img width="634" height="431" alt="image" src="https://github.com/user-attachments/assets/32e89fb9-6b85-4ea2-b444-f057dd77a1b1" />

## Auto Populate the Tree View
Inside the Audio Event Conductor, right-click in the left panel and select either "Auto Populate from Selected Folder" or "Selected Sound Cues."
This requires the Content Browser to have the desired selection. For example: select the Content folder to scan the entire project, or the Sounds folder, or specific Sound Cues.

<img width="730" height="567" alt="image" src="https://github.com/user-attachments/assets/5175504d-c559-4f62-8620-7b727e2fe241" />

## Adding To the Tree View Manually
Alternatively, you can build the tree view from scratch via right-click → Add Folders/Events, or using the keyboard shortcuts Ctrl+N (New Folder) or Ctrl+E (New Event).

<img width="129" height="90" alt="image" src="https://github.com/user-attachments/assets/092846cc-3915-4d3a-8e54-444bec655c41" />


## Create SoundClasses
The Sound Class structure is derived from the Tree View folder structure. Once you have an initial tree view layout, right-click → Create Sound Classes.
The Audio Event Conductor automatically creates the folder structure, Sound Classes, wires the Sound Classes together, and assigns them to the folders in the Tree View.


## Create Atteunation Profile
Right-click on a folder and select "Create Attenuation for Selected Folder."
This automatically creates a Sound Attenuation asset and assigns it to the folder.

NOTE: You can also manually create these in the Content Broswer

<img width="628" height="61" alt="image" src="https://github.com/user-attachments/assets/5d4c62f5-39a8-4d4a-96ab-d06604410396" />

<img width="1539" height="716" alt="image" src="https://github.com/user-attachments/assets/84f9080d-8295-4a8b-976b-709871801731" />

## Create Sound Concurrency
Right-click on a folder and select "Create Sound Concurrency for Selected Folder."
NOTE: You can also manually create these in the Content Browser.

## Create Sound Cue
Right-click on an Event and select "Create Sound Cue(s) for Selected Event."
NOTE: You can also manually create these in the Content Browser.

<img width="729" height="232" alt="image" src="https://github.com/user-attachments/assets/e0813dde-865c-4f77-be67-e4b6f3d1cafc" />

## Inject Settings into the Sound Cue
Right-click on event(s) and select the Inject options.
IMPORTANT: This is a required step for the settings to be applied to the Sound Cues.
Use this to apply Sound Classes, Attenuation, or Sound Concurrency Settings into the Sound Cue.

<img width="733" height="112" alt="image" src="https://github.com/user-attachments/assets/ee3a5987-43c4-4dd8-8154-e19690c041e7" />

NOTE: The Audio Event Conductor Will notify when the Atteunation state of the Sound Cue is out of date with the latest changes for the Attenuation Profile

<img width="221" height="87" alt="image" src="https://github.com/user-attachments/assets/cd079270-fa70-4c13-a145-c5ef103d50b2" />

## Attenuation Profile
This is a visualized variant of the Unreal Sound Attenuation. It is recommended that you use the Debug Actor tool in a level as you learn how it works to see the curves' expected behaviors.
Volume Curve: The start and end points cannot be modified. The 2nd key is locked to 1.0 on the X axis, as this defines the Inner Radius end point.
The left pane allows you to click on individual curves to solo view, or Show All.

<img width="255" height="178" alt="image" src="https://github.com/user-attachments/assets/c7522582-1ec3-4138-b33e-ccf83c4e0129" />

Scale Curves with Falloff

This automatically adjusts the falloff distance in relation to the Volume Inner Radius point.

<img width="217" height="51" alt="image" src="https://github.com/user-attachments/assets/9b6ae5a8-936c-4f5e-84ef-ed230496f60f" />

Since the falloff distance only begins at the Inner Radius end point, the total Audible Distance is included for clarity.

<img width="513" height="92" alt="image" src="https://github.com/user-attachments/assets/dca9e948-7584-454e-9699-5f5ec45f48ab" />

## Debug Actors
It's recommended to create a new level with your Debug Actor. 

NOTE: This is an actor, not an actor component. 

NOTE: The intention is to use one variant at a time, to analyize the curves in depth, but not attached to anything. 
Due to the amount of debug detail provided, it's not realistic for it to useful in multiple instances. 

Speak up in the Discord if you have feedback or would want a streamlined Actor Component variant. 
Add actors: Attenuation Profile Debug Actor or Sound Attenuation Debug Actor. They provide identical results.
The ADFXSound workflow is to begin with the Attenuation Profile variant if you are using those.

<img width="499" height="121" alt="image" src="https://github.com/user-attachments/assets/c7382067-d144-4560-ba8e-50c06f79aba0" />

When you add it to your project it's recommended to reset it's cooridnates if not at 0,0,0
<img width="694" height="106" alt="image" src="https://github.com/user-attachments/assets/d9ca34a2-d4f6-49c5-8cba-949babf02fc2" />

The Curves update in real time as you edit.
<img width="1124" height="455" alt="image" src="https://github.com/user-attachments/assets/64fee5db-26a8-4069-9565-6c76854c5346" />

The Roll off curve will change from Green to red, if using a custom curve 
<img width="937" height="290" alt="image" src="https://github.com/user-attachments/assets/1e1a86d9-36a4-4780-9869-8db389a9b111" />
<img width="1150" height="458" alt="image" src="https://github.com/user-attachments/assets/637ca176-623b-462e-9d8b-6e168b840231" />

## Debug Actors (Crossover Preset)

<img width="680" height="105" alt="image" src="https://github.com/user-attachments/assets/d528bf75-1f02-4c33-b97a-6bc242db7d3c" />

When in use, you will see the crossover visualization.
<img width="785" height="280" alt="image" src="https://github.com/user-attachments/assets/79d7ae99-84d1-4d44-bad8-249ea467470a" />


## Debug Actors (Filterizer Preset)

<img width="662" height="141" alt="image" src="https://github.com/user-attachments/assets/0ac41970-d949-4ddb-8b68-70f5574912f8" />

When in use, you will see the Filterizer frequency visualization.

<img width="1869" height="315" alt="image" src="https://github.com/user-attachments/assets/a13e0556-73ed-4bb4-8233-06beb40fd1e7" />

## Debug Actors (Test Audio)

You can add a sound to test with that can either play on/off with time intervals, or loop with Start/Stop (for gunshots, etc.).
<img width="673" height="497" alt="image" src="https://github.com/user-attachments/assets/a995e532-a51a-42c5-a1a0-a21a742012fd" />

IMPORTANT: Ensure "Apply Attenuation Profile to Sound" is checked so you can properly audition the settings. Otherwise, it will use whichever Sound Attenuation is active in the Sound Cue.
<img width="332" height="22" alt="image" src="https://github.com/user-attachments/assets/7131de30-6215-4a07-8cec-ea2933148431" />

## RandomizerADFX
The RandomizerADFX sound node streamlines common Sound Cue workflows related to individual sound wave players linked into a Random node, then linked into a modulator. It also auto-populates the sound waves to reduce redundant navigating and dragging from the Content Browser. It will also function with just one sound.

<img width="737" height="606" alt="image" src="https://github.com/user-attachments/assets/afcc96f2-4b8d-4735-9a38-8f2240ac095a" />


The option also exists to add silence.

<img width="624" height="249" alt="image" src="https://github.com/user-attachments/assets/1daaa3ab-2858-485d-8d6b-9c21f9c1dd0a" />

The Volume Modulation and The Pitch Modulation are activated by defauled and indicated as on in the Node with [VP], respectively.

<img width="180" height="60" alt="Randomizer2" src="https://github.com/user-attachments/assets/53298f54-9550-4016-ba69-5e6870112bf5" />


<img width="568" height="194" alt="image" src="https://github.com/user-attachments/assets/28d6141d-1c19-4589-a71d-3383c3d4fc6c" />

## LooperADFX

The LooperADFX is a variant of many of the features from RandomizerADFX, but it's built specifically for looping audio. It will also function with just one sound, but the additional looping features become obsolete.

<img width="157" height="60" alt="Looper2" src="https://github.com/user-attachments/assets/61acdcc2-f735-4e2c-a6dd-3832ac719940" />

Additions include Sequenital and Random selection

<img width="561" height="81" alt="image" src="https://github.com/user-attachments/assets/c01ba038-ad94-4f59-bbb1-0360407a8e31" />



## CrossfaderADFX
The CrossfaderADFX is a simple crossfader that enables you to easily create blend distances. It defaults to 2 inputs, but users can add additional crossover points.

<img width="236" height="90" alt="Crossfader2" src="https://github.com/user-attachments/assets/11b409a7-f2d3-48d3-b920-eac6cc76aaa7" />

<img width="767" height="322" alt="image" src="https://github.com/user-attachments/assets/88b0d988-7113-47b8-be4b-14552e58cbef" />

RECOMMENDED: Use the Preset categorically in many Sound Cues, so you can edit the preset and change the blend values for any Sound Cue that has the same Preset allocated.

## FilterizerADFX
The FilterizerADFX enables Low Pass and High Pass filters based on attenuation start distance and draws to the end of the defined distance.
<img width="136" height="60" alt="Filterizer2" src="https://github.com/user-attachments/assets/2a0b6546-851b-422a-b22a-cc77620a4c39" />

<img width="424" height="324" alt="image" src="https://github.com/user-attachments/assets/2cc27a52-2481-42f0-ad85-2ea3ef937d72" />

RECOMMENDED: Use the Preset categorically in many Sound Cues, so you can edit the preset and change the values for any Sound Cue that has the same Preset allocated.

## Debug Commands
a.Debug.CrossfaderADFX - CrossfaderADFX verbose logging

a.Debug.RandomizerADFX - RandomizerADFX verbose logging

a.Debug.LooperADFX - LooperADFX verbose logging

## Performance
While The Audio Event Conductor is optimized, should you encounter severe performance issues, there are a few built in features to help focus its attention to less tasks simulatenously.

## Live Update

When disabled you will need to press the Update button manually to obtain the same expected results.
When enabled (checkbox next to the "Update" button), the editor automatically refreshes the UI in real-time as you make changes:
Tree view updates immediately when you add, rename, or reorganize items
Details panel updates instantly when you select items
Inline SoundCue panel loads and displays embedded editors immediately

<img width="201" height="34" alt="image" src="https://github.com/user-attachments/assets/fb3b44f2-5f42-421b-a0d6-2bb6c5c41fbf" />

## Auto Sort Tree
Automatically keeps the hierarchy tree alphabetically sorted at all times:
When you rename items, they move to their correct alphabetical position
When you add new folders/events, they're inserted in sorted order
Sorting happens recursively through all nested folders

<img width="288" height="35" alt="image" src="https://github.com/user-attachments/assets/478d2a4c-8d47-491d-8133-84c87956abe0" />
















