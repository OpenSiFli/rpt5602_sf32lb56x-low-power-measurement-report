# 测量结果汇总

表中的 Scan和Snif电流为增量电流，平均电流需加上 Standby的底电流，计算方法参照备注中的计算示例。

## BT 功耗
### BT Sniff Mode 测试结果

<div class="table-wrapper docutils container">
<table class="docutils align-default">
	<thead>
		<tr>
			<th class="head">模式</th>
			<th class="head">时间周期 (s)</th>
			<th class="head">电源电压：3.8V  TXpower 0 dBm (uA)</th>
			<th class="head">电源电压：3.8V  TXpower 4 dBm (uA)</th>
			<th class="head">电源电压：3.8V  TXpower 10 dBm (uA)</th>
			<th class="head">单位</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td rowspan="5">BT Sniff Mode</td>
			<td>50</td>
			<td>214.9</td>
			<td>222.8</td>
			<td>253.6</td>
			<td rowspan="5">uA</td>
		</tr>
		<tr>
			<td>100</td>
			<td>107</td>
			<td>111.4</td>
			<td>211.6</td>
		</tr>
		<tr>
			<td>200</td>
			<td>53.4</td>
			<td>55.7</td>
			<td>63</td>
		</tr>
		<tr>
			<td>500</td>
			<td>21.3</td>
			<td>22.3</td>
			<td>25.1</td>
		</tr>
		<tr>
			<td>1000</td>
			<td>10.7</td>
			<td>11.1</td>
			<td>12.6</td>
		</tr>
		<tr>
			<td>Standby</td>
			<td>-</td>
			<td colspan="3">2</td>
			<td>uA</td>
		</tr>
	</tbody>
	</table>
</div>

### Scan 测试结果

<div class="table-wrapper docutils container">
<table class="docutils align-default">
	<thead>
		<tr>
			<th class="head">场景</th>
			<th class="head">电源电压 3.8V 电流 (uA)</th>
			<th class="head">单位</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>Inquiry enable, Page disable</td>
			<td>14.9</td>
			<td rowspan="3">uA</td>
		</tr>
		<tr>
			<td>Page enable, Inquiry disable</td>
			<td>29.7</td>
		</tr>
		<tr>
			<td>Both scans enable</td>
			<td>45.6</td>
		</tr>
		<tr>
			<td>Standby</td>
			<td>2</td>
			<td>uA</td>
		</tr>
	</tbody>
	</table>
</div>

1. Inquiry Scan 每 2.56s 接收 16.87ms，Page Scan 每 1.28s 接收 16.87ms。
1. * 电源：1.8V对PVDD供电，3.3V对3V3_ANA + 3V3_BRF供电。
2. * 以上电源电压3.8V的功耗是依据1.8V及3.3V两路供电的测试数据按照效率计算的结果（计算公式：I3.8v = I1.8v * 1.8 / 90% / 3.8 + I3.3v）。
4. * 计算示例：
Standby mode bt 500ms sniff @TXpower10dBm: =23.1+0=23.1uA