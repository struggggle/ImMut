### The source code of ImMut
The source code of ImMut consists of two parts and you can download them in the following links:
* (1) hook apps and inject external-source images with large ones: [ImageInjector](https://github.com/struggggle/ImageInjector).
* (2) copy-past a repeatable fragment and slightly mutating the copies to display many (potentially distinct) images: [InputGenerator](https://github.com/struggggle/InputGenerator).

### The usage of ImMut

Requirements for building and running the ImMut tool:
* Mac (tested on macOS 10.14), 16 GB memory
* JDK 1.8 and Gradle 7.1.1


Running ImMut consists of three steps:
* Step 1: root Android simulator and install Xposed 
     * create a virtual device (Nexus 6, 1440*2560, 560dpi, API level 27) and name it Nexus_6_API_27.
     * root the created virtual device. 
     * install Xposed in the virtual device.
* Step 2: install the tool apk: used to hook the running Android apps (replace image resource and collect execution trace information)
     * start the created virtual device
     ```
     $ $emulatorPath/emulator -avd Nexus_6_API_27 -writable-system
     ``` 
     * import project "ImageInjector" to Android Studio.
     * add the package name of the apk you want to test at the end of the local variable "testAppNames".
     * build the project and generate a signed apk file.  
     * install the apk file in the Android simulator.
     * open Xposed and select "ImageInjector" in the "Modules".
     
* Step 3: build and run InputGenerator
     * build and run InputGenerator:
     ```
     $ git clone https://github.com/struggggle/InputGenerator.git
     $ cd InputGenerator
     $ ./gradlew build
     $ java -cp build/classes/java/main:libs/*:build/classes/kotlin/main  edu.nju.ics.alex.inputgenerator.MainKt $apkPath  $directoryPath $test_case_name $apkName $packageName
     ```
     
`$apkPath` is the path to the folder where apks to be tested are stored.
`$directoryPath` is the path to the folder where the running results are stored.
`target_fileName` is the file name of functional test case
`apkName` is the name of the apk to be tested
`packageName` is the package name of the apk to be tested
An example of the `java` commond:
```
     java -cp build/classes/java/main:libs/*:build/classes/kotlin/main  edu.nju.ics.alex.inputgenerator.MainKt /testInput/apks/ /testInput addTwoPasses.sh org.ligi.passandroid_356_apps.evozi.com org.ligi.passandroid
```

Results
* The detection results are in the file directory of `directoryPath`.
