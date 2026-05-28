# Connection Scenario
1. * Open a serial terminal, connect to the HCPU console UART, and connect the measurement equipment to the device under test.
2. * Pull the wake PIN low and power-cycle the development board. After successful reset the log shown below appears. As in the ADV section, disable BT Scan when measuring ADV current.

```{figure} assert/image8.png
:width: 50%
:align: center
```

3. * On a phone open the LightBlue app as shown below. In the Scan list find the device named SIFLI_APP and tap CONNECT to connect.

```{figure} assert/image9.png
:width: 40%
:align: center
```

4. * After a successful connection BLE enters the connected state. The default connection interval is 15 ms.

5. * Pull the wake PIN low to exit low-power mode. In the console send `ble_config conn 50` to change the connection interval to 50 ms. Confirm the console prints the message shown below — for example, `Updated connection interval: 40` indicates a connection interval in units of 1.25 ms, so 40 × 1.25 = 50 ms. If the message does not appear the parameter update failed and you should resend the command and observe the current waveform to verify the interval update.

```{figure} assert/image10.png
:width: 70%
:align: center
```

6. * Pull the wake PIN high to enter low-power mode. Similar to ADV current measurement, select one cycle, measure the active current to obtain active duration `At` and average active current `Ac`, and measure the sleep duration `St` and average sleep current `Sc`. Substitute into the formula below to compute the average current consumption.
Calculation formula: Average current = (Ac * 1000 * At + Sc * St) / (At + St)
![](assert/image11.png)
<div align="center"><strong>Cycle selection</strong></div>

Repeat steps 5 and 6 to measure current for connection intervals of 50 ms, 100 ms, 200 ms, 500 ms, and 1000 ms.
