# antha-releases

Home of binary distribution of antha tools.

  - clientdevice (aka Antha Connect): A program that should be run on each
    computer with lab devices attached to it. It connects those devices to
    AnthaOS and allows the devices to be run by Antha.

## Clientdevice

### Installation

1. Download the latest version of clientdevice from the [releases tab](https://github.com/Synthace/antha-releases/releases).

2. Unpack the file on a computer attached to your lab devices.

3. Run the following command in a terminal in the directory you unpacked
   clientdevice in and for each device attached to the computer:
   ```sh
   clientdevice add --device pipetmax
   clientdevice add --device bioshake
   ```
   To see a list of devices available run:
   ```sh
   clientdevice add --help
   ```

### Running

1. Run the following command in a terminal in the directory you unpacked
   clientdevice:
   ```sh
   clientdevice connect
   ```

### Non-standard installations

By default, clientdevice pairs with https://antha.synthace.com . If you want
to connect to another AnthaOS deployment add the following options to both
the `add` and `connect` commands above: 
```sh
--endpoint https://my.different.endpoint --insecureSkipVerify
```
