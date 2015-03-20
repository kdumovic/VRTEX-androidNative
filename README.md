#VRTex-androidNative

### Instructions: Getting Eclipse to build Gear apps
####Mac OSX
You're in luck. I've already done this and Unix is pretty nice. I zipped up my installation of all the resources, so just unpack, follow the instructions and do minor mods, and use:
[Download the Packaged IDE here, 6GB Gzipped](https://www.dropbox.com/s/7p398400zjkhm0y/oculusDev.tar.gz?dl=0)

- Download the prepackaged development set from this address (TBD) and unpack it into `~/oculusDev/`
  2. such that there is 3 folders in the `oculusDev` folder. 
- Set up your ~/.profile
```
export ANDROID_HOME=~/oculusDev/adt-bundle-mac-x86_64-20140702/sdk
export ANDROID_NDK=~/oculusDev/android-ndk-r10d
export PATH=$PATH:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools:$ANDROID_NDK
export JAVA_HOME=$(/usr/libexec/java_home)
```
- Install Apache Ant. You can do this through:
  3. `brew install ant` from HomeBrew if you have it.
  4. Or figuring out another way to do it following the android build instructions in the `mobilesdk.pdf`, found in `MobileSDK/Doc/`. The Apache Ant section is on page 26.
- Add the next thing to the `~/.profile`:
```
export ANT_HOME=/*WHEREVER THE Ant file IS Mine is at */
/*e.g. */ export ANT_HOME=/usr/local/Cellar/ant/1.9.4
```
  - if you're not sure, follow Pg 25 of `mobilesdk.pdf`

- add the Ant executable to your PATH variable. You can test this by typing `ant` in Terminal and seeing if anything pops up. If it's not found, then you should add Apache Ant's `bin` folder to PATH.


####Windows
This is tricky, so follow the instructions faithfully:
1. [Download Oculus Mobile SDK, which supports Gear](https://developer.oculus.com/downloads/#sdk=mobile)
1. follow the android build instructions in the `mobilesdk.pdf`, found in `MobileSDK/Doc/`. Start from Page 15 onwards. Remember to install 4.4.2 (API 19) and the ARM EABI v7a system image. Oculus Mobile SDK uses API Level 19.
2. Remember to install Android Native Development Kit from the Eclipse Install Software screen. This is just a reminder. Keep following the guide, you're doing good.
3. If you're on page 19, you're done! congrats.



