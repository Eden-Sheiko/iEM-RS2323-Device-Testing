# iEM-RS2323 Device Testing

This is a simple C program to test communication with the iEM-RS2323 device using RS232 serial communication protocol. The program writes a string of characters to the serial port "/dev/ttyUSB0" at a baud rate of 9600, 8 data bits, no parity, and 1 stop bit.
Requirements

   * C compiler
   * iEM-RS2323 device connected to the computer via USB-to-serial cable

## Usage

 Connect the iEM-RS2323 device to the computer using a USB-to-serial cable.
 Compile the program using a C compiler.
 Run the program.
 Check the iEM-RS2323 device for the received data.

## Code Explanation

The program opens the serial port "/dev/ttyUSB0" using the open() function with O_RDWR and O_NOCTTY flags. The struct termios structure is used to configure the serial port. The program sets the baud rate to 9600, 8 data bits, no parity, and 1 stop bit using the cfsetospeed(), cfsetispeed(), and c_cflag fields of the struct termios. The program then writes the string "Hello, RS232!" to the serial port using the write() function. The program continues to write the same string to the serial port every 1 second until the program is terminated.
## Note

Make sure that the iEM-RS2323 device is properly connected to the computer and that the device's settings match those specified in the program. If the program fails to communicate with the device, check the device's documentation for the correct settings.
