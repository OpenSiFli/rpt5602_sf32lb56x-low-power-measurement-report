# 测试说明
CoreMark 例程测试以下场景下的功耗:
* 一个核执行 CoreMark 基准测试程序
* 一个核执行一段时间的 while 循环，循环中执行 nop 指令
* 系统关机，可由 RTC 定时唤醒
* 系统关机，由唤醒引脚唤醒

为便于控制测试条件，使用PA52作为HCPU的唤醒PIN。当唤醒PIN不为高电平时HCPU无法进人低功耗模式，此时可以通过console给HCPU发送命令执行指定任务，当唤醒PIN接高电平（即1.8V电压，下文如未特别说明，高电平均指1.8V电压）时，HCPU进人低功耗模式，此时HCPU无法响应console命令。

LCPU始终不进人低功耗模式，如果启动了LCPU，当不执行任务时LCPU处于WFI状态，可以响应来自console的命令，未启动LCPU时，则认为LCPU处于halt状态，无法处理console命令。

需要注意发送的命令都要以回车换行符结尾。

PC 与调试板使用 USB Type-C 线连接后会枚举出两个串口，分别作为HCPU以及LCPU的console，如下图所示。

![](assert/image2.png)

串口设置参见下图，波特率均设置为 1000000。

![](assert/image1.png)

非关机场景下，当一个核在执行指定任务时，另外一个核需进人如下状态以保证测量值的准确
* HCPU 执行任务时，LCPU 处于wfi 状态 (hcpu的console端发送 lcpu on 命令)
* LCPU执行任务时，HCPU进人Standby低功耗模式 (唤醒pin接高电平)

HCPU 可使用以下命令启动相应任务：
* run_coremark freq_in_mhz：修改主频并执行 CoreMark，freq_in_mhz是以 MHz 为单位的频率
例如：run_coremark 48，以 48MHz 主频执行 CoreMark
* run_while_loop freq_in_mhz：修改主频并执行一段时间 while loop，freq_in_mhz是以 MHz 为单位的频率
例如：run_while_loop 48，以 48MHz 主频执行 while loop

HCPU还支持以下命令：
* lcpu on:启动LCPU，启动成功后LCPU可以接收console命令执行指定任务
* shutdown[wakeup_time_in_sec]:关机，wakeup_time_in_sec为可选参数，单位为秒，表示关机后多久自动开机，如果不带参数，则关机后只能被唤醒引脚唤醒

注：由于编译采用 Ofast 优化等级，跑分结果仅作参考，并不能达到 Omax 时的最高分。