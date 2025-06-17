# Importing project as a dependency

NOTE: IT'S EASIER TO JUST USE THE METHOD DEFINED IN GRADLE NOTES AND THEN JUST REIMPORT THE GRADLE PROJECT.

Examaple (group) project: C:\development\opengi\git\opengi-commons
This contains subprojects such as: opengi-commons-services

Import the group commons project (the group/parent) via the gradle panel on the right. (Click the '+' symbol in the gradle panel.)
In the gradle panel, right click on the main (CLPPP) project -> Composite build configuration -> Check the group project.

Reload all gradle projects in the right hand panel (top left button)

Code references should follow through to the project.

## Removing the project
Click the "composite build configuration" at the top of the panel.
Uncheck the relevant project.

Right click on the imported project
Select "Unlink gradle project"


## Troubleshooting
Reset configuration for gradle by:
 Delete the module from the gradle panel.
 deleting: ..\.idea\gradle.xml

It should remove the modules on the right automatically.
Reload the gradle project via the popup in the bottom right.

Also:
Try refreshging project dependencies on right hand pane - right click on project



-------
