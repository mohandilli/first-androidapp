<b> Steps to create a hello world android application: </b><br />
1.Download eclipse,<a href='http://developer.android.com/sdk/index.html'>android SDK</a>,<a href='http://ant.apache.org/bindownload.cgi'>Ant 1.8 or above.</a> <br />
2.Install android plugin in eclipse using  android plugin - http://dl-ssl.google.com/android/eclipse/ <br />
3.create a android project using New-->others-->android-->android project <br />
4.set path=%path%;%SDK\_HOME%\tools;%SDK\_HOME%\platforms-tools; in env variables.In my case SDK\_HOME=D:\Mohan\Android App Development\android-sdk\android-sdk-windows <br />
5.open command prompt and traverse to the newly created project root folder.In my case it was "D:\Mohan\AndroidAppDev\WS\TestProject" <br />
6.Type the below command to generate the build.xml file. <br />
<b>android update project -t 2 -p . <br>
<br>
Unknown end tag for </B><br>
<br>
 <br />
Succes message will appear in the console if build.xml is generated sucessfully.<br />
7.Type below command to create a .apk in the bin folder.".apk" file a archive just like jar or war that will be installed in the mobile device or emulator as an application.<br />

<b>ant debug</b> <br />
you should get the build successfull. <br />
8.Once the build is successfull your application is ready to be deployed in the emulator.<br />
9.Traverse into the bin folder which is a step ahead from your current directory in the command prompt.<br />
10.Type the below command to start the emulator<br />

<b>emulator -avd emulator_name -scale 76dpi </b><br />

<b><font color='red'>Note:</font>This will take few minutes to start be patient untill the emulator has been started.</b><br />
11.Type the below command to install the "project_name"-debug.apk.In my case the project .apk was TestProjectActivity-debug.apk <br />
<b>adb install apk filename </b> <br />
(i.e)In my case<br />
<b>adb install TestProjectActivity-debug.apk</b><br />
12.Its time to enjoy your own application in the emulator.You should able to find app icon with the project name in the list of app's.<br />

<b>Logging related stuffs </b><br />
If your env variable's are properly configured with SDK_HOME\tools then just open a new command prompt and type below command to open dalvik debug monitor to see the application ans system out logs<br />
<b>ddms</b>


Happy Coding :)