# CoreMark

## HPSYS
1. * 打开串口调试工具，连接 HCPU 与 LCPU 的 console 串口，连接测量设备与被测模块
2. * 复位，启动成功后在 HCPU 的 console 中出现如下图的 log

```{figure} assert/image4.png
:width: 60%
:align: center
```
3. * 发送命令 lcpu on，指示LCPU进入 wfi 模式，LCPU启动后会显示如下图所示的 log
```{figure} assert/image9.png
:width: 70%
:align: center
```
4. * 发送命令run_coremark 240得到平均电流C1，发送run_coremark 192得到平均电流C2，得到240MHz和192MHz的增量电流 C=(C1-C2)/(240-192)

5. * 如下图所示，阶段 1 是 HCPU 跑在 192MHz 主频时 WFI 模式下的电流波形，开始执行 CoreMark后进入阶段 2，电流上升并保持至测试结束，阶段 3 为回到 WFI 模式的电流波形
![](assert/image5.png)

## LPSYS
1. * 打开串口调试工具，同时连接HCPU和LCPU的 console串口，连接测量设备与被测模块
2. * HCPU的串口窗口发送命令 lcpu on，指示LCPU进入 wfi 模式，LCPU启动后会显示如下图所示的 log
```{figure} assert/image9.png
:width: 70%
:align: center
```
3. * 将唤醒PIN接高电平使HPSYS进人低功耗模式
4. * 在LCPU的console中发送命令run_coremark 48，指示LCPU在48MHz频率下执行CoreMark基准测试，测量此时的平均电流C1
5. * 发送命令run_coremark 24，指示LCPU在24MHz下执行CoreMark 基准测试，测量此时的平均电流C2，由此得到每MHz的电流增量为C=(C1-C2)/(48-24)