# Device Initialization
When testing Bluetooth on the board for the first time, run the following initialization commands after power-on. Execute them in the HCPU console. Keep the wake-up pin low to prevent HPSYS from entering low-power mode; otherwise, HCPU cannot process commands.
1. `nvds reset_all 1`
2. `nvds update addr 6 <BT_ADDRESS>`

Example: `nvds update addr 6 1234567890C8`. Keep the address format consistent; it is recommended not to change the trailing `C8`, while other parts can be customized. After the commands complete, press Reset to reboot the device.