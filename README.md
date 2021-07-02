Construct Yodo1 MAS plugin<br>
=====
This is an Yodo1 MAS plugin for Cordova.

When you integrate the SDK, you import the SDK library file into your project so you can use that file’s functions. Integrating the MAS SDK into your mobile app project gives you access to MAS's fully managed monetization solution. This solution taps into multiple add mediation platforms, selecting the one best suited for your game and monetizing through high quality ad networks that serve in-app ads.

Before you can start monetizing your app, you’ll need to integrate the MAS SDK.

Integrating the SDK
----------
First of all, you need download this repository.

yodo1-construct.c3p file contains construct3 project, just open it with construct.
The project contains 2 main files.

* main.js - all initialization code related to MAS.
* Event sheet 1 - examples of the events.
You can use this code and events in your project.

## Platform SDK supported ##

* latest iOS
* latest Android

## Quick start ##
Demo project are ready to be exported to cordova project.
Basically you are going to build cordova project to android or ios platforms.


1. Change Id and MAS app ids in consruct3 project. You can find app ids on MAS dashboard.
<img src="/images/bundleId_and_appId.png" width="700">

2. Add events for button using Event sheet. Event type should be on clicked. Action should be javascript. Take a look at screenshot below.
<img src="/images/add_btn_event.png" width="700">

3. Export construct project to android or ios cordova project. It does not matter with one because it will be possible to compile cordova project 
to the both ios and android.

4. Now you have a cordova project. Use terminal commands to prepare a project. 
```bash
cordova prepare
cordova platform add ios
cordova platform add android
cordova plugin add cordova-plugin-device
```

5. Clone MAS cordova plugin via git clone, or download it from here: https://github.com/nazgull30/CordovaYodo1Mas.git
6. In the cloned MAS cordova plugin folder you need to put your admob id for both ios and android platforms.

Android:
```
    <config-file target="AndroidManifest.xml" parent="/manifest/application" >
      <meta-data
              android:name="com.google.android.gms.ads.APPLICATION_ID"
              android:value="PUT ADMOB ID HERE"/>
    </config-file>
```

iOs:
```
    <config-file target="*-Info.plist" parent="GADApplicationIdentifier">
      <string>PUT ADMOB ID HERE</string>
    </config-file>
```
7. In terminal from you construct codova project (step 3) add cordova plugin with the command `cordova plugin add PATH_TO_CLONED_CORDOVA_PLUGIN_HERE`
folders platform/android and platform/ios contain android and ios projects. You can open android project with Android Studio and ios project with xCode (open xcworkspace file).

If you want a debug build for android them use command `cordova build android`. 

For ios: open the workspace from platform/ios folder.


