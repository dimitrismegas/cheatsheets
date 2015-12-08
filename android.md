# Various android commands
## ADB
* List of connected devices<br>
`adb devices`
* Direct command to a specific device<br>
`adb -s <device_serialNumber> <command>`
* Install an application<br>
`adb install <path_to_apk>`
* Stop the adb server<br>
`adb kill-server`
* Run test on a device or emulator<br>
`adb shell am instrument -w <test_package_name>/<runner_class>`
* Run test on a device or emulator using InstrumentationTestRunner<br>
`adb shell am instrument -w <test_package_name>/android.test.InstrumentationTestRunner`
* Run a specific test class<br>
`adb shell am instrument -w -e class <class_name> <test_package_name>/android.test.InstrumentationTestRunner`
