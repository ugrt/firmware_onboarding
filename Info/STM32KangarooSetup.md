# Setup the STM32 for Kangaroo Communication
## Driveboard/STM32 Pins
Each line to the Kangaroo is labelled as ENCx on driveboard. So, ENCx can control one Kangaroo/two motors. 
ENCx-Aout = STM32 Tx (send to Kangaroo). ENCx-Bout = STM32 Rx (Receive from Kangaroo).

Here are which pins on the STM32F767 Nucleo are used for Kangaroo communication. ENCx represents the pins the Kangaroo connects to on the driverboard, so ENC1 controls Kangaroo1, ENC2 -> Kangaroo2, etc...
- ENC1
  - PE9 -> Tx
  - PE11 -> Rx
- ENC2
  - PA5 -> Tx
  - PB3 -> Rx
- ENC3
  - PA6 -> Tx
  - PA7 -> Rx
- ENC4
  - PD12 -> Tx
  - PD13 -> Rx
- ENC5
  - PA0 -> Tx
  - PA1 -> Rx
- ENC6
  - PC6 -> Tx
  - PC7 -> Rx

## Configure STM32 Pins
Here is a PDF showing the setup of the STM32 for communicating with one Kangaroo:
[View on Sharepoint](https://uoguelphca.sharepoint.com/:b:/r/sites/UGRT2/Rover/Firmware/Setup.pdf?csf=1&web=1&e=ITk84)
[Download from GitHub]()

