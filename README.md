# Nanopi Core2 

This is a base Nerves System configuration for the [NanoPi Core2](http://www.orangepi.org/orangepizero/).

![Orange Pi Zero Black image](assets/images/Core2_02-900x630.jpg)
<br><sup>[Image credit](#nanopi)</sup>

* CPU: Allwinner H5, Quad-core 64-bit high-performance Cortex A53
* DDR3 RAM: 512MB/1GB
* Storage: 8GB/16GB/32GB eMMC
* Connectivity: 10/100/1000M Ethernet utilizing RTL8211E-VB-CG
* USB Host x 3(included in 2.54mm pitch pin header)
* MicroSD Slot x 1
* LED: x 2, one for power status and the other for system status
* GPIO1: 2.54mm pitch 12 x 2 pin header containing UART, SPI, I2C, GPIO and etc
* GPIO2: 2.54mm pitch 24 pin header containing SPI, IR, I2S, USB, serial debug port, audio and etc
* GPIO3: 2.54mm pitch 20 pin header containing USB, Gbps Ethernet, I2C and etc
* PCB Size: 40 x 40mm


## Preparing your Orange Pi Zero

The Orange Pi Zero does not have built in eMMC memory. Booting simply requires writing a Nerves firmware image to an SD card and inserting it.

## Console access

The console is configured to output to `ttyS0` by default. This is the
UART output accessible by the 4 pin header (labeled "Debug Serial Port" above). A 3.3V FTDI
cable is needed to access the output.

The Orange Pi Zero does not support HDMI output.

## Linux / Driver Support

### Device tree overlays

Both the SPI and I2C devices have been enabled in the default in-kernel DTS via a kernel patch. Supporting runtime configuration of I2C/SPI is less straightforward than RPi's which have many tools available for apply DTS fragments. If you need to enable or disable these ports, please feel free to submit a pull request with the appropriate tooling support. Future work may involve porting over the `configfs` patches from the Armbian project for this purpose.

### Supported USB WiFi devices

The kernel driver for the XRadio chip has _not_ been included due to instability issues. It is possible to port it to recent 4.x kernels, but the implementation quality is low. Until the driver improves or mainline linux driver is added, this repo isn't likely to support wifi.

## Installation

If [available in Hex](https://hex.pm/docs/publish), the package can be installed as:

  1. Add nerves_system_nanopi_core2 to your list of dependencies in `mix.exs`:

        def deps do
          [{:nerves_system_nanopi_core2, "~> 0.2.4"}]
        end

  2. Ensure nerves_system_nanopi_core2 is started before your application:

        def application do
          [applications: [:nerves_system_nanopi_core2]]
        end


[Image credit](#orangepi): This image is from the [Orange Pi Website](http://www.orangepi.org/).
