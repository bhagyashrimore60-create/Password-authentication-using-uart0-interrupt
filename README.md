# Password-authentication-using-uart0-interrupt
  Interfacing: LPC2129 UART0 (TXD0=P0.0, RXD0=P0.1) via MAX232/USB-UART to PC terminal. 3 LEDs (correct/incorrect/lockout) on GPIO pins with resistors.  Program: UART0 ISR reads each byte into rx_buffer; on Enter, strcmp checks password. Match lights correct LED; 3 fails trigger lockout with 100ms LED blink. main() stays idle—all logic runs in ISR.
