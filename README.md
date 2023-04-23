# ALScope

An FPGA based logic analyzer for Colorlight ECP5 boards.

This comes with no support.

## Install OSS-CAD and LiteX

Follow the instructions at:
https://github.com/YosysHQ/oss-cad-suite-build

## Build and boot the board

```shell
./main.py --ip-address=10.0.0.42 --build --flash
```

## Start the server
```shell
litex_server --udp --udp-ip=10.0.0.42
```

## Start the acquisition
```shell
litescope_cli -r 'user_btn_n0' --dump dump.sr
```

## Display in a terminal
```shell
sigrok-cli -i dump.sr -O ascii
```
## See a video

[![Demo](https://kraut.zone/lazy-static/previews/9eab62a9-1530-4d78-b685-2ea261f50b67.jpg)](https://kraut.zone/w/k2qy5PXbBuHhozcDf9QgbP)

## Sources and useful stuff

Started with [Colorlite](https://github.com/enjoy-digital/colorlite) as a base.

[Sigrok](https://sigrok.org) to display ascii waves

