# Spot Welder Pico
Made for a Raspberry PI Pico W hooked up to a relay that switches a step down microwave transformer for spot welding new cells to my thinkpad t420 battery.

## Usage
```conosle
$ mkdir build && cd build
$ cmake -DCMAKE_EXPORT_COMPILE_COMMANDS=1 -DPICO_SDK_PATH=<path-to-pico-sdk> -DPICO_BOARD=<target_board>
```