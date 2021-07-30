### The source code of ImMut
The source code of ImMut consists of two parts and you can download them in the following links:
* (1) hook apps and inject external-source images with large ones: [ImageInjector](www.abc.com).
* (2) copy-past a repeatable fragment and slightly mutating the copies to display many (potentially distinct) images: [InputGenerator](www.abc.com).

### The usage of ImMut

Runtime environment requirements of ImMut tool:
* Android studio 4.2, IntelliJ 2020.2.3.

Running ImMut consists of three steps:
* Step 1: root Android simulator and install Xposed 
     * create a virtual device: Nexus 6, 1440*2560, 560dpi, API level 27.
     * root Android simulator. 
     * install Xposed in the Android simulator.
* Step 2: generate and install tool apk: used to hook the running Android apps (replace image resource and collect execution trace information)
     * import project "ImageInjector" to Android Studio.
     * add the package name of the apk you want to test at the end of the local variable "testAppNames".
     * build the project and generate an apk file.  
     * install the apk file in the Android simulator.
     * open Xposed and select "ImageInjector" in the "Modules".
* Step 3: import project and test user's Android app
     * import the project `inputgenerator` in intelliJ.
     * open the .kt file `edu.nju.ics.alex.inputgenerator.Main.kt`, modify five variables:
          * modify global variable `apkPath`: path to the folder where apks to be tested are stored.
          * modify global variable `directoryPath`: path to the folder where the running results are stored.
          * modify local variable `target_fileName`: the file name of functional test case
          * modify local variable `apkName`: the name of the apk to be tested
          * modify local variable `packageName`: the package name of the apk to be tested
     * run `inputgenerator`

Results
* The detection results are in the file directory of `directoryPath`.
