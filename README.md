# antha-releases

Home of binary distribution of antha tools.

  - clientdevice (aka Antha Connect): A program that should be run on each
    computer with lab devices attached to it. It connects those devices to
    AnthaOS and allows the devices to be run by Antha.

## Clientdevice

### Installation

0. Depending on the devices you want to connect you may have to also install
   more software in addition to clientdevice. See [supplemental software](#supplemental-software)
   for details based on your desired device(s).

1. Download the latest version of clientdevice from the [releases tab](https://github.com/Synthace/antha-releases/releases).

2. Unpack the file on a computer attached to your lab devices.

3. Run the following command in a terminal in the directory you unpacked
   clientdevice in and for each device attached to the computer:
   ```sh
   clientdevice --endpoint https://my-co.antha.com add --device pipetmax
   clientdevice --endpoint https://my-co.antha.com add --device bioshake
   ```
   Make sure to replace `https://my-co.antha.com` with the appropriate URL.

   To see a list of device types available run:
   ```sh
   clientdevice add --help
   ```

### Running

1. Run the following command in a terminal in the directory you unpacked
   clientdevice:

   ```sh
   clientdevice --endpoint https://my-co.antha.com connect
   ```

## Supplemental Software

### Gilson PIPETMAX

A modified version of Trilution is required for Antha to communicate with a
Gilson PIPETMAX. Please contact Synthace for details.

### QInstruments BioShake

The Prolific USB to Serial driver is required for Antha to communicate with a
QInstruments BioShake ([Windows
drivers](http://www.prolific.com.tw/US/ShowProduct.aspx?p_id=225&pcid=41), [OSX
drivers](http://www.prolific.com.tw/US/ShowProduct.aspx?p_id=229&pcid=41)).

## Changelog

  - v0.5.3
    * Name is required when adding a new device (clientdevice add --name ...)
  - v0.5.2
    * Changed default endpoint
  - v0.5.1
    * Update QInstruments BioShake driver to include diagnostic program
  - v0.5
    * Initial release
