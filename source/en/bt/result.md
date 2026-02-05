# Summary of Measurements

The Scan and Sniff currents in the tables are incremental currents. The average current should include the Standby base current; see the notes for calculation examples.

## BT Power
### BT Sniff Mode Results

<div class="table-wrapper docutils container">
<table class="docutils align-default">
	<thead>
		<tr>
			<th class="head">Mode</th>
			<th class="head">Interval (s)</th>
			<th class="head">Supply 1.8V  TX Power 0 dBm (uA)</th>
			<th class="head">Supply 1.8V  TX Power 4 dBm (uA)</th>
			<th class="head">Supply 1.8V  TX Power 10 dBm (uA)</th>
			<th class="head">Unit</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td rowspan="5">BT Sniff Mode</td>
			<td>50</td>
			<td>218.43</td>
			<td>227.46</td>
			<td>375.65</td>
			<td rowspan="5">uA</td>
		</tr>
		<tr>
			<td>100</td>
			<td>109.87</td>
			<td>116.80</td>
			<td>204.37</td>
		</tr>
		<tr>
			<td>200</td>
			<td>53.58</td>
			<td>56.78</td>
			<td>106.89</td>
		</tr>
		<tr>
			<td>500</td>
			<td>22.84</td>
			<td>24.50</td>
			<td>43.97</td>
		</tr>
		<tr>
			<td>1000</td>
			<td>11.57</td>
			<td>12.07</td>
			<td>22.20</td>
		</tr>
		<tr>
			<td>Standby</td>
			<td>-</td>
			<td colspan="3">0</td>
			<td>uA</td>
		</tr>
	</tbody>
	</table>
</div>

<div class="table-wrapper docutils container">
<table class="docutils align-default">
	<thead>
		<tr>
			<th class="head">Mode</th>
			<th class="head">Interval (s)</th>
			<th class="head">Supply 3.8V  TX Power 0 dBm (uA)</th>
			<th class="head">Supply 3.8V  TX Power 4 dBm (uA)</th>
			<th class="head">Supply 3.8V  TX Power 10 dBm (uA)</th>
			<th class="head">Unit</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td rowspan="5">BT Sniff Mode</td>
			<td>50</td>
			<td>115</td>
			<td>119.7</td>
			<td>197.7</td>
			<td rowspan="5">uA</td>
		</tr>
		<tr>
			<td>100</td>
			<td>57.8</td>
			<td>61.5</td>
			<td>107.6</td>
		</tr>
		<tr>
			<td>200</td>
			<td>28.2</td>
			<td>29.9</td>
			<td>56.3</td>
		</tr>
		<tr>
			<td>500</td>
			<td>12</td>
			<td>12.9</td>
			<td>23.1</td>
		</tr>
		<tr>
			<td>1000</td>
			<td>6.1</td>
			<td>6.4</td>
			<td>11.7</td>
		</tr>
		<tr>
			<td>Standby</td>
			<td>-</td>
			<td colspan="3">0</td>
			<td>uA</td>
		</tr>
	</tbody>
	</table>
</div>

### Scan Results

<div class="table-wrapper docutils container">
<table class="docutils align-default">
	<thead>
		<tr>
			<th class="head">Scenario</th>
			<th class="head">Supply 1.8V Current (uA)</th>
			<th class="head">Unit</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>Inquiry enable, Page disable</td>
			<td>25.31</td>
			<td rowspan="3">uA</td>
		</tr>
		<tr>
			<td>Page enable, Inquiry disable</td>
			<td>49.35</td>
		</tr>
		<tr>
			<td>Both scans enable</td>
			<td>77.91</td>
		</tr>
		<tr>
			<td>Standby</td>
			<td>0</td>
			<td>uA</td>
		</tr>
	</tbody>
	</table>
</div>

<div class="table-wrapper docutils container">
<table class="docutils align-default">
	<thead>
		<tr>
			<th class="head">Scenario</th>
			<th class="head">Supply 3.8V Current (uA)</th>
			<th class="head">Unit</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>Inquiry enable, Page disable</td>
			<td>13</td>
			<td rowspan="3">uA</td>
		</tr>
		<tr>
			<td>Page enable, Inquiry disable</td>
			<td>26</td>
		</tr>
		<tr>
			<td>Both scans enable</td>
			<td>41</td>
		</tr>
		<tr>
			<td>Standby</td>
			<td>0</td>
			<td>uA</td>
		</tr>
	</tbody>
	</table>
</div>

1. Inquiry Scan receives 16.87 ms every 2.56 s; Page Scan receives 16.87 ms every 1.28 s.
1. Power: PVDD + AVDD33_ANA.
2. The 3.8V power consumption above is calculated from the 1.8V and 3.3V supply test data based on efficiency (formula: I3.8V = I1.8V × 1.8 / 90% / 3.8 + I3.3V).
4. Example calculation:
Standby mode BT 500 ms sniff @ TX Power 10 dBm: = 23.1 + 0 = 23.1 uA