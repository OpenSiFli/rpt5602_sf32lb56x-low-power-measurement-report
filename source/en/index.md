# SF32LB56x Low-Power Test Report

Welcome to the low-power test report for the SF32LB56x series chips!


::::{grid} 1 2 2 3
:gutter: 3

:::{grid-item-card}  Chip Overview
:link: brief_introduction
:link-type: doc

Introduction to the chip
:::

:::{grid-item-card}  Test Environment
:link: test_environment/index
:link-type: doc

Hardware setup, software configuration, and tools required for testing
:::

:::{grid-item-card}  BLE Low-Power Tests
:link: ble/index
:link-type: doc

Detailed methods and results for BLE low-power scenarios
:::

:::{grid-item-card}  BT Classic Bluetooth Tests
:link: bt/index
:link-type: doc

Power consumption data for classic Bluetooth scenarios
:::

:::{grid-item-card}  CoreMark Performance Tests
:link: coremark/index
:link-type: doc

Power behavior analysis in benchmark performance tests
:::

::::


````{if-builder} html
```{toctree}
:maxdepth: 3
:hidden:

brief_introduction
test_environment/index
ble/index
bt/index
coremark/index
```
````

````{if-builder} simplepdf
```{toctree}
:maxdepth: 3
:hidden:
:numbered:

brief_introduction
test_environment/index
ble/index
bt/index
coremark/index
```
````
