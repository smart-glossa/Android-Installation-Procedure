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
      <br>
        $ ./studio.sh
       <br>
Step 4 : Launch Android Studio ⇒ Check "I do not have previous version of Android Studio" ⇒ Android studio setup wizard will download more SDK components ⇒ Wait for it to complete ⇒ Finish.<br>

Step 5 : Select "Configure" ⇒ "SDK Manager" ⇒ Select "SDK Tools" tab ⇒ Check "Android Support Library", "Intel x86 Emulator Accelerator (HAXM Installer)" and "Google USB Driver" ⇒ Apply.<br>

<h4>Occur type of Error Installion Time :</h4> 
 <br>
 <b>Error 1</b>
 
<h5>Cannot launch AVD in emulator.</h5>
<br>
Output:
<br>
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

<b>Error 2</b>
<br>
IllegalArgumentException: Unable to locate adb<br>

Solution:
    
 >> In Android Studio, Click on 'Tools' on the top tab bar of android studio<br><br>
 >>  Tools >> Android >> SDK Manager >> Launch Standalone Sdk manager<br><br>
there you can clearly see which platform tool is missing , then just install that and your adb will start working properly.

<b>Error 3</b>

How To Change API SDK Level In Android Studio<br>

Solution :<br>

follow the link ===>http://abhiandroid.com/androidstudio/change-api-sdk-level-android-studio.html

<br>

<b>Error 4</b>

Session 'app': Error Installing APK
<br>
Solution :
<br>
You have to enable Developer options and enable USB Debugging:<br>

Step 1 : Go to the settings menu, and scroll down to "About phone." Tap it.<br>
Step 2 : Scroll down to the bottom again, where you see "Build number." (Your build number may vary from ours here.)
Tap it seven (7) times.<br> 
Step 3 : After the third tap, you'll see a playful dialog that says you're four taps away from being a developer. (If only it were that simple, eh?) Keep on tapping, and poof, you've got the developer settings back.<br>

<b>Error 5</b><br>
  Error running Application: Instant Run requires 'Tools | Android | Enable ADB integration' to be enabled.
  
  <br>
  Solution :<br>
  
     Step 1 : go to files<br> 
     Step 2 : go to setings <br> 
     Step 3 : click build,Execution,deployment<br> 
     Step 4 : select instant run <br>
     Step 5 : mark out the first point  Enable instant run to hot swap code<br>
     
     <b> Error 6</b><br>
     Error:Unable to start the daemon process.<br>
This problem might be caused by incorrect configuration of the daemon.<br>
For example, an unrecognized jvm option is used.<br>
Please refer to the user guide chapter on the daemon at https://docs.gradle.org/2.14.1/userguide/gradle_daemon.html<br>
Please read the following process output to find out more:<br>

Solution <br>
         his means the JVM hasn't enough memory space. Adding following property in the gradle.properties file will fix your problem:
<br>
   open projetct gradle.properties :<br>
    Added line:
<br>
     org.gradle.jvmargs=-Xmx512m -XX:MaxPermSize=512m
     <br>
     <b>Error 7</b>
     <br>
     Error:The supplied javaHome seems to be invalid. I cannot find the java executable. Tried location: D:\run\android-studio\jre\bin\java.exe<br>

  Solution:<br>
    
if you do not have JAVA_HOME Variable into environment variables then<br>

Set the JAVA_HOME Variable<br>

Once you have the JDK installation path:<br>

Step 1 : Right-click the My Computer icon on your desktop and select Properties.<br> 
Step 2 : Click the Advanced tab. Click the Environment Variables button.<br> 
Step 3 : Under System Variables, click New. Enter the variable name as JAVA_HOME.<br>
Step 4 : Enter the variable value as the installation path for the Java Development Kit. Click OK. Click Apply Changes.<br>
(Open with system right click --> open control panel home select  to Advenced system settings -->Environment variable ---> select New )
If you have JAVA_HOME value then<br>
Change the value of environment variable JAVA_HOME to C:\Program Files (x86)\Java\Jre7\ instead of C:\Program Files (x86)\Java\Jre7\bin\java.exe<br>
 or<br>
Change the value of environment variable JAVA_HOME to C:\Program Files (x86)\Java\Jdk7\ instead of C:\Program Files (x86)\Java\Jdk7\bin\java.exe<br>

JAVA_HOME should be always pointing to the parent directory of JDK or JRE installation inside of which, we find the bin directory containing the java, javac, etc. binaries
<br>                                                                  (AND)
    <br>              you can manually set JDK locato for your project :<br>
                 1.  Go to Android stdio file<br>
                 2.  Project Structure<br>
                 3.  JDK location box :Enter and browse to your JDK<br>
                 4.  ok<br>
               
