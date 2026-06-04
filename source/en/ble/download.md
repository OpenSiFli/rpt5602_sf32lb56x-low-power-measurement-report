# Build and Flash the Example
## Build
If you already have a prebuilt image, skip to the flashing section to start testing.
Go to `example\pm\bt\project\hcpu`.
If your board is `sf32lb56-wlan-core_a128r12n1`, build with:
```
scons --board=sf32lb56-wlan-core_a128r12n1 -j8 
```
If your board is `sf32lb56-wlan-core_n16r12n1`, build with:
```
scons --board=sf32lb56-wlan-core_n16r12n1 -j8 
```

For `sf32lb56-wlan-core_a128r12n1`, the built image is stored under the `build` directory.

![](assert/image3.png)


## Flash the Image
In the build directory, run:
```
build_sf32lb56-wlan-core_a128r12n1_hcpu\uart_download.bat
```
This flashes the image built under `build`.

## Transmit Power Configuration
The project is configured with a default transmit power of 0 dBm. Use the command `ble_tx_pwr_save x` to adjust transmit power, where x represents the target power value in dBm.Example: To set transmit power to 10 dBm, run `ble_tx_pwr_save 10`.The device will automatically reboot for the setting to take effect after modification.