# Loklight-hardware
A light for model railways (H0) that can be DCC controlled as digital drop-in replacement for MS4 &amp; E5.5 lightbulbs

When upgrading older locomotives from analog to digital DCC operation through a decoder, the onboard glowbulbs must be rewired for proper DCC operation. 
Particularly in the case of steam engine models, this requires adding wires from the tender to the front of the locomotives. 
This prevents the model from being used in the normal way where tender and loc can be seperated by the coupling mechanism. Also, the wires could be visible from outside.

The Loklight project undertakes to provide the hardware and software for a DCC controlled LED PCB that can be used as a drop-in replacement for glowbulbs in the commonly used sizes.

By removing the LEDs, the Loklight PCB can also be used for custom loads. In this case the load will be connected to VCC and an open-collector BJT connected to 0V. 
The designed is hardware limited to currents up to 15mA. There are two LEDs, and therefore two loads of up to 15mA are possible.

Steps to use the project:

1. Acquire the hardware. 
Either contact me or have the design produced at a vendor of your choosing. The design only uses JCPCB / LCSC indexed components.

2. Flash the firmware. 
Please refer to this project to obtain the firmware. Use either an ST-link or Segger JLink and Tag-Connect TC2030-IDC-NL adapter to flash the firmware.
Use the available connections to provide power to the PCB, either through the DCC inputs or the VCC, GND contacts.

3. Test. 
Before performing the next steps, connect your model railway controller track outputs to the Loklight DCC inputs. Verify that light functionality works as expected.
Flash the required CV settings (refer to software project) and verify function keys, speed and lok addressing yield the expected results.

4. Modify the hardware. 
First, use jumper bars or solid core copper wire (dia 0.5mm) and solder it onto the DCC inputs. One tip must be at the far end of the PCB, the other at the side.
Optimize the wire location and length either for MS4 retention or E5.5 thread-engagement in the socket. 
Optionally remove the LEDs and at custom outputs, using the LED pads for wire connection to the PCB.
Optionally test the hardware again. Remove the programming connection by using a Dremel or similar tool to sever the breakout section. Be careful to remove the via breakouts (almost) completely without damaging the internal PCB traces.
Finally, protect components if required from short circuiting against metal parts. For E5.5 sockets, the components should clear the socket, but a small wrapper will guarantee this.
 
5. Assemble the hardware.
Put the Loklight in the target locomotive. 

6. Configure and test.
Set the CVs are required (loc address, min and max brightness, etc) and test proper function.

7. Let me know.
I'd love to know if you have used this project!

This work has been made available to you for non-commercial (i.e. hobby) purposes only, under the Polyform license. Please reach out to me to discuss potential commercial use.
