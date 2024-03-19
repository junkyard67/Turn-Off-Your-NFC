# Turn-Off-Your-NFC
I created this repository to experiment with the NFC Functionalty and figure out if i can upload a file to a device unnoticed through NFC.
This idea comes from the basic human vunlerability that people keep their NFC open on their Phones.
If the NFC is open and readily available, then an attacker can just go by you in public and being in close range he can make your Phone open a malicious link, infecting your device with potential malware.

# Implementation idea
This project has in mind the Flipper Zero, but it can easily be emulated by any Phone or NFC emulation device.

This project will use the Suspicious_Malicious.txt file instead of an actual malicious file. This file will contain text regarding the vulnerability and a notice to the target that the NFC functionality should be turned off when not in use.
1) Create a NFC Tag data which contain a link to download the Suspicious_Malicious.txt file.
2) Add a NFC Tag to the Flipper Zero so it can be emulated.
3) Write your Flipper Zero NFC Tag with the link mentioned in step 1.
4) Use your Flipper Zero to emulate the NFC Tag near user phone when it have the NFC enabled.

# Obstacles
After step 4, the device will ask the user about which application to use to open the link. This is a blocking point as the user might just chose to not open the link.
For some devices, they might have a default application set in place and it might just open the link without any notice.

Can this be circumvented somehow? This is the real quiestion and the place to experiment with!

# ! Important Note !

Please don't to this to random people, this can be considered malicious intent by some people and it might even be illegal, even tho it does not do anything bad to their device.
This repository scope is to mitigate and educate about this vulnerability.
Always get the consent of the target you want to use this on.
