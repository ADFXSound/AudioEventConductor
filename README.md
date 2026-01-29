## AudioEventConductor
Thanks for your interest in the Audio Event Conductor!

The Audio Event Conductor is an Unreal Engine Plugin built in C++. Enabling a "wwise" inspired workflow Conducting Built-in UE Audio with a familiar Tree view and Inline Editor workflow. Easily manipulate Attenuations, Sound Cues, Sound Classes and Sound Concurrency Settings. 

## Installation

Get the plugin from Unreal Marketplace. Enable and restart the editor. 

<img width="531" height="104" alt="image" src="https://github.com/user-attachments/assets/71766307-a37c-417e-b65c-0dd0eb31caf2" />

## Usage

Right Click in the Content Broswer and Create an Audio Event Conductor

<img width="634" height="431" alt="image" src="https://github.com/user-attachments/assets/32e89fb9-6b85-4ea2-b444-f057dd77a1b1" />

## Auto Populate the Tree View
Inside the Audio Event Conductor, right click in the left Panel and Select either Auto Populate from Selected Folder, or Selected Sound Cues

This requires the context browser have the desired selection. For example: select the Content Folder to scan the entire project, or Sounds Folder, or specific Sound Cues.

<img width="730" height="567" alt="image" src="https://github.com/user-attachments/assets/5175504d-c559-4f62-8620-7b727e2fe241" />

## Adding To the Tree View Manually
Alternatively, you can build the treeview from scratch via Right click Add Folders/Events, or using the keyboard shortcuts Crtl+N (New Folder), or Crtl+E(New Event)

<img width="129" height="90" alt="image" src="https://github.com/user-attachments/assets/092846cc-3915-4d3a-8e54-444bec655c41" />


## Create SoundClasses
The SoundClass structure is deririved from the TreeView Folder Structure, once you have an initial treeview layout, Right Click - Create SoundClasses.
The Audio Event Conductor automatically creates the Folder Structure, Sound Classes, Wires the Sound Classes, and assigns them to the Folders in the Tree View


## Create Atteunation Profile
Right Click on an Folder and select the Create Atteunation for Selected Folder

This automatically creates an Sound Concurrency Folder and Assigns it to the Folder

NOTE: You can also manually create these in the Content Broswer

<img width="628" height="61" alt="image" src="https://github.com/user-attachments/assets/5d4c62f5-39a8-4d4a-96ab-d06604410396" />

<img width="1539" height="716" alt="image" src="https://github.com/user-attachments/assets/84f9080d-8295-4a8b-976b-709871801731" />

## Create Sound Concurrency
Right Click on an Folder and select the Create Sound Concurrency for Selected Folder

NOTE: You can also manually create these in the Content Broswer

## Create Sound Cue
Right Click on an Event and select the Create Sound Cue(s) for Selected Event

NOTE: You can also manually create these in the Content Broswer

<img width="729" height="232" alt="image" src="https://github.com/user-attachments/assets/e0813dde-865c-4f77-be67-e4b6f3d1cafc" />

## Inject Settings into the Sound Cue
Right click on events(s), and select the Inject Options 

IMPORTANT: This is a required step for the settings to be applied to the Sound Cues.

To apply the Sound Classes, Atteunation, or Sound Concurrency Settings into the Sound Cue.

<img width="733" height="112" alt="image" src="https://github.com/user-attachments/assets/ee3a5987-43c4-4dd8-8154-e19690c041e7" />

NOTE: The Audio Event Conductor Will notify when the Atteunation state of the Sound Cue is out of date with the latest changes for the Attenuation Profile

<img width="221" height="87" alt="image" src="https://github.com/user-attachments/assets/cd079270-fa70-4c13-a145-c5ef103d50b2" />

## Attenuation Profile
This is a visualized variant of the Unreal Sound Atteunation, it is recommend that you use the Debug Actor tool in a level as you learn how it works to see the curves expected behaviors.

Volume Curve the start and and end points can not be modified, the 2nd key is locked to 1.0 x axis as this is defining the Inner Radius End point

The Left Pane can click on individual curves to solo view, or Show All 

<img width="255" height="178" alt="image" src="https://github.com/user-attachments/assets/c7522582-1ec3-4138-b33e-ccf83c4e0129" />

Scale Curves with Falloff

This automatically adjusts the falloff distance in relation to the Volume Inner Radius point.

<img width="217" height="51" alt="image" src="https://github.com/user-attachments/assets/9b6ae5a8-936c-4f5e-84ef-ed230496f60f" />

Since the falloff distance only begins at the Inner Radius End point, the total Audible Distance is included for clarity

<img width="513" height="92" alt="image" src="https://github.com/user-attachments/assets/dca9e948-7584-454e-9699-5f5ec45f48ab" />

## Debug Actors

It's recommended to make a new level with your Debug Actor

Add actors Attenuation Profile Debug Actor, or Sound Atteunation Debug Actor They provide identical results.

ADFXSound workflow is to begin with the Attenuation Profile variant if you are using those.
<img width="499" height="121" alt="image" src="https://github.com/user-attachments/assets/c7382067-d144-4560-ba8e-50c06f79aba0" />

When you add it to your project it's recommended to reset it's cooridnates if not at 0,0,0
<img width="694" height="106" alt="image" src="https://github.com/user-attachments/assets/d9ca34a2-d4f6-49c5-8cba-949babf02fc2" />

The Curves update in real time as you edit.
<img width="1124" height="455" alt="image" src="https://github.com/user-attachments/assets/64fee5db-26a8-4069-9565-6c76854c5346" />

















