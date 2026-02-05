# Testing Instructions
Use the BLE example to measure typical ADV and connection power consumption (TX power 0 dBm). After power-on, the example automatically starts advertising. Send commands via the HCPU console to change the advertising interval and the connection interval. Commands must end with a carriage return and newline (CRLF).

After connecting the PC and the board with a USB Type‑C cable, two serial ports will appear, serving as the consoles for HCPU and LCPU, as shown below.

![](assert/image1.png)

Serial settings: set the baud rate to 1,000,000 for both ports.

![](assert/image2.png)

To control test conditions, use PA52 as the HCPU wake-up pin. When the wake-up pin is not high, HCPU cannot enter low-power mode, and you can send commands via the console for specific tasks. When the wake-up pin is high (1.8 V unless noted otherwise), HCPU enters low-power mode and cannot respond to console commands.

In this test example, LCPU runs at 24 MHz. Both HCPU and LCPU use the Standby low-power mode.

HCPU supports the following commands to modify the BLE advertising and connection intervals. You can also use the `btskey` command to operate the BT configuration menu.
* `ble_config adv <interval_ms>`: Advertising interval in milliseconds.
	Example: `ble_config adv 100` sets the ADV period to 100 ms.
* `ble_config conn <interval_ms>`: Connection interval in milliseconds.
	Example: after establishing a connection, `ble_config conn 100` sets the connection interval to 100 ms.
