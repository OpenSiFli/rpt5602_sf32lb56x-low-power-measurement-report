# Summary of Measurements

The ADV and Connection current values in the tables are incremental currents for the respective modes. Standby is the sleep current. The actual average current equals the sum of incremental current and sleep current.
## Results Table - 1.8V Raw Data

<div class="table-wrapper docutils container">
<table class="docutils align-default">
  <thead>
    <tr>
      <th class="head">Mode</th>
      <th class="head">Interval (ms)</th>
      <th class="head">Supply 1.8V   TX Power 0 dBm (uA)</th>
      <th class="head">Supply 1.8V   TX Power 4 dBm (uA)</th>
      <th class="head">Supply 1.8V   TX Power 10 dBm (uA)</th>
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

## Results Table - 3.8V Converted Data

<div class="table-wrapper docutils container">
<table class="docutils align-default">
  <thead>
    <tr>
      <th class="head">Mode</th>
      <th class="head">Interval (ms)</th>
      <th class="head">Supply 3.8V   TX Power 0 dBm (uA)</th>
      <th class="head">Supply 3.8V   TX Power 4 dBm (uA)</th>
      <th class="head">Supply 3.8V   TX Power 10 dBm (uA)</th>
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

1. Power: PVDD + AVDD33_ANA.
2. The 3.8V power consumption above is calculated from the 1.8V and 3.3V supply test data based on efficiency (formula: I3.8V = I1.8V × 1.8 / 90% / 3.8 + I3.3V).