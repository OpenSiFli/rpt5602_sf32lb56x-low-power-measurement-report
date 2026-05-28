# Measurement Results Summary

The ADV and Connection currents shown in the table are the incremental currents for each mode. `Standby` is the sleep current. The actual average current equals the incremental current plus the standby current.


## Test Results Table - Converted to 3.8 V

<div class="table-wrapper docutils container">
<table class="docutils align-default">
  <thead>
    <tr>
      <th class="head">Mode</th>
      <th class="head">Interval (ms)</th>
      <th class="head">Supply 3.8V, TX power 0 dBm (uA)</th>
      <th class="head">Supply 3.8V, TX power 4 dBm (uA)</th>
      <th class="head">Supply 3.8V, TX power 10 dBm (uA)</th>
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

1. * Power: PVDD is supplied by 1.8 V; 3V3_ANA and 3V3_BRF are supplied by 3.3 V.
2. * The above 3.8 V power consumption values are calculated from the measured 1.8 V and 3.3 V supply data using efficiency. (Calculation formula: I_3.8V = I_1.8V * 1.8 / 90% / 3.8 + I_3.3V)