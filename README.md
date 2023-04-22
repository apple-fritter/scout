## Bloatware preempt
To preempt the installation of bloatware on a new or freshly reset device., you can follow these steps:

First, connect your device to your computer via USB cable and enable USB debugging mode in the device settings.

Open a command prompt or terminal window on your computer and type the following command to check if the device is connected properly:

```
adb devices
```

If the device is listed, then it is connected properly. If not, make sure USB debugging is enabled and that the correct drivers are installed for your device.

To disable the "android setup" process, use the following command:
```
adb shell pm disable-user --user 0 com.google.android.setupwizard
```

This will disable the setup wizard that runs when you first turn on the device.

To prevent bloatware from being installed on the device, you can use the following command:
```
adb shell pm disable-user --user 0 com.android.providers.downloads.ui
```

This will disable the download manager that is responsible for downloading and installing apps.

## Privacy
These steps will help you turn off Google's analytics/telemetry on your Android device. Please note that some features may not work properly if you turn off certain activity controls

To turn off "Web & App Activity" and "Location History" use the following commands:
```
adb shell settings put global google_activity_controls_enabled 0
adb shell settings put secure location_mode 0
```
These commands will turn off the toggles for "Web & App Activity" and "Location History" respectively.

To turn off "YouTube History" use the following command:
```
adb shell settings put global youtube_history_enabled 0
```
This command will turn off the toggle for "YouTube History."

To turn off "Ad personalization" use the following command:
```
adb shell settings put global pref_ads_personalization_enabled 0
```
This command will turn off the toggle for "Ad personalization."

To turn off "Opt out of Ads Personalization" use the following command:
```
adb shell settings put global opt_out_of_ads_personalization 1
```
This command will turn on the toggle for "Opt out of Ads Personalization."

To turn off usage and diagnostics reporting use the following command:
```
adb shell settings put global settings_global_send_action_opt_out 1
```
This command will turn off usage and diagnostics reporting.

## Note:

These commands may not work on all Android devices or versions. Additionally, some settings may be located in different places depending on the device and version of Android. Please be careful when entering these commands, as they may have unintended consequences if entered incorrectly.

## DISCLAIMER:
**This software is provided "as is" and without warranty of any kind**, express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose and noninfringement. In no event shall the authors or copyright holders be liable for any claim, damages or other liability, whether in an action of contract, tort or otherwise, arising from, out of or in connection with the software or the use or other dealings in the software.

**The authors do not endorse or support any harmful or malicious activities** that may be carried out with the software. It is the user's responsibility to ensure that their use of the software complies with all applicable laws and regulations.

## License

These files released under the [MIT License](LICENSE).
