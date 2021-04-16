# KiCAD files of a SDR ram addon for ECP5 evaluation board

KiCAD files of a simple RAM addon for Lattice LEF5UM5G-85G

![print board](https://github.com/kazkojima/ecp5evn-sdram-addon/blob/main/images/sdram-addon-board.png)


![LEF5UM5G-85G+addon](https://github.com/kazkojima/ecp5evn-sdram-addon/blob/main/images/sdram-addon.png)

## LiteX/[litex-boards](https://github.com/litex-hub/litex-boards.git) platform hunk of the addon

```
    # SDR SDRAM on connector J39 and J40
    ("sdram_clock", 0, Pins("K5"), IOStandard("LVCMOS33")),
    ("sdram", 0,
        Subsignal("a",     Pins(
            "B10 E7  A11 A19 K4  D14 P1  C14",
            "L1  L2  A9  N2  L3")),
        Subsignal("dq",    Pins(
            "D15 B15 C15 B13 B20 D11 E11 B12",
            "N4  M4  L4  J3  J4  H2  A15 K2")),
        Subsignal("we_n",  Pins("D12")),
        Subsignal("ras_n", Pins("C13")),
        Subsignal("cas_n", Pins("E12")),
        Subsignal("cs_n",  Pins("D13")),
        Subsignal("cke",   Pins("M5")),
        Subsignal("ba",    Pins("E13 A14")),
        Subsignal("dm",    Pins("C12 N3")),
        IOStandard("LVCMOS33"),
        Misc("SLEWRATE=FAST"),
    ),
```
