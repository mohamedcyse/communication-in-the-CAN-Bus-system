#Implementation of the communication in the CAN bus system.



#CAN-Bus:
-Development was mainly driven by the cooperation of Bosch and Intel.
-Bus systems were used in cars since 1990.



#This project demonstrate how to use the integrated CAN controller of the demonstration boards.
-Several tasks for the receiving and sending CAN messages have to be done.



#First part:
-Timer function is prepared, IRQ number can be found in "Interrupt_vector_table.pdf".



#Second part:
-This part concerns with the preparation of controller pins and message buffers.
-"buffer.pdf" used to configure sending buffers.
-Messages buffers are configured in "can.c".
-Interrupt flags for message buffers are cleared.
-CAN message is sent every 200ms, speed value is between 0 and 300 km/h and the speed value
should not exceed 300 km/h.
-Message ID is the last number of the IP address of the computer.
-"Virtual Cockpit" is a software that was used to verify the results.



#Third part:
-For reception a FIFO buffer is configured ,Every successful message reception causes an 
interrupt.
-When a button is pressed, the program connects to the 'TinyCAN' and sends a message.



 
