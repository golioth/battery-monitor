# Copyright (c) 2023 Golioth, Inc.
# SPDX-License-Identifier: Apache-2.0

if (CONFIG_ALUDEL_BATTERY_MONITOR)
  zephyr_library()
  zephyr_include_directories(include)
  zephyr_library_sources(battery.c)
  zephyr_library_sources_ifdef(CONFIG_ALUDEL_BATTERY_MONITOR_VOLTAGE_DIVIDER bat_voltage_divider.c)
  zephyr_library_sources_ifdef(CONFIG_ALUDEL_BATTERY_MONITOR_MAX17262 bat_max17262.c)
endif (CONFIG_ALUDEL_BATTERY_MONITOR)
