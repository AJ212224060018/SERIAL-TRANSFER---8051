# SERIAL-TRANSFER-OF-SINGLE-BYTE-CHARACTER-USING-8051-KEIL.-EMBEDDED-C-PROGRAM-

**AIM:** 

To write and execute Embedded C Program for Serial Transfer of Single Byte / Character using 8051 KEIL.

**APPARATUS REQUIRED:**

Personal computer with Keil software

**PROGRAM:**

**(i)	Serial port transfer a character A**

#include<reg51.h> void main(void)

{

TMOD=0X20;//TIMER 1,MODE 2 TH1=0XFA;

SCON=0X50; TR1=1;

while(1)

{ SBUF='A';

while(TI==0); TI=0;

}

}

**(ii)	Serial port to Transfer a Message**

#include<reg51.h> void main(void)

{

unsigned char msg[]="Programming 8051"; unsigned char i;

TMOD=0X20;//TIMER 1,MODE 2 TH1=0XFA;

SCON=0X50; TR1=1;

for (i=0; i<17;i++)

{

SBUF= msg[i]; while(TI==0); TI=0;

}

while(1);

}

 
**OUTPUT:**

<img width="1920" height="358" alt="Screenshot 2025-10-27 105520" src="https://github.com/user-attachments/assets/56d2400f-f9ca-4321-afb7-52b53ab6a9f2" />

<img width="1920" height="343" alt="Screenshot 2025-10-27 105155" src="https://github.com/user-attachments/assets/44260dc9-a819-4f35-bf0e-ba8e2a2b7b10" />

**Result:**

Thus the Serial transfer of Single Byte / Character using 8051 KEIL was done and shown the output.
