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
5. Similar to Scan current measurement, the Sniff-mode incremental current is the 10-second average current minus the sleep baseline between two peaks.

6. Sniff interval and attempt count depend on the phone. In this test with OnePlus Ace 6, attempt count is 4. The incremental current for a given interval can be derived from the current waveform. For example, if the Bluetooth active duration is `T = 7 ms` and average current is `I = 1.9 mA`, then for a 500 ms interval the incremental current is `ΔI = I × T / (500 ms − T) ≈ 27 µA`.