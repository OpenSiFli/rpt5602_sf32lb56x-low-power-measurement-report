# Summary of Measurements

## Processor Power
Tests were performed under 3.3V and 1.8V supply conditions, and the results are consolidated below.
### CoreMark Results

<div class="table-wrapper docutils container">
<table class="docutils align-default">
  <thead>
    <tr>
      <th class="head">CPU</th>
      <th class="head">Frequency</th>
      <th class="head">Supply 3.3V Current (uA)</th>
      <th class="head">Increment (uA/MHz)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="2">HCPU</td>
      <td>240MHz</td>
      <td>9550</td>
      <td rowspan="2">30.62</td>
    </tr>
    <tr>
      <td>192MHz</td>
      <td>8080</td>
    </tr>
    <tr>
      <td rowspan="2">LCPU</td>
      <td>48MHz</td>
      <td>936</td>
      <td rowspan="2">17.41</td>
    </tr>
    <tr>
      <td>12MHz</td>
      <td>518</td>
    </tr>
  </tbody>
  </table>
</div>

<div class="table-wrapper docutils container">
<table class="docutils align-default">
  <thead>
    <tr>
      <th class="head">CPU</th>
      <th class="head">Frequency</th>
      <th class="head">Supply 1.8V Current (uA)</th>
      <th class="head">Increment (uA/MHz)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="2">HCPU</td>
      <td>240MHz</td>
      <td>16740</td>
      <td rowspan="2">56.04</td>
    </tr>
    <tr>
      <td>192MHz</td>
      <td>14050</td>
    </tr>
    <tr>
      <td rowspan="2">LCPU</td>
      <td>48MHz</td>
      <td>1540</td>
      <td rowspan="2">26.2</td>
    </tr>
    <tr>
      <td>12MHz</td>
      <td>911</td>
    </tr>
  </tbody>
  </table>
</div>

### WhileLoop Results

<div class="table-wrapper docutils container">
<table class="docutils align-default">
  <thead>
    <tr>
      <th class="head">CPU</th>
      <th class="head">Frequency</th>
      <th class="head">Supply 3.3V Current (uA)</th>
      <th class="head">Increment (uA/MHz)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="2">HCPU</td>
      <td>240MHz</td>
      <td>7910</td>
      <td rowspan="2">23.75</td>
    </tr>
    <tr>
      <td>192MHz</td>
      <td>6770</td>
    </tr>
    <tr>
      <td rowspan="2">LCPU</td>
      <td>48MHz</td>
      <td>721</td>
      <td rowspan="2">13.54</td>
    </tr>
    <tr>
      <td>12MHz</td>
      <td>396</td>
    </tr>
  </tbody>
  </table>
</div>

<div class="table-wrapper docutils container">
<table class="docutils align-default">
  <thead>
    <tr>
      <th class="head">CPU</th>
      <th class="head">Frequency</th>
      <th class="head">Supply 1.8V Current (uA)</th>
      <th class="head">Increment (uA/MHz)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="2">HCPU</td>
      <td>240MHz</td>
      <td>13740</td>
      <td rowspan="2">42.91</td>
    </tr>
    <tr>
      <td>192MHz</td>
      <td>11680</td>
    </tr>
    <tr>
      <td rowspan="2">LCPU</td>
      <td>48MHz</td>
      <td>1140</td>
      <td rowspan="2">17.62</td>
    </tr>
    <tr>
      <td>12MHz</td>
      <td>717</td>
    </tr>
  </tbody>
  </table>
</div>

### Shutdown Power

```{eval-rst}
.. list-table::
   :header-rows: 1
   :widths: 40 20

   * - Test Item
     - Supply 1.8V Current (uA)
   * - Wake-up pin (send shutdown)
     - 0.30
   * - RTC wake-up (send shutdown 5)
     - 0.31
```

