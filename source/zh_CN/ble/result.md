# 测量结果汇总

表格中 ADV 与 Connection 的电流值为该模式的增量电流，standby 为睡眠电流，实际的平均电流等于增量电流与睡眠电流之和


## 测试结果表 - 3.8V转换数据

<div class="table-wrapper docutils container">
<table class="docutils align-default">
  <thead>
    <tr>
      <th class="head">模式</th>
      <th class="head">间隔 (ms)</th>
      <th class="head">电源电压：3.8V   TXpower 0dBm (uA)</th>
      <th class="head">电源电压：3.8V   TXpower 4dBm (uA)</th>
      <th class="head">电源电压：3.8V   TXpower 10dBm (uA)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="5">ADV</td>
      <td>50</td>
      <td>172.9</td>
      <td>184.8</td>
      <td>360.8</td>
    </tr>
    <tr>
      <td>100</td>
      <td>83.6</td>
      <td>102.8</td>
      <td>186.1</td>
    </tr>
    <tr>
      <td>200</td>
      <td>42.7</td>
      <td>52.3</td>
      <td>94.9</td>
    </tr>
    <tr>
      <td>500</td>
      <td>17.7</td>
      <td>21.2</td>
      <td>39.2</td>
    </tr>
    <tr>
      <td>1000</td>
      <td>8.9</td>
      <td>10.6</td>
      <td>19.5</td>
    </tr>
    <tr>
      <td rowspan="5">Connection</td>
      <td>50</td>
      <td>122.4</td>
      <td>130.7</td>
      <td>147.9</td>
    </tr>
    <tr>
      <td>100</td>
      <td>60.8</td>
      <td>64.8</td>
      <td>74.6</td>
    </tr>
    <tr>
      <td>200</td>
      <td>30.4</td>
      <td>32.4</td>
      <td>37.3</td>
    </tr>
    <tr>
      <td>500</td>
      <td>12.2</td>
      <td>13</td>
      <td>15.0</td>
    </tr>
    <tr>
      <td>1000</td>
      <td>6.1</td>
      <td>6.5</td>
      <td>7.6</td>
    </tr>
    <tr>
      <td>Standby</td>
      <td>-</td>
      <td colspan="3">2</td>
    </tr>
  </tbody>
  </table>
</div>

1. * 电源：1.8V对PVDD供电，3.3V对3V3_ANA + 3V3_BRF供电。
2. * 以上电源电压3.8V的功耗是依据1.8V及3.3V两路供电的测试数据按照效率计算的结果（计算公式：I3.8v = I1.8v * 1.8 / 90% / 3.8 + I3.3v）。