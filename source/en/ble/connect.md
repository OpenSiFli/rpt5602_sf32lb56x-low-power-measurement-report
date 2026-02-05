# Connection Scenario
1. Open a serial debug tool, connect to the HCPU console port, and hook up the measurement device to the DUT.
2. Pull the wake-up pin low and power-cycle the board; upon successful reset you will see the log below. As in the ADV chapter, disable BT Scan before measuring current.

```{figure} assert/image8.png
:width: 50%
:align: center
```

3. On the phone, open LightBlue as shown, find `SIFLI_APP` in the Scan list, and tap CONNECT.

```{figure} assert/image9.png
:width: 40%
:align: center
```

4. After a successful connection, BLE enters the connected state with a default connection interval of 15 ms.

5. Pull the wake-up pin high to enter low-power mode and measure current at 15 ms interval.

6. Pull the wake-up pin low to exit low-power mode. In the console, send `ble_config conn 50` to set the interval to 50 ms. Confirm the console prints “Updated connection interval: 40”, where 40 means 40×1.25 ms = 50 ms. If no print appears, the update failed; resend the command and check the current waveform to confirm the interval.

```{figure} assert/image10.png
:width: 70%
:align: center
```

7. Pull the wake-up pin high to re-enter low-power mode. Measure current at 50 ms interval. As with ADV, record 10 s average current C1, sleep current C2 between peaks, and compute incremental current C=C1−C2.

Repeat steps 6 and 7 to measure current at connection intervals of 50 ms, 100 ms, 200 ms, 500 ms, and 1000 ms.
