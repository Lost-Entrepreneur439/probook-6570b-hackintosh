macOS Catalina EFI for the HP ProBook 6570b using OpenCore. I will try to keep this EFI up to date with the latest OpenCore and kexts

<img width="1366" height="768" alt="dhp21q" src="https://github.com/user-attachments/assets/5994007f-78b3-415d-9c62-3c8fdb4925a5" />


# WARNING! SMBIOS DETAILS ARE NOT INCLUDED IN THE CONFIG.PLIST.
You will have to use [GenSMBIOS](github.com/corpnewt/GenSMBIOS) to generate a **MacBookPro9,2** SMBIOS for your system, and add them to the config.plist.
Make sure you're on BIOS [F74](https://ftp.hp.com/pub/softpaq/sp96001-96500/sp96091.exe) before continuing. Older versions may cause issues

## Other macOS versions?
No. Catalina is the latest supported by MacBookPro9,2, so it's all I'll ever support. If you want a different version, feel free to fork this repo to modify it for whatever version you want. Do note newer versions will likely require OCLP.

## System specs
Do note if your hardware differs, while unlikely, you may have issues.
- CPU: Intel Core i5-3320m
- GPU: Intel HD Graphics 4000
- Chipset: Intel HM77
- Touchpad: Synaptics PS/2
- Audio: some IDT thing i forgot the exact model
- Wi-Fi: Intel Centrino Advanced-N 6205
- Ethernet: Intel 82579LM

## Issues:
- The SD Card reader does not work. The Alcor card reader HP uses is not supported in macOS.
- Fingerprint sensor does not work. macOS requires a T1 or T2 chip for fingerprint to work, which only real Macs have, and the drivers for the Synaptics fingerprint sensor used in the 6570b are very closed source.
- The touchpad tends to stick to lines and is very sensitive. You can lower the sensitivity in System Preferences to make the issue less severe.

If you notice any other problems, please open an issue (or pull request if you have a fix)
