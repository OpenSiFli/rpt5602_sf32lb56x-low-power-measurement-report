# While Loop
## HPSYS
1. * 打开串口调试工具，连接 HCPU 与 LCPU 的 console 串口，连接测量设备与被测模块
2. * 复位，启动成功后在 HCPU 的 console 中出现如下图的 log
```{figure} assert/image4.png
:align: center
```
3. * 发送命令 lcpu on，指示LCPU进入 wfi 模式，LCPU启动后会显示如下图所示的 log
```{figure} assert/image9.png
:width: 70%
:align: center
```
4. * 发送命令run_while_loop 240，指示HCPU在240MHz频率下执行whileloop测试，测量此时的平均电流C1，如HCPU While Loop 测试电流图所示，阶段1是HCPU跑在240MHz主频时WFI模式下的电流波形，开始执行whileloop后进人阶段2，电流上升并保持至测试结束，阶段3为回到WFI模式的电流波形。console 中显示HCPU 的频率和whileloop的持续时间，如HCPU While Loop Log 图所示
5. * 发送命令run_while_loop 192，指示HCPU在192MHz下执行while loop测试，测量此时的平均电流C2，
由此得到每MHz的电流增量为C=(C1-C2)/(240-192)

```{figure} assert/image5.png
:align: center

HCPU While Loop 测试电流图
```

```{figure} assert/image6.png
:align: center

HCPU While Loop Log 图
```
## LPSYS
1. * 打开串口调试工具，同时连接HCPU和LCPU的 console串口，连接测量设备与被测模块
2. * HCPU的串口窗口发送命令 lcpu on，指示LCPU进入 wfi 模式，LCPU启动后会显示如下图所示的 log
```{figure} assert/image9.png
:width: 70%
:align: center
```
3. * 将唤醒PIN接高电平使HPSYS进人低功耗模式
4. * 在LCPU的console中发送命令run_while_loop 48，指示LCPU在48MHz频率下执行while loop测试，测量此时的平均电流C1
5. * 发送命令run_while_loop 24，指示LCPU在24MHz下执行while loop测试，测量此时的平均电流C2，由此得到每MHz的电流增量为C=(C1-C2)/(48-24)



