<!-- Copyright (c) 2025 Golioth, Inc. -->
<!-- SPDX-License-Identifier: Apache-2.0 -->

# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [v1.1.0] - 2025-06-06

### Breaking Changes

- `get_batt_lvl_str()` renamed to `get_batt_pct_str()`

### Changed

- Rename `lvl` to `pct`. This is a more intuitive way to indicated
  reference refer to percentage.

## [v1.0.0] - 2025-03-12

### Added

- Battery monitor code moved from [Reference Design Template at
  1387aab](https://github.com/golioth/reference-design-template/tree/1387aab5e5ebec0d250938f2822e476db8b7c05b/src/battery_monitor)
