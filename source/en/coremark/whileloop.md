# While Loop
## HPSYS
1. Open the serial terminal and connect to the HCPU and LCPU consoles. Connect the measurement device and the module under test.
2. Reset. After a successful boot, the HCPU console prints logs as shown below.
```{figure} assert/image4.png
:align: center
```
3. Send `lcpu on` to set LCPU into WFI mode. After LCPU starts, logs appear as below.
```{figure} assert/image9.png
:width: 70%
:align: center
```
4. Send `run_while_loop 240` to run the while-loop test at 240 MHz and measure average current `C1`. As shown in the HCPU While Loop current figure: Phase 1 is the WFI waveform at 240 MHz; after starting the while loop (Phase 2), current rises and remains until the test ends; Phase 3 is the return to WFI. The console shows HCPU frequency and while-loop duration.
5. Send `run_while_loop 192` to run at 192 MHz and measure average current `C2`. The per-MHz increment is `C = (C1 − C2) / (240 − 192)`.

```{figure} assert/image5.png
:align: center

HCPU While Loop 测试电流图
```

```{figure} assert/image6.png
:align: center

HCPU While Loop Log 图
```
## LPSYS
1. Open the serial terminal and connect to both HCPU and LCPU consoles. Connect the measurement device and the module under test.
2. In the HCPU console, send `lcpu on` to set LCPU into WFI mode. After LCPU starts, logs appear as below.
```{figure} assert/image9.png
:width: 70%
:align: center
```
3. Set the wake-up pin high to put HPSYS into low-power mode.
4. In the LCPU console, send `run_while_loop 48` to run at 48 MHz and measure average current `C1`.
5. Send `run_while_loop 24` to run at 24 MHz and measure average current `C2`. The per-MHz increment is `C = (C1 − C2) / (48 − 24)`.



