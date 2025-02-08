


# SETTINGS CHANGE

Settings Changed:

Change FOV to 90, click the camera button in the top right.

Slightly increase the Gizmo Size by 2 clicks

Game Settings - Texture quality to Fast, but change it to best for deployment.




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






# RESOURCES

Resources should be put in the Resources folder that is created with the Stride Project, to have a centralized location when sharing.




# TEXTURES

Generate Mipmaps - Allows for better performance when rendering textures at a smaller size than the original when seen at a distance. Uses more memory.
DO NOT USE IT FOR UI

Compress - Compresses the texture to save memory, but can cause artifacts.

Stream - Dynamic texture loading, don't use for things that are always seen, like the player character.
No loading splash screens.
Stream textures only load textures when needed.

Normal Map - basically its' a texture that has divots or cracks, which can reflect engine light, causing it to have depth but not affect the model itself.

Global Texture quality Settings - in the Game Settings




# MODELS

Groups - You can set groups to be rendered by a camera. One camera might not see a group, the other might see it, useful for certain types of games or fog of war, invis, etc.

How to flow of the Model Pipeline Works:

Texture - This is the base image to be applied to the model.
Material - This is the container for the texture, and other properties like shininess, transparency, etc.
Model - Apply the Material to the Model.
Model is technically a component on the Entity, so in a strange way the Model asset is preloaded with the Model component, which in itself has the Material component.



# COLLIDERS

Static - Doesn't move colliders, like walls, floors, not affected by gravity, etc.
Can be moved by code if need be.

Rigid Bodies - Crates, balls, barrels, effected by other things like gravity or explosions.

Character Collider - Attach to Playable Character.

Custome Model Collider - Get your Model, Add Asset - Convex Hull - Select your model
If you want a more detailed collider, then go to that collider shape asset, then go to Decomposition and select it,
then fiddle with settings until you get to what you like.
Selecting decomposition will auto create the collider upon it to be more detailed and you can see that.



