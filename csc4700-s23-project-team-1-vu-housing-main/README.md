# csc4700-s23-project-team-1-vu-housing
csc4700-s23-project-team-1-vu-housing created by Jimmy Gamboli, Daniel Perez, Rowan Dillon, and Peter Carr

The following describes the steps required to setup and install our application for IOS and Android. 

Make sure to navigate into the VUHousing Folder before executing any commands:

`cd VUHousing`

---
**To run the application on ios:**

Step 1: install npm dependencies \
`npm install`

Step 2: install axios package (required to run application) \
`npm install axios`

Step 3: Switch to the ios directory \
`cd ios`

Step 4: update cocoapods dependencies (IOS only) \
`pod install`

Step 5: nativate to the root directory \
`cd ..`

Step 6: start the application \
`npx react-native run-ios`

The metro server should start automatically and appear on a second terminal window which can be used to load the application onto an IOS emulator. 

--- 

**To run the application on android:**

Step 1: Verify android device is connected: `adb devices` should show a device as connected. 

Step 2: Reverse android internal development port \
`adb -s <device name> reverse tcp:8081 tcp:8081`

Step 3: Run `npm install` \
-> (If Build Error occurs, delete /node-modules then run `npm install` again)

Step 4: Start Application \
`npx react-native run-android`

If the metro server (there should be a popup window with a metro logo while building) does not start on its own, 
run `npx react-native start` before step 4. 
