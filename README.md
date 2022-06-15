# Lab-Ex.-No---5-Design-simulate-an-environment-for-Robot-Painting-using-Robo-DK
 
## AIM:
To design a and simulate the painting environment for a serial manipluator and teach the surface for the same 

## Software  Required:
 
  Robodk 
## Theory
 

## Procedure
New project
Follow these steps to create a new RoboDK project (RDK station):
1. Download and install RoboDK from the website: https://robodk.com/download
2. Double click the shortcut on the Desktop
3. If other stations are open:
select File New Station (Ctrl+N) to start a new project
Multiple RoboDK projects can be open at the same time. Double clicking the Station icon in the tree will
activate and display that project.

Select a robot
New robots can be added from a local drive or from the online library:
1. Select File Open online library (Ctrl+Shift+O). A new nested window will appear showing the
online library
It is also possible to select the corresponding button in the toolbar.
2. Use the filters to find your robot by brand, payload, ...
In this example, we will use a UR10 robot (10 kg payload robot and 1.3 m reach).
3. Select Download. The robot should automatically appear in the station in a few seconds.
4. The online library can be closed once the robot is loaded
5. ![image](https://user-images.githubusercontent.com/36288975/173728975-43978edf-209a-43b3-bc4c-28d2d90bab18.png)
Add a Reference Frame
A Reference frame allows placing objects with respect to a robot or with respect to other objects in the 3D
space (including position and orientation).
Note: More information about reference frames in RoboDK in the reference frames section.
To add a new reference frame:
1. Select Program Add Reference Frame
Alternatively, select the equivalent button in the toolbar
2. Double click the reference frame (on the tree or on the 3D geometry on the main screen) to enter the
coordinates shown in the image (X,Y,Z position and Euler angles for the orientation). The mouse wheel
can be used on top of each case to quickly update the position of the reference frame on the main
screen.
The following colors are used by default:
o X coordinate  Red
o Y coordinate  Green
o Z coordinate  Blue
o 1st Euler rotation  Cyan
o 2nd Euler rotation  Magenta
o 3rd Euler rotation  Yellow
Tip: Select ToolsOptionsDisplayDisplay XYZ axis letters to see the Coordinate system axes.
3. Select ViewMake reference frames bigger (+) to increase the size of the reference frames
4. Select ViewMake reference frames smaller (-) to decrease the size of the reference frames
5. Select ViewShow/Hide text on screen (/) to show or hide the text on the screen
6. Optionally, rename any reference frame or object in the tree by selecting F2
![image](https://user-images.githubusercontent.com/36288975/173728997-ce0d0fa7-db74-4b07-b8fc-908a803bb478.png)
Import 3D objects
RoboDK supports most standard 3D formats such as STL, STEP (or STP) and IGES (or IGS) formats. Other
formats such as WRML, 3DS or OBJ are also supported (STEP and IGES are not supported on Mac and Linux
versions). To load a new 3D file:
1. Select File Open
2. Select the object Object Inspection available in RoboDK’s default library:
C:/RoboDK/Library/Object Inspection.
3. Alternatively, drag & drop files into RoboDK’s main window to import them automatically
4. Drag & drop the object to the reference frame Frame 2 (inside the station tree)


![image](https://user-images.githubusercontent.com/36288975/173729051-e883fc50-b5e5-49ff-9b20-5a12b61e49a4.png)
Create a TCP
New tools can be created in RoboDK from previously loaded 3D geometry:
1. Select File Open (as described in the previous section)
2. Select the Paint gun.stl file to add it as an object (it will be added at the robot base frame)
3. Drag & drop the object to the robot item inside the station tree as shown in the next image
New tools can be loaded or saved as a .tool format.
By default, RoboDK will define the TCP at the position [X,Y,Z]=[0,0,200] mm. This can be changed by entering
the coordinates manually and/or by moving the TCP holding the ALT+Shift key as shown in the next image:
1. Hold ALT+Shift or select the highlighted button from the toolbar
2. Select the light blue plane (XZ plane of the TCP) and drag the TCP approximately towards the surface
of the spray gun, as shown in the next image
![image](https://user-images.githubusercontent.com/36288975/173729087-9e7ab693-7065-43ca-971b-de7952856d97.png)
![image](https://user-images.githubusercontent.com/36288975/173729098-1b3986f5-f4eb-4de3-90de-406aef711563.png)
By default, RoboDK will define the TCP at the position [X,Y,Z]=[0,0,200] mm. This can be changed by entering
the coordinates manually and/or by moving the TCP holding the ALT+Shift key as shown in the next image:
1. Hold ALT+Shift or select the highlighted button from the toolbar
2. Select the light blue plane (XZ plane of the TCP) and drag the TCP approximately towards the surface
of the spray gun, as shown in the next imageGetting Started with RoboDK 7
3. Select the Green rounded arrow (rotation around the Y axis) to make the Z axis point outwards
4. Once an estimate of the coordinates is obtained it is possible to touch up these values manually by
double clicking the Paint gun object. The mouse wheel can be used on top of each case to quickly
update the position on the main screen.
Note: These are estimate values according to the 3D drawings. If the definition of the TCP is calibrated on the
robot it is possible to import it by pasting the coordinates in that box.
By default, RoboDK will define the TCP at the position [X,Y,Z]=[0,0,200] mm. This can be changed by entering
the coordinates manually and/or by moving the TCP holding the ALT+Shift key as shown in the next image:
1. Hold ALT+Shift or select the highlighted button from the toolbar
2. Select the light blue plane (XZ plane of the TCP) and drag the TCP approximately towards the surface
of the spray gun, as shown in the next imageGetting Started with RoboDK 7
3. Select the Green rounded arrow (rotation around the Y axis) to make the Z axis point outwards
4. Once an estimate of the coordinates is obtained it is possible to touch up these values manually by
double clicking the Paint gun object. The mouse wheel can be used on top of each case to quickly
update the position on the main screen.
Note: These are estimate values according to the 3D drawings. If the definition of the TCP is calibrated on the
robot it is possible to import it by pasting the coordinates in that box.
![image](https://user-images.githubusercontent.com/36288975/173729267-d5599e55-30ad-4a59-bfda-3575116efcc6.png)
Create Targets
Robot positions are recorded as Targets. Follow these steps to create two targets as a new home target and
approach target respectively:
1. Double click the robot to show the robot panel
2. Select Paint gun as the Tool Frame. Once a tool or a reference frame becomes active it will show a
green dot.
3. Select Frame 2 as the Reference Frame
4. Hold the Alt key and move the robot by dragging it through the TCP or the robot flange to a safe
position, free of collisions with any objects. Alternatively, move the coordinates of the Tool Frame (TCP)
with respect to the reference Frame.
5. Use the Other configurations section to switch between different robot configurations and make sure
that none of the robot axes are close to the axis limits.
Tip: In general, it is better if the first target of a program has the joint axes as centered as possible (the joint
sliders are as centered as possible, as shown in the following image). This makes sure that the robot won’t
reach the axis limits as it follows linear moves along the program. This is possible by changing the robot
configuration.
6. Select Program Teach Target (Ctrl+T), or the corresponding button in the toolbar (as shown in
the image). The target will be placed as a dependency of the active reference frame and will
automatically remember the current robot position (cartesian and joints axes).
In this example, the robot joint coordinates used for the first target are: [-150, -75, -90, -60, 70, 110]
deg. These values can be copied from this text and pasted in the Joint axis jog of the robot panel
using the corresponding button.

![image](https://user-images.githubusercontent.com/36288975/173729300-681d96a6-c064-4e23-a7af-c0230765725c.png)
7. Rename the first target as Home by pressing F2. Alternatively, select ToolsRename item.
8. Move the robot closer to one edge of the part (by dragging the tool using the Alt key, entering
coordinates or jogging the axis manually)
In this example we used the following robot joint coordinates [0,0,200,180,0,180] deg.
9. Select Program Teach Target (Ctrl+T) or the appropriate button in the toolbar to create a new
target
10. Rename the target to Approach as shown in step 7
11. 11. Select the Home target and the Approach target alternatively to see the robot moving between the two
targets
12. Right click the target and select Teach Current Position (Alt+double click) if a different position needs
to be recorded for one of the targets
13. Right click the target and select Target Options… (F3) to open the target options window shown
in the next image
Add an Approach Program
Follow these steps to create a program that moves from the Home target to the Approach target:
1. Select Program Add Program from the menu or the corresponding button in the toolbar (as
shown in the next image)
2. Rename the program to ApproachMove
3. Select the Home target
4. Select Program Move Joint Instruction (or the corresponding button in the toolbar)
Two instructions will be added automatically to tell the robot what tool frame and reference frames we
are using
Note: If no target is selected, a new target will be created at the same location of the robot.
5. Select the Approach target
6. Select Program Move Joint Instruction again
Double click the ApproachMove program and it will execute the program simulation. The simulation bar and
an estimated cycle time will be displayed.   
![image](https://user-images.githubusercontent.com/36288975/173729348-a700964f-505d-4935-b4d9-a5e95aa32d7a.png)

Create Targets on Surface
The Create Targets on Surface feature, is useful for applications such as painting or inspection:
1. Select Program Teach Target(s) on Surface (Ctrl+Shift+T)
2. Move the mouse cursor over the part to see a preview of what the robot looks like when it reaches the
part
3. Select a few points on the object (left click). Each mouse left click will define a new target keeping the Z
axis of the TCP normal to the surface (perpendicular to the surface).
4. If necessary, adjust the orientation around the Z axis by moving the wheel on the left panel or pressing
the left/right keys.
5. Hold Alt to move an existing target
6. Hold Alt+Shift to move an existing target while keeping it on the surface
7. Select Esc key or right click on the screen and select Done to exit the Create Targets on Surface mode
8. ![image](https://user-images.githubusercontent.com/36288975/173729366-e0d49a75-454d-4366-b7f5-1e02de369d1d.png)

1. Select all the targets created on the surface and right click
Tip: Hold the Ctrl key to select multiple targets. Alternatively, select the Target 3, hold shift, then select Target
10 to select all targets between Target 3 and Target 10.
2. Select Rename group from the pop up menu
3. Enter Top Paint. All selected targets will be renamed and numbered.
4. Right click on the targets again and select Create Program. A new program will be generated. The first
movement will be a joint move and following movements will be linear.
5. Select F2 to rename the program to PaintTop
6. Double click the PaintTop program to see the simulation moving along the targets
7. If required, reorder the movements by dragging the move instructions inside the program


![image](https://user-images.githubusercontent.com/36288975/173729404-a7b7ffef-3366-434b-9cc4-8246e93fec28.png)
Add a Retract Program
Similar to the previous operations:
1. With the robot placed at the last target, move the robot upwards by increasing the Z coordinate of the
TCP with respect to the reference frame in the robot panel (highlighted case in the next image)
2. Select Program Add Program, or the appropriate button in the toolbar.
3. Select Program Move Linear Instruction, or the appropriate button in the toolbar . Rename it
to Retract by pressing F2 key.
4. Select the Home target
5. Select Program Move Joint Instruction. A new move instruction will be added, linked to the
Home target

![image](https://user-images.githubusercontent.com/36288975/173729436-d4d9e8b7-7504-4b24-beda-dd213813557d.png)



##Program:
/*
 
Developed by: 
RegisterNumber:  
*/
 

 
## Results of simulation :
 
