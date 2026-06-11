# Sniff Mode
1. Refer to the Scan section to reset the board and disable ADV.
2. Connect a phone to the board’s Bluetooth device. Confirm the pairing dialog; once paired, the device appears in the paired list and shows a connected state, as below:
::::{grid} 1 1 2 2
:gutter: 2

:::{grid-item}
```{figure} assert/image7.png
:width: 60%
:align: center

```
:::

:::{grid-item}
```{figure} assert/image8.png
:width: 60%
:align: center

```
:::

::::

3. After connection, wait a moment—the console will print "»Sniff mode", indicating the device has entered Sniff mode.
4. Send `btskey` commands to disable Scan. Steps:
```
(a) btskey s: show current menu
(b) If in HFP HP Menu, then send
(c) btskey r: return to BTS2 Demo Main Menu, then send:
(d) btskey 1: select Generic Command
(e) btskey 7: select Scan mode
(f) btskey 0: disable scan
```
5. * Similar to the Scan current measurement method, select the sniff active current within one cycle, measure the active duration At and the average current AC, then measure the sleep duration St within the same cycle and the sleep average current Sc. Substitute these values into the following formula to calculate the average current consumption of sniff.
Formula: Average current = (Ac * 1000 * At + Sc * St)/(At + St)
![](assert/image11.png)
<div align="center"><strong> Select period</strong></div>


6. * The Sniff mode interval and attempt count depend on the phone. In this test, a OnePlus Ace 6 was used, and the attempt count was 4.