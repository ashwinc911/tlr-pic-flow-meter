# Build and Develop #

In order to develop, build, and deploy the code for the TLR Flow meter, you will need to correct hardware and software.  The hardware that was utilized for this project was the PIC24/PIC32 PIM Companion Board and was purchased from http://www.eflightworks.net/. Eric was the person that I dealt with at eflightworks and was a FANTASTIC resource for supporting his boards.  I purchased a custom configuration for the TLR flow meter and he was always responsive in my **many** support questions as I developed this board. The boards that were purchased were Rev C.

The first thing to note is that the development for this project must be done under windows as that is the only platform that runs the MPLAB IDE that I used to program the PIC board.  So, the first thing to do is install the MPLAB IDE (version 8.10).  Once the IDE is installed, you then need to check out the source code from Google code.  Browse the **Source** tab on the Google code home page to see how to check out the code.

TODO kgomes - Document hardware setup (power ICD 2 externally).

TODO kgomes - Document how to run Project->Project Wizard... to create a new project and include the files that were checked out (select correct device). Add correct .gld file. Right click on project and select Build Options. Click on Directories tab. Select Intermediary Directory and then New, type in .\tmp and click outside to set. Select Include Search Path, then New, then type in .\include and click outside to set. Select Library Search Path, then New, then type in .\lib and click outside to set. Click OK, and click on Project->Save

Then choose Debugger->Select Tool->MPLAB ICD 2.  Follow the wizard (if prompted) and choose to power the ICD 2 externally and manually connect. Click on Debugger->Connect and you might have to install operating system to ICD 2. Then run Project->Clean.  Then run Project->Build All.  Hopefully you will see the "Build Succeeded".