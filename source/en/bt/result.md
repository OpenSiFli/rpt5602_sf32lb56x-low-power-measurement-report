# Measurement Results Summary

The Scan and Sniff currents in the table are incremental currents. The average current must include the Standby base current; see the calculation example in the notes.

## BT Power Consumption
### BT Sniff Mode Results

<div class="table-wrapper docutils container">
<table class="docutils align-default">
    <thead>
        <tr>
            <th class="head">Mode</th>
            <th class="head">Period (s)</th>
            <th class="head">Supply 3.8V, TX power 0 dBm (uA)</th>
            <th class="head">Supply 3.8V, TX power 4 dBm (uA)</th>
            <th class="head">Supply 3.8V, TX power 10 dBm (uA)</th>
            <th class="head">Unit</th>
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

### Scan Results

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
            <td>Inquiry enabled, Page disabled</td>
            <td>14.9</td>
            <td rowspan="3">uA</td>
        </tr>
        <tr>
            <td>Page enabled, Inquiry disabled</td>
            <td>29.7</td>
        </tr>
        <tr>
            <td>Both scans enabled</td>
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

1. Inquiry Scan receives for 16.87 ms every 2.56 s, Page Scan receives for 16.87 ms every 1.28 s.
1. * Power: PVDD is supplied by 1.8 V; 3V3_ANA and 3V3_BRF are supplied by 3.3 V.
2. * The above 3.8 V power consumption values are calculated from the measured 1.8 V and 3.3 V supply data using efficiency. (Calculation formula: I_3.8V = I_1.8V * 1.8 / 90% / 3.8 + I_3.3V)
4. * Calculation example:
Standby mode bt 500 ms sniff @ TX power 10 dBm: = 23.1 + 0 = 23.1 uA