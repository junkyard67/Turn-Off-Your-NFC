# Turn-Off-Your-NFC
I created this repository to experiment with the NFC Functionality and figure out if i can upload a file to a device unnoticed through NFC.
This idea comes from the basic human vunlerability that people tend to keep their NFC open on their Phones even when it's not needed.
If the NFC is open and readily available, then an attacker can just walk by you in public and being in close range he can make your Phone open a malicious link, infecting your device with potential malware.

# ! Important Note !

Please don't to this to random people, this can be considered malicious intent by some people and it might even be illegal, even tho it does not do anything bad to their device.
This repository scope is to mitigate and educate about this vulnerability.

**Always get the consent of the target you want to use this on.**

# Implementation idea
This project has in mind the Flipper Zero, but it can easily be emulated by any Phone or NFC emulation device.

This project will use the Suspicious_Malicious.txt file instead of an actual malicious file. This file will contain text regarding the vulnerability and a notice to the target that the NFC functionality should be turned off when not in use.
1) Create a NFC Tag Data which contain a link to access/download the Suspicious_Malicious.txt file.
2) Add a NFC Tag to the Flipper Zero so it can be emulated.
3) Write your Flipper Zero NFC Tag with the link mentioned in step 1.
4) Use your Flipper Zero to emulate the NFC Tag near user phone when it have the NFC enabled.

# Obstacles
- Just accessing the link to the Suspicious_Malicious.txt file will not download any file from the internet. The proof of concept is enough just by accessing the link.
However, to download the file you need to have some web server with a javascript which will do a GET request to github so the file can be donwloaded to the device.

- After step 4, the device will ask the user about which application to use to open the link. This is a blocking point for the attacker as the user might just chose to not open the link.
For some devices, they might have a default application set in place and it might just open the link without any notice to the user.

- When downloading the file, the user might be asked to choose the download location. This is a blocking point for the attacker as the user might just cancel the download.
For some devices, they might have a default option in place and the download will execute without any prompt to the user.

Can these be circumvented somehow? This is the real quiestion and the place to experiment with!

# Mitigation

To mitigate this vulenrability, several steps can be taken, listed in the order of importance and impact.
1) Turn off your NFC while it's not used. This is the best and easiest method.
2) Don't have a default application to open links, always manually choose an application for such cases.
3) Don't have a default save option for downloading files, always manually choose where to download a file from the internet.
4) Keep your Device in a place where it would be hard for an Attacker to get close enought to launch this attack.
