# URobInt

## How to make your blender to use the export

Put all your light in the categories 'env', use only point and area light. Create a node Emission with the Strength equivalent to your power to keep the information.

If you want to create door, put all your door in a collection with the name door in it. Then as the main mesh use the mesh you want to be open when using the door.
You need at least one son with this mesh, either one with 'handle' in the name if you want your handle to rotate on unreal or one with 'wrist' in his name if you want a static one. You can add a left_door, a lock and a frame, for the left_door the mesh should have 'left' or 'half' in his name , for the other two put "lock" or "frame" in the name.
for the orignis, the lock, wrist and handle should have their origin to their center, you can try and adjust to find the best feating in unreal. for the door, frame and second door, you should put them the same originis to one of the corner of the door. be sure that your door is well set to the origins of the worlds and the rotations of the world else it might end up in the wrong way.

If you have multiples mesh of a same objects and you want to import them as one to make it easier, put all your mesh in a categories inside the "furnitures" categories. Be sure that all your mesh have the same name with one without dot example: box, box.001 , box.002 , ect. In this case box will be the mesh of references to all the boxes but the scale, location and rotation of the other boxes will be conserved. The object will be export from origin so be sure they are well set in the world.

If you just want to export from origins but not a mesh, right now you can put your objects in an 'appartement' categories or modify the condition to enter to your collection, the line in the code to modify is : "elif collection.name == 'appartement'"

To create an elevator, put your mesh in the elevator folder, no need to have any kind of relationship between mesh. Your mesh can have the following one as a name:
interior, door_exterior_top_001 , door_exterior_top, door_interior_botom_001, door_interior_botom, door_interior_top_001, door_interior_top, gf_elevator, exterior_door_botom_001, exterior_door_botom. the name are pretty explicit there is two door ech time that why there is sometimes a 001.

If you want your objects to be grapable in unreal, put them in a collection named "grapable" in it that will be export the same as furnitures.