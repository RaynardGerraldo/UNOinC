default:
	avr-gcc -Os -DF_CPU=160000000UL -mmcu=atmega328p -c -o led1.o led1.c
	avr-gcc -o led1.bin led1.o
	avr-objcopy -O ihex -R .eeprom led1.bin led1.hex
	sudo avrdude -F -V -c arduino -p ATMEGA328P -P /dev/ttyUSB0 -b 115200 -U flash:w:led1.hex
