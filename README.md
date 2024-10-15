Anbernic Unisoc T820 Bootloader Unlock Guide - TheGammaSqueeze - https://github.com/TheGammaSqueeze
---------------------------------------------------------------------------------------------------

The bootloader unlock is required before flashing any custom firmware or custom fixes.
You may be interested in this analog stick sensitvity fix after unlocking your bootloader: https://github.com/TheGammaSqueeze/Bootloader_Unlock_Anbernic_T820/releases/tag/analog_fix

Warning:
- Proceed at your own risk. Unlocking the bootloader will void your warranty and can potentially damage your device. I am not responsible for any damage to your device or any data loss incurred.
- Only supported on Windows systems.


Important Notices:
- Data Erasure: Unlocking the bootloader will erase all data on your device. Your device will be factory reset to its original state.
- Unlock Warning: After unlocking, an unlock warning message will appear on the screen every time you boot your device. This is normal and cannot be removed.

Prerequisites:
- Unisoc USB Drivers: Install the Unisoc USB drivers located in the UnisocDrivers folder. This is essential for your computer to communicate with the device.

Unlocking Procedure:
- Shut Down Device: Ensure your device is completely shut down with no USB cable attached.
- Run Unlock Script: Open the unlock.bat script on your computer.

Connect Device:
- Within 30 seconds of running the script, hold down the HOME/BACK button on the turned-off unit.
- While holding the button, plug in the USB cable to your device.
- Continue Unlock Process: The unlock script will now proceed. You can release any buttons once the script is running.
- Wipe data: Your unit will now reboot. It will likely show the battery charging screen, in this case just turn on the device. Upon the second reboot you will be asked to wipe your device. Use the volume buttons to navigate to the wipe option, use the power button to confirm this option. Your unlock is now complete.

Locking bootloader:
- To lock your bootloader again, you will need to ensure you flash the original firmware back to avoid a brick. This will wipe your data again. Once this is done, it'll be as if you never unlocked or modified the device at all.
- Locking instructions: Enable USB Debugging, then use the following commands:
- - adb reboot bootloader
  - fastboot flashing lock
  - Press the home/back button to confirm you want to relock
  - fastboot reboot
 
Stock firmware package:
- RG 556: https://drive.google.com/file/d/1hYuUPBTHAghZXXVt5urnAhJP-_vofg3K/view?usp=sharing
- RG Cube: https://drive.google.com/file/d/1DBl9ZwvyqUdjMmetA2ekYWKS1uUcmI0b/view?usp=sharing
- RG 406v: https://drive.google.com/file/d/10ivdlP5CsVInWOa66RpjjCxLI38Lo1-2/view?usp=sharing

Credits:
This bootloader unlocking process is based on the work from the following repository: [TomKing062/CVE-2022-38694_unlock_bootloader](https://github.com/TomKing062/CVE-2022-38694_unlock_bootloader). We are using a modified version of this exploit specifically tailored for our Anbernic devices.

By following this guide, you acknowledge that you understand the risks involved in unlocking your device's bootloader. Ensure you have backed up all important data before proceeding.
