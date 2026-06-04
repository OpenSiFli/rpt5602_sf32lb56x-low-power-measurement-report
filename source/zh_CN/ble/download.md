# 例程编译与烧录
## 编译
如果使用已编译好的 image 文件，可以直接跳到烧录部分进行烧录开始测试。
进入example\pm\bt\project\hcpu目录
如果使用的开发板型号为 `sf32lb56-wlan-core_a128r12n1`,就使用如下命令进行编译
```
scons --board=sf32lb56-wlan-core_a128r12n1 -j8 
```
如果使用的开发板型号为 `sf32lb56-wlan-core_n16r12n1`,就使用如下命令进行编译
```
scons --board=sf32lb56-wlan-core_n16r12n1 -j8 
```

以`sf32lb56-wlan-core_a128r12n1`为例，编译生成的 image文件保存在 build 目录下。

![](assert/image3.png)


## 烧录镜像
在命令行编译的目录下执行
```
build_sf32lb56-wlan_core_a128r12n1_hcpu\uart_download.bat
```
烧写 build 目录下编译生成的镜像文件。

## 改变发射功率
工程默认配置的发射功率是0dbm，可以使用`ble_tx_pwr_save x`命令修改发射功率，x是需要修改的发射功率大小，例如改变发射功率为10dbm：`ble_tx_pwr_save 10` 。改完后会自动重启生效。