


# SETTINGS CHANGE

Settings Changed:

Change FOV to 90, click the camera button in the top right.

Slightly increase the Gizmo Size by 2 clicks




# SCENE NOTES

Root Scene should only have player logic and lighting elements.
Child scenes should have levels, enemies, and other game objects.

A Parent Scene doesn't know anything about its child scene,
however the Child Scene knows about the Parent Scene

At runtime, only the root scene is loaded, not the children,
which is done via code.




# ASSET PIPELINE

Resources - Made outside of Stride
Models, Skeletons, Audio, Skyboxes, Fonts, Sprites, Textures, Animations,

Assets - Representations of Element inside of game during Design Time
Some Assets require Resource files.
Some Assets do not, things like Prefabs, Materials, Scenes, Colliders
Editors are used to Modify Assets

Entities - Assets within the Scene.

Components - Entities hold a list of Components, 
All Entities have at least 1 Entity, the Transform Component

Content - Assets get compiled into Content, Runtime Representation that are Loaded while the Game is Running
Game code is working with content.






# Resources

Resources should be put in the Resources folder that is created with the Stride Project, to have a centralized location when sharing.







