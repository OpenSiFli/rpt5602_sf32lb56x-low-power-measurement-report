# 测试说明
使用BLE例程可以测试典型的ADV和连接场景功耗（发射功率为0dBm），系统上电后例程自动开启ADV发送，通过HCPU的console发送命令修改ADV发送间隔和连接周期，发送的命令都要以回车换行符结尾。

PC 与调试板使用 USB Type-C 线连接后会枚举出两个串口，分别作为HCPU以及LCPU的console，如下图所示。

![](assert/image1.png)

串口设置参见下图：波特率均设置为 1000000。

![](assert/image2.png)

为便于控制测试条件，使用PA52作为HCPU的唤醒PIN。当唤醒PIN不为高电平时HCPU无法进人低功耗模式，此时可以通过console给HCPU发送命令执行指定任务，当唤醒PIN接高电平（即1.8V电压，下文如未特别说明，高电平均指1.8V电压）时，HCPU进人低功耗模式，此时HCPU无法响应console命令。

测试例程LCPU的主频为24MHz，HCPU与LCPU使用的低功耗模式为Standby模式。

HCPU 支持如下命令修改 BLE ADV 和连接周期，同时还可使用 btskey 命令操作菜单修改 BT 的配置。
* ble_config adv interval_in_ms: 其中interval_in_ms是毫秒为单位的 ADV 间隔；
例如：发送命令ble_config adv 100，可将 ADV 周期改为 100ms
* ble_config conn interval_in_ms: 其中interval_in_ms是毫秒为单位的连接周期；
例如：在连接之后发送ble_config conn 100，可将连接周期改为 100ms
