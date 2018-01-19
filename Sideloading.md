<!-- Sideloading - once you've created, run and tested your app, it's time to download or "sideload" - installing the XCode project onto your phone -->

Tools Needed: 

  - iCloud Account: your login details for your iCloud account
  - iPhone
  - USB Cable 
  - Xcode 
  - Internet 
  
<!-- Steps to Sideload your XCode project -->
  
1. **MOST IMPORTANT STEP** First Step - Ensure that your XCode version (the number after the period) matches with your iOS version on your iPhone (i.e. iOS 11.1 and XCode 9.1)
2. In XCode, select Project Navigator > project title > if project and target list are not showing in the middle pane, click on top left button to "unhide" > select target > Select General from top menu option 
3. In General tab - make sure you have the Bundle Identifier field filled in (i.e. com.charityyounblood.projectname)
4. In Signing field, below Identity - make sure that "Automatically manage signing" button is checked 
5. Select the Team drop down menu > select add account > this will take you to your Sign In for iCloud > enter log in credentials
6. This will take you to the accounts menu > close window
7. In Team drop down menu > select Charity Youngblood 
8. Connect your iPhone device to the laptop via USB > To make sure you have the right device selected, click on Product tab > Destination drop down menu > Select your device 
9. In top status bar, next to Run button, you should see your project name, followed by your device name
10. Click Run
11. When pop up window comes up "code sign", or Mac OS wants to make changes or keychain - use the password for your Mac Laptop (admin password)
12. ***IMPORTANT: ALWAYS ALLOW - NEVER SELECT DENY**
13. Make sure your iPhone is unlocked, then select Run in XCode
14. Another pop up window will appear in XCode, after build, "Could not launch" > Click ok to dismiss alert
15. On your iPhone, select and run app
16. On your iPhone, select Settings > General > Device Management > Developer App > click on blue "trust"
17. Go back to XCode, make sure your device is selected at top left, then click run
18. If any errors, pop up windows come up, first trouble shoot by unplugging USB from laptop, closing XCode, then relaunching 
