# Various android commands
## ADB
* List of connected devices<br>
`adb devices`
* Direct command to a specific device<br>
`adb -s <device_serialNumber> <command>`
* Install an application<br>
`adb install <path_to_apk>`
* Uninstall an application<br>
`adb uninstall <application_package>`
* Stop the adb server<br>
`adb kill-server`
* Run test on a device or emulator<br>
`adb shell am instrument -w <test_package_name>/<runner_class>`
* Run test on a device or emulator using InstrumentationTestRunner<br>
`adb shell am instrument -w <test_package_name>/android.test.InstrumentationTestRunner`
* Run a specific test class<br>
`adb shell am instrument -w -e class <class_name> <test_package_name>/android.test.InstrumentationTestRunner`
* Run a specific test class and test method<br>
`adb shell am instrument -w -e class <class_name>#<method_name> <test_package_name>/android.test.InstrumentationTestRunner`
* Option to set debug mode
`.. -e debug true .. `
