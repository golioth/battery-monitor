# Golioth Battery Monitor

A Zephyr module to read the battery voltage and calculate the remaining
percentage. Helper functions to log the values and stream to Golioth are
provided. This library depends on the [Golioth Firmware
SDK](https://github.com/golioth/golioth-firmware-sdk/).

The library will use the MAX17262 fuel gauge IC when one is detected in
the devicetree. Otherwise, it will use a voltage divider based on the
`vbatt` path found in devicetree.

## Add the module to your Zephyr project

Add this block to `west.yml` and run `west update`:

```
    - name: Golioth Battery Monitor
      path: deps/modules/lib/battery-monitor
      revision: v1.0.0
      url: https://github.com/golioth/battery-monitor
```

## Enable the library

1. Ensure your board has either a [MAX17262 compatible
   node](https://docs.zephyrproject.org/latest/build/dts/api/bindings/sensor/maxim%2Cmax17262.html)
   or a `vbatt` path to a voltage divider in the devicetree.
2. Enable the library by setting the Kconfig symbol:

    ```
    CONFIG_ALUDEL_BATTERY_MONITOR=y
    ```
