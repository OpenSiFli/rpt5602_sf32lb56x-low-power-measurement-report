# SF32LB56x Brief Introduction

## Architecture Overview

**SF32LB56x** is a big.little SoC based on the **Arm Cortex‑M33 STAR‑MC1** processor.

:::::{grid} 1 2 2 2
:gutter: 3

::::{grid-item-card} High-Performance Big Core
:class-header: bg-primary text-white

**Max Frequency**: 240 MHz
^^^
Designed for high-performance compute scenarios:
- Graphics processing
- Audio processing  
- Neural network computation
::::

::::{grid-item-card} Low-Power Little Core (LCPU)
:class-header: bg-success text-white

**Max Frequency**: 96 MHz
^^^
Optimized for low-power tasks:
- BLE protocol stack
- Sensor data acquisition
- Sensor algorithm computation
::::

:::::



## Test Overview

This document provides power measurement methods and reference results for SF32LB56x across multiple usage scenarios:

```{list-table} Test Scenarios Overview
:header-rows: 1
:widths: 20 30 50

* - Category
  - Test Scenario
  - Description
* - **Wireless Communication**
  - BLE (Low-Power Bluetooth)
  - Typical scenarios: advertising, connection, data transfer
* - **Wireless Communication**
  - BT (Bluetooth Classic)
  - Various operating modes of classic Bluetooth
* - **Performance Tests**
  - CoreMark benchmark
  - Power behavior in standardized CPU performance tests
* - **Basic Tests**
  - While Loop
  - Baseline power for simple loop operations
* - **Standby Mode**
  - Shutdown mode
  - Minimum-power state measurements
```

## Important Reminder

```{warning}
**Test results are for reference only**

Results depend on specific hardware and software environments; actual applications may differ.
```

### Key Factors Affecting Power

:::::{grid} 1 2 2 3
:gutter: 3

::::{grid-item-card} Chip Factors
- Chip-to-chip variations
- Process lot variations
::::

::::{grid-item-card} Hardware Factors
- Selection and quality of external components
- External inductor for on-chip buck
- PCB design and layout
::::

::::{grid-item-card} Test Environment
- Instrument accuracy and calibration
- Power supply stability and ripple
- Ambient temperature and humidity
::::

::::{grid-item-card} Software Configuration
- Firmware version and compiler options
- I/O pin configuration states
- Clock and power management settings
::::

::::{grid-item-card} Environmental Conditions
- Operating temperature range
- EMI levels
- Supply voltage variation
::::

:::::


