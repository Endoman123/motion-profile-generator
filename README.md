# Motion Profile Generator
Generate Motion Profiles to follow with a Talon SRX.

This is a program originally based off of Vannaka's Motion Profile Generator.
 
![alt text][logo]

[logo]: https://github.com/Endoman123/motion-profile-generator/blob/master/images/motionwindow.jpg

## Motion Variables
---
- **Time Step**
	- The rate at which the control loop on the RoboRio runs
	- Units are in seconds
- **Velocity**
	- The max velocity rate your robot is capable of achieving
	- Units are in ft/s
- **Acceleration**
	- The max acceleration rate your robot is capable of achieving
	- Units are in ft/s/s
- **Jerk**
	- The rate of change of acceleration; that is, the derivative of acceleration with respect to time
	- Units are in ft/s/s/s
- **Wheel Base W**
	- The distance between your left and right wheels
	- Units are in feet
- **Wheel Base D**
	- The distance between your front and back wheels
	- Used with the Swerve modifier
	- Units are in feet
	
## Waypoints
---
- **All points are relative meaning you do not have to start at 0,0**
- **X**
	- Forward and Backwards movement of the robot
	- Inrease X to move forwards
	- Decrease X to move backwards
- **Y**
	- Left and Right movement of the robot
	- Inrease Y to move left
	- Decrease Y to move right
- **Angle**
	- This is the **ending** angle after the robot reaches the point
	- The first point should **always** have an angle of Zero
- **Editing existing points**
	- Once you have added a point to the list you can double click on it to change it. 
	- The old point will be deleted and the edited point will take that place
	- After the point is replaced it will go back to normal behavoir and add points to the end

## Load Project
---
- Motion profile projects are saved in XML format. 
You can load them to continue editing them by using the "Load" option in.
the "File" menu.
	
## Export Profile
---
 
![alt text][logo1]

[logo1]: https://github.com/Endoman123/motion-profile-generator/blob/master/images/exportprofile.jpg

1. Enter the root name for the trajectory as the file name
2. Choose the type of export you want to save the trajectories as
   - *.csv: Comma Separated Values, human readable
   - *.traj: Binary Trajectory file, not human readable

3-5 trajectories should be exported, depending on the type of drive base you use:
- Source trajectory: the center trajectory, what is created before the drive base modifiers.
- Tank Drive:
  - Left Trajectory: trajectory for the left side of the drive base.
  - Right Trajectory: trajectory for the right side of the drive base.
  
- Swerve Drive:
  - Front-Left Trajectory: trajectory for the front-left motor of the drive base.
  - Front-Right Trajectory: trajectory for the front-right motor of the drive base.
  - Back-Left Trajectory: trajectory for the back-left motor of the drive base.
  - Back-Right Trajectory: trajectory for the back-right motor of the drive base.

## Menu Bar
---

![alt text][logo2]

[logo2]: https://github.com/Endoman123/motion-profile-generator/blob/master/images/menubar.jpg

- **File Menu**
	- New: Clears all your waypoints and graphs allowing you to start over
	- Open: Opens a motion profile project (project files are *.xml)
	- Save: Saves to the working project file
	- Save As...: Saves the project to a new file
	- Export...: Exports the trajectory files to a directory
	- Exit: Exits the application
- **Help Menu**
	- Help: Opens a browser window to this github
	- About: Displays a window with information about the app. ie: The app version and the developers
		
## Acknowledgments
---

- [Jaci](https://github.com/JacisNonsense/Pathfinder) for the path generation code
- [Vannaka](https://github.com/vannaka/Motion_Profile_Generator) for the original MP generator
- [Team Mercury 1089](https://github.com/Mercury1089) for being my team