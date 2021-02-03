# Bluetooth Headset Profile Switcher

Allow to switch your Bluetooth Headset profile between AD2P (good sound quality but no mic) and headset (bad sound quality but working mic).

![](images/ad2p.png)

![](images/headset.png)

(Empty space when the bluetooth headset is not plugged)

# Dependencies

fonts-font-awesome, python3, [pulsectl](https://github.com/mk-fg/python-pulse-control) (I installed it via pip3).

# Installation

To use with i3blocks, use the following in `i3blocks.conf` file:

```INI
[bt_headset_mode]
command=$SCRIPT_DIR/bt_headset_mode
markup=pango
interval=10
bluetoothcard=<NameOfYourBluetoothCard>
```

<NameOfYourBluetoothCard> is the name of your bluetooth card that you can find using:

```bash
pactl list cards | grep bluez_card
```

You should get something like this:
```bash
Name: bluez_card.4C_87_5D_2B_62_1D
```

use the full name for the `bluetoothcard` variable.
