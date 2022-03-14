Here is the first pass of or [gpio pin mapping](https://user-images.githubusercontent.com/8724975/158108831-fbf8fa47-cd49-4bae-8a7a-24a997bb3a8b.png).

This comes from mcu.kicad_sch, but is broken out for discussion and to be of more immediate use to 
those not versed in Kicad.

As of March 14, Robert is uncomfortable with Pin 16. (Robert's a software guy, so his uneasiness is 
trumped by other boards successfully using Pint 16.) Section 3.2.5 on page 25 describes the versaitle 
pin muxing available on the BL60x parts. It shows that we can populate the five bit mode enum to bring 
it into UART mode.  UNfortunately, the pins default to UART mode SIG1, which maps to UART0_CTS when 
a SIG6 would give us a compliment to our UART1_RX currently on GPIO 7.

Trying to harvest from current code is frustrating.

~/src/bl_mcu_sdk/drivers/bl602_driver/regs/glb_reg.h 
creates a perfectly lovely bitmapped union, which the code signores and splats over its own 
incomprehensible macros and bit-banging.  uart-swap_set is never used. The bits are actually 
set in GLB_UART_Sig_Swap_Set() inside drivers/bl602_driver/std_drv/src/bl602_glb.c

So we're currently researching this. Help welcome.

![image](https://user-images.githubusercontent.com/97197236/158119342-f2fa74e5-93d4-4910-bfef-eec654abc3fc.png)



