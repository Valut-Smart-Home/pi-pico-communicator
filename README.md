# PI PICO based communication board
Usb to many serial interfaces

## Board design
Board has many [75176B](https://www.ti.com/lit/ds/symlink/sn65176b.pdf?ts=1711953903418) interfaces:
- One connected directly to GP0, GP1 as hardware UART0 with GP2 as direction control
- One connected directly to GP4, GP5 as hardware UART1 with GP6 as direction control
- Four connected to GP8, GP9 as PIO driven UART 9200 8N1 with direction control by [MCP230008](https://ww1.microchip.com/downloads/en/DeviceDoc/MCP23008-MCP23S08-Data-Sheet-20001919F.pdf), DE and RE connected separatelly
Additionally there is one more RX only UART 9200 8N1 PIO driven interface on GP28

## USB Serial 0 - Control for PI PICO
Controls interface setup for UART0 and UART1. Switches actually active 75176B by MCP230008 setup.

## USB Serial 1 - Control for PI PICO
Connected directly with hardware UART0

## USB Serial 2 - Control for PI PICO
Connected directly with hardware UART1

## USB Serial 3 - Control for PI PICO
Connected with PIO driven TX/RX interface

## USB Serial 4 - Control for PI PICO
Connected to RX only PIO driven interface
