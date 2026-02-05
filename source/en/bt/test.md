# Testing Instructions
Use the BT example to measure power in Scan and Sniff modes (TX power 0 dBm). After power-on, the test example automatically enables Scan and ADV. Connect a phone to the Bluetooth device. Use the HCPU console to send commands and change settings. Commands must end with carriage return and newline (CRLF).

After connecting the PC and the board with a USB Type‑C cable, two serial ports will appear, serving as the consoles for HCPU and LCPU, as shown below.

![](assert/image1.png)

Serial settings: set the baud rate to 1,000,000 for both ports.

![](assert/image2.png)

To control test conditions, use PA52 as the HCPU wake-up pin. When the wake-up pin is not high, HCPU cannot enter low-power mode and can process console commands. When the wake-up pin is high (1.8 V unless otherwise noted), HCPU enters low-power mode and cannot respond to console commands.

In this test example, LCPU runs at 24 MHz. Both HCPU and LCPU use the Standby low-power mode.
Use `btskey` commands to operate the menu and change BT configuration.
