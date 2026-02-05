# 测量结果汇总

表格中 ADV 与 Connection 的电流值为该模式的增量电流，standby 为睡眠电流，实际的平均电流等于增量电流与睡眠电流之和
## 测试结果表 - 1.8V原始数据

<div class="table-wrapper docutils container">
<table class="docutils align-default">
  <thead>
    <tr>
      <th class="head">模式</th>
      <th class="head">间隔 (ms)</th>
      <th class="head">电源电压：1.8V   TXpower 0dBm (uA)</th>
      <th class="head">电源电压：1.8V   TXpower 4dBm (uA)</th>
      <th class="head">电源电压：1.8V   TXpower 10dBm (uA)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="5">ADV</td>
      <td>50</td>
      <td>262.44</td>
      <td>337.95</td>
      <td>396.34</td>
    </tr>
    <tr>
      <td>100</td>
      <td>118.36</td>
      <td>157.38</td>
      <td>191.70</td>
    </tr>
    <tr>
      <td>200</td>
      <td>53.56</td>
      <td>79.94</td>
      <td>94.01</td>
    </tr>
    <tr>
      <td>500</td>
      <td>20.58</td>
      <td>28.49</td>
      <td>36.49</td>
    </tr>
    <tr>
      <td>1000</td>
      <td>11.01</td>
      <td>13.93</td>
      <td>18.18</td>
    </tr>
    <tr>
      <td rowspan="5">Connection</td>
      <td>50</td>
      <td>163.64</td>
      <td>169.33</td>
      <td>184.30</td>
    </tr>
    <tr>
      <td>100</td>
      <td>62.50</td>
      <td>64.15</td>
      <td>70.62</td>
    </tr>
    <tr>
      <td>200</td>
      <td>24.94</td>
      <td>26.39</td>
      <td>30.09</td>
    </tr>
    <tr>
      <td>500</td>
      <td>10.40</td>
      <td>11.21</td>
      <td>12.29</td>
    </tr>
    <tr>
      <td>1000</td>
      <td>6.42</td>
      <td>6.50</td>
      <td>6.83</td>
    </tr>
    <tr>
      <td>Standby</td>
      <td>-</td>
      <td colspan="3">0</td>
    </tr>
  </tbody>
  </table>
</div>

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
      <td>138.1</td>
      <td>177.9</td>
      <td>208.6</td>
    </tr>
    <tr>
      <td>100</td>
      <td>62.3</td>
      <td>82.8</td>
      <td>100.9</td>
    </tr>
    <tr>
      <td>200</td>
      <td>28.2</td>
      <td>42.1</td>
      <td>49.5</td>
    </tr>
    <tr>
      <td>500</td>
      <td>10.8</td>
      <td>15</td>
      <td>19.2</td>
    </tr>
    <tr>
      <td>1000</td>
      <td>5.8</td>
      <td>7.3</td>
      <td>9.6</td>
    </tr>
    <tr>
      <td rowspan="5">Connection</td>
      <td>50</td>
      <td>86.1</td>
      <td>89.1</td>
      <td>97</td>
    </tr>
    <tr>
      <td>100</td>
      <td>32.9</td>
      <td>33.8</td>
      <td>37.2</td>
    </tr>
    <tr>
      <td>200</td>
      <td>13.1</td>
      <td>13.9</td>
      <td>15.8</td>
    </tr>
    <tr>
      <td>500</td>
      <td>5.5</td>
      <td>5.9</td>
      <td>6.5</td>
    </tr>
    <tr>
      <td>1000</td>
      <td>3.4</td>
      <td>3.4</td>
      <td>3.6</td>
    </tr>
    <tr>
      <td>Standby</td>
      <td>-</td>
      <td colspan="3">0</td>
    </tr>
  </tbody>
  </table>
</div>

1. * 电源：PVDD+AVDD33_ANA。
2. * 以上电源电压3.8V的功耗是依据1.8V及3.3V两路供电的测试数据按照效率计算的结果（计算公式：I3.8v = I1.8v * 1.8 / 90% / 3.8 + I3.3v）。