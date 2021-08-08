---
title: The Usage of ImMut
---
#### The usage of ImMut

Requirements for running ImMut:
* Mac (tested on macOS 10.14), 16 GB memory
* JDK 1.8 and Android Studio 4.2.2


Running ImMut consists of two steps:
* Step 1: create Android virtual device and install Xposed 
     * create an Android virtual device (Nexus 6, 1440*2560, 560dpi, API level 27) and name it Nexus_6_API_27.
     * root the Android virtual device. 
     * install Xposed in the Android virtual device.
     
     **Note:** we have provided the running environment and you can download the [avd.zip](https://drive.google.com/file/d/1Wa-yXkT80lkrO2HTMOGBUTBp7hujw3fC/view?usp=sharing). Then, you can unzip avd.zip and copy-paste the contants in avd folder to path `~/.android/avd/`
   
  
* Step 2: run ImMut
     * start Android virtual device
     ```
     $ ~/Library/Android/sdk/emulator/emulator -avd Nexus_6_API_27 -writable-system
     ```
     * execute ImMut:
     download and unzip [ImMut.zip](https://drive.google.com/file/d/1ZGSSwGo5PH3iMx-OR__rWKncwLiN1CEq/view?usp=sharing)
     ```
     $ cd ImMut
     $ java -cp edu.nju.ics.alex.inputgenerator.MainKt  inputgenerator.jar:libs/*  $apkPath  $directoryPath $test_case_name $apkName $packageName
     ```
     
`$apkPath` is the path to the folder where apks to be tested are stored.
`$directoryPath` is the path to the folder where the running results are stored.
`target_fileName` is the file name of functional test case.
`apkName` is the name of the apk to be tested.
`packageName` is the package name of the apk to be tested.

An example of the `java` commond:
```
     java -cp edu.nju.ics.alex.inputgenerator.MainKt  inputgenerator.jar:libs/*  $savePath/testInput/apks/ /testInput addTwoPasses.sh org.ligi.passandroid_356_apps.evozi.com org.ligi.passandroid
```

Results
* The detection results are in the file directory of `$directoryPath`.

### The source code of ImMut
The source code of ImMut consists of two parts and you can download them in the following links:
* (1) hook apps and inject external-source images with large ones: [ImageInjector](sourceCode.html).
* (2) copy-past a repeatable fragment and slightly mutate the copies to display many (potentially distinct) images: [InputGenerator](sourceCode.html).
