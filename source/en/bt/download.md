# Build and Flash
## Build
If you already have a compiled image file, you can skip to the flashing section to start testing.
Go to `example\pm\coremark\project\hcpu`.
If your board model is `sf32lb56-wlan_core_a128r12n1`, build with:
```
scons --board=sf32lb56-wlan_core_a128r12n1 -j8 
```
If your board model is `sf32lb56-wlan_core_n16r12n1`, build with:
```
scons --board=sf32lb56-wlan_core_n16r12n1 -j8 
```

Using `sf32lb56-wlan_core_a128r12n1` as an example, the compiled image is saved under the `build` directory.

![](assert/image3.png)

The default transmit power is 0 dBm. To test power consumption at 10 dBm, run in the HCPU project directory:
```
menuconfig --board=sf32lb56-wlan_core_a128r12n1
```
Open the `menuconfig` configuration menu, change the three values shown in the figure to `10`, save and exit, then build a new image.

![](assert/image4.png)

## Flash Image
In the build output directory, run:
```
build_sf32lb56-wlan_core_a128r12n1_hcpu\uart_download.bat
```
Flash the compiled image from the `build` directory.