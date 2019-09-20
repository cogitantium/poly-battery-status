# poly-battery-status
Generates a pretty status-bar string for multi-battery systems on Linux. 
Written in Rust and should<sup>TM</sup> work with _n_ batteries. 

Personally used with i3blocks under i3.

## Features
- Uses sysfs for gathering batteries and values on these
- Calculates time-to-depleted and time-to-full from current power-draw
- Omits time-to-* when passive (specifically when sysfs delivers a status of `Unknown`)

## Usage
For developing and experimenting use Cargo:
```
repo/~ cargo run
```

For building also use Cargo:
```
repo/~ cargo build --release
```
Find the built executable under `repo/target/release/poly-battery-status`
Alternatively, see the [releases](https://github.com/cogitantium/poly-battery-status/releases) page for pre-compiled executables. 