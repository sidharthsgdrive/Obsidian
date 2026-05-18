Setup:
1. Navigate to Downloads/platform-tools-latest-windows/platform-tools/
2. Shift + Rightclick empty space in file explorer, select open Powershell here
3. Connect laptop to phone using USBC cable
4. `.\adb devices` and confirm that device is listed
5. `.\adb shell sh /sdcard/Android/data/moe.shizuku.privileged.api/start.sh`