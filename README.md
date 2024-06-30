This program is written in cpulator. choose "ARMv7" in Architecture and "ARMv7 DE1-SoC" in System. Here is a direct link to the website https://cpulator.01xz.net/?sys=arm-de1soc instead of taking theses steps.
This program useses some I/O devices. part of the program uses polling and part of it uses interrupts from some I/O device.

I/O stands for Input/Output and can be all sorts of devices connected to a processor (CPU). By I/O is often meant some physical "thing" that allows a user to communicate with the computer system, a kind of user interface.
  Here one can think of a keyboard, mouse and computer screen for a PC, or push buttons, display and LEDs for an "apparatus" with a built-in computer (e.g. a printer or a heat pump).
  Other examples of I/O devices can be various sensors (temperature, humidity, distance, etc.) or controllers to turn on/off or regulate things. It can also be timers or network cards.
  These do not have direct communication with the user, but are needed for the computer system to be able to detect and communicate with "its surroundings".

What is polling and interupts:
- Polling here means that the program constantly reads all alarm sensors (Input units), in turn in an infinite loop.
    If any sensor detects an alarm, the program handles it immediately when that sensor has been read, before the next sensor is read. Everything happens in order.

- Interruption means that the I/O units (only the Input units in this case) themselves signal to the processor that something has occurred,
    for example that a door alarm has been detected. This signaling is called an interrupt and is handled by a special interrupt routine for that particular event.
    Here, nothing happens in turn order as with polling, instead each event is handled separately exactly when it occurs. It is also possible to give different priorities to different events.
    Interrupt means that the I/O unit is connected to a special hardware input on the processor and sends a signal when some event occurs,
    whereby the processor "automatically" interrupts ongoing program execution and jumps to the corresponding interrupt routine.
  


How to use:

- The user can press "U" usung keyboard to increase the number by 1 and "D" to decrease the number by 1. "U" and "D" should be used pressed in "JTAG UART" input device in this case. Here we use polling.

- The user can press on "0" in (Push buttons devise) to count up and "1" in (Push buttons devise) to count down. Here we use interupts. 
