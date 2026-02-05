# Device Initialization
When testing BLE for the first time on the board, run the following initialization commands after power-on (flashing the file system image clears the BLE address, so reconfigure it). Execute commands in the HCPU console; keep the wake-up pin low to prevent HPSYS from entering low-power mode, otherwise HCPU cannot process commands.
* `nvds reset_all 1`
* `nvds update addr 6 <BLE_ADDRESS>`

For example: `nvds update addr 6 1234567890C8`. Keep the address format consistent; it is recommended not to change the trailing `C8`, while other parts can be customized. After the commands complete, press Reset to reboot the device.
