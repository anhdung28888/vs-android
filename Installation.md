# Installing vs-android #

  * Download the latest release of vs-android from [here](http://www.gavpugh.com/vs-android/).

  * Unzip it anywhere you want. The install process copies files out of it, so you can safely delete it when you're done.

  * Go into the `MsBuild` directory of what you just unzipped.

  * For Windows 2000 or XP, just double click on 'install\_vs2010.cmd', 'install\_vs2012.cmd', or 'install\_vs2013.cmd'. Depending on which Visual Studio you use. You can install for more than one, if you have multiple versions installed. They co-exist fine.

  * For Vista or Windows 7 you will need to right click 'install\_vs20XX.cmd', and choose to 'Run as Administrator". Don't worry, you can view the install batch file in notepad if you wish. All it does is copy files to the correct place in your Visual Studio install.

  * That's it. The command box that pops up should show a number of files as successfully copied. It will prompt you to press any key, and then close itself.

  * Feel free to delete the files you unzipped earlier. They are no longer required.

## Manual Install ##

If you don't want to run the 'install\_vx20XX.cmd' file, you can copy the files manually. Obviously skip these steps if you already installed it.

  * In the 'MSBuild' directory contained in the zip file is a directory named 'Android'.

  * Navigate to one of these directories, depending on whether you are running 32-bit or 64-bit windows, for VS2010:

`C:\Program Files\MSBuild\Microsoft.Cpp\v4.0\Platforms`

`C:\Program Files (x86)\MSBuild\Microsoft.Cpp\v4.0\Platforms`

  * For VS2012:

`C:\Program Files\MSBuild\Microsoft.Cpp\v4.0\V110\Platforms`

`C:\Program Files (x86)\MSBuild\Microsoft.Cpp\v4.0\V110\Platforms`

  * For VS2013:

`C:\Program Files\MSBuild\Microsoft.Cpp\v4.0\V120\Platforms`

`C:\Program Files (x86)\MSBuild\Microsoft.Cpp\v4.0\V120\Platforms`

  * In this directory will already be a 'Win32' subdirectory. Possibly an 'Itanium' and 'x64' directories too. You want that 'Android' directory to sit alongside them.

  * You should also copy the DLL from the "2010 DLL", "2012 DLL", or "2013 DLL" directory into the "Android" directory in the destination folder, too.

# NDK Setup #

  * Download the NDK from here: http://developer.android.com/sdk/ndk/index.html

  * Unzip it somewhere, and note the root directory.

  * You need to set an environment variable named **ANDROID\_NDK\_ROOT** which points to this directory. This can be done from the command line:
<pre>
setx ANDROID_NDK_ROOT c:\android-ndk-r10d<br>
</pre>



# SDK Setup #

  * Java is a prerequisite for the Android SDK. Install the x86 JDK from here:
http://www.oracle.com/technetwork/java/javase/downloads/index.html

  * I would recommend using the x86 version of the JDK, **not** the x64 one. People have reported issues with the x64 version, which go away when using the x86 one instead.

  * You'll also need the Android SDK itself, download it from here:
http://developer.android.com/sdk/index.html

  * Use the installer version. It's the easiest way. Be sure to run the 'SDK Manager' it installs afterwards, so it can download the latest packages.



# Ant Setup #

  * Download Ant from here:
http://ant.apache.org/

  * Unzip it somewhere, just like you did for the NDK.

  * Set an environment variable named **ANT\_HOME** to point to where you unzipped it. For example:
<pre>
setx ANT_HOME c:\apache-ant-1.9.4<br>
</pre>


# Finished #

  * At this point you can build NDK executables in Visual Studio!

  * If you already had any Visual Studio sessions open, you will need to close and reopen them to make use of the new 'Android' platform.

  * Go ahead and download the Sample Projects: [Compiling a simple Android app with vs-android](HowTo_Samples.md). It's an easy way to get started.

# Problems? #

  * Take a look here: [Troubleshooting](Troubleshooting.md)