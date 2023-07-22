
# Use OBS in MS Teams as Virtual Camera

### <u>A. PREREQUISITE:</u>

A1. Install the [Microsoft Teams Desktop App](https://www.microsoft.com/en-us/microsoft-365/microsoft-teams/download-app)  
A2. Install OBS from the [official page](https://obsproject.com/download)  
A3. Install the latest [Mac Virtual Camera plugin for OBS](https://github.com/johnboiles/obs-mac-virtualcam/releases/) by [John Boiles](https://github.com/johnboiles)

<br>

### <u>B. MODIFY THE LATEST VERSION OF TEAMS</u>
(Required to allow virtual camera inputs - disabled by Microsoft in a recent version)

B1. Quit MS Teams  
B2. Open Terminal (Applications/Utilities/Terminal.app) and run the following commands:  
B3. If you haven't installed Xcode previously, first run:  
~~~
xcode-select --install
~~~
B4. then, run the following command (will require your user password):   
~~~
sudo codesign --remove-signature "/Applications/Microsoft Teams.app"
~~~

B5. and followed by:
~~~
sudo codesign --remove-signature "/Applications/Microsoft Teams.app/Contents/Frameworks/Microsoft Teams Helper.app"
~~~

<br>

### <u>C. USE OBS AS VIRTUAL CAMERA</u>
C1. Start OBS and from the menu select `Tools > Start Virtual Camera`  
C2. Start a Microsoft Teams video call  
C3. From the bottom right camera input cycle through the inputs until you see OBS

<br>

### <u>EXTRAS</u>

To mirror content in OBS, select the desired OBS layer and use the menu:  
`Edit > Transform > Flip Horizontally`

*Updated on 23.10.2020*
