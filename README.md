PCB to support 2 USB-C PD charging ports operating on 9-36V input voltage and supporting up to 100W charging profiles.

The idea of this PCB was to work on boats and cars and support up to 100W usb-c pd output.
The PCB is build around the TPS65988 from Texas Instruments. 
At the time of creating the schematic, this was the only IC capable of 100W output profiles at low input voltages.

Due to chip shortages, the DPO2036 has been chosen as an overvoltage protection ic. The supported frequency is not enough for full USB-2 support, but should be enough for USB-PD and USB QC.
A cheaper receptacle could be used if USB QC is not needed.
The main challenge will be heat dissipation when operating at 100W.
The Buck-Boost controller will run hot.
To avoid high cost of 2oz copper layers for one-offs an alternative cooling solution needs to be consiered.

### TODO:
- Route PCB
- Feedback Control Loop of the Buck-Boost controller. Key challenge is to keep it stable on entire output range. The chosen inductor seems to be a good choice. Control loop might have to be done experimentally.
- Thermal design
