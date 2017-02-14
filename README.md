# Android-Installation-Procedure

  <h4>Download Android Studio</h4>

     Google provides Android Studio for the Windows, Mac OS X, and Linux platforms.<br>
     You can download this software from the Android Studio homepage<br>
                           
     (You'll also find the traditional SDKs, with Android Studio's command-line tools, available from the Downloads page.) 
     <br>Before downloading Android Studio, make sure your platform meets one of the following requirements:
        <br>
              Download link-->>https://developer.android.com/studio/index.html
<br>
  <h4>Windows OS</h4></br>
<h5>
 > Microsoft Windows 7/8/10 (32-bit or 64-bit)<br>
 > 2 GB RAM minimum, 8 GB RAM recommended<br>
 > 2 GB of available disk space minimum, 4 GB Recommended (500 MB for IDE + 1.5 GB for Android SDK and emulator system image)
   1280 x 800 minimum screen resolution<br>
   JDK 8
</h5>


Step 1 : Download Android stuido and android tool in windows<br><br>
Step 2 : Extract Android Studio and tools<br><br>
Step 3 : Go to Android studio => bin folder Click on the studio Application<br><br>
Step 4 : Launch Android Studio ⇒ Check "I do not have previous version of Android Studio" ⇒ Android studio setup wizard will download more SDK components ⇒ Wait for it to complete ⇒ Finish.<br><br>

Step 5 : Select "Configure" ⇒ "SDK Manager" ⇒ Select "SDK Tools" tab ⇒ Check "Android Support Library", "Intel x86 Emulator Accelerator (HAXM Installer)" and "Google USB Driver" ⇒ Apply.<br><br>


<h4>Ubundu OS </h4>
<br>
Step 1 : Download Android stuido and android tool in Ubundu<br><br>
Step 2 : Extract Android Studio and tools  don't use folder<br><br>
Step 3 : Open with terminal Android Studio path using Terminal<br><br>
  (Ex)
      $ cd Document/android-studio/bin/ 
      <br><br>
         ./studio.sh
       <br><br>
Step 4 : Launch Android Studio ⇒ Check "I do not have previous version of Android Studio" ⇒ Android studio setup wizard will download more SDK components ⇒ Wait for it to complete ⇒ Finish.<br><br>

Step 5 : Select "Configure" ⇒ "SDK Manager" ⇒ Select "SDK Tools" tab ⇒ Check "Android Support Library", "Intel x86 Emulator Accelerator (HAXM Installer)" and "Google USB Driver" ⇒ Apply.<br><br>

<h4>Occur type of Error Installion Time :</h4> 
 <br><br>
<h5>Cannot launch AVD in emulator.</h5>
<br><br>
Output:
<br><br>
sh: 1: glxinfo: not found<br><br>
sh: 1: glxinfo: not found<br><br>
libGL error: unable to load driver: radeonsi_dri.so<br>
libGL error: driver pointer missing<br>
libGL error: failed to load driver: radeonsi<br>
libGL error: unable to load driver: swrast_dri.so<br>
libGL error: failed to load driver: swrast<br>
X Error of failed request:  BadValue (integer parameter out of range for operation)<br>
  Major opcode of failed request:  155 (GLX)<br>
  Minor opcode of failed request:  24 (X_GLXCreateNewContext)<br>
  Value in failed request:  0x0<br>
  Serial number of failed request:  33<br>
  Current serial number in output stream:  34<br>
QObject::~QObject: Timers cannot be stopped from another thread<br>
<b>Answer:</b>
<br><br>
  I am using Android Studio 2.1.1 and Ubuntu 16.04 (x64). 
  <br>The following solved the problems ("sh: 1: glxinfo: not found" and "libGL error:..") for me.<br><br>
Step 1 : $ sudo apt-get install lib64stdc++6 (if it is not installed)<br><br>
Step 2 : $ cd ~/Android/Sdk/tools/lib64/libstdc++<br><br>
Step 3 : $ mv libstdc++.so.6 libstdc++.so.6.original<br><br>
Step 4 : $ ln -s /usr/lib64/libstdc++.so.6 ~/Android/Sdk/tools/lib64/libstdc++<br><br>
Step 5 : $ sudo apt-get install mesa-utils (if it is not installed)<br><br>
