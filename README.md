# ACER-F5-573G-Hackintosh

Complete EFI for ACER F5-573G, to make Hackintosh using macOS Mojave 10.14.3 (18D109)

⚠️ Before editing, I suggest that you open the config.plist of the EFI folder, in the SMBIOS tab generate a new serial in the "Serial Number" field, check the site https://checkcoverage.apple.com/ if the serial is INVALID, that's it INVALID, it can not be from a real Mac. Copy the "Serial Number" to the "Board Serial Number" field and add 5 more random characters, copy this "Board Serial Number" and go to the "Rt Variables" tab and paste in the "MLB" field, click "Generate" to generate a valid ROM, open the macOS terminal and type "uuidgen" and copy the displayed value and paste in "SmUUID" in the "SMBIOS" tab, also paste in the "System Parameters" tab in the "Custom" UUID "the value copied from the terminal, done that, save and restart.

# IO80211Family
**IO80211Family.kext** [download](https://drive.google.com/file/d/1ZF1iDlaztfGoGXGQTbGlu106oocgFXdB/view?usp=sharing)

The Kext that must be installed in the System/Library/Extensions with the help of the Kext Utility are:  
After installing kext, open the terminal and run the commands:

```
sudo kextcache -i/
```

# Audio Headphone FIX

1) Download the **ALCJackEAPDFixP2HDA** [from here](https://drive.google.com/file/d/1oBUW2uCtfG2LN5YBz3lX8x6mJdnj9xHl/view?usp=sharing)
2) Extract the folder on the Desktop
3) Open the terminal and type:

```
cd Desktop
cd ALCJackEAPDFixP2HDA/
sudo ./Install.sh
```

You will be asked for your password, type and restart the computer for an effective result.

# Status

| Device                                          | Status |
| ----------------------------------------------- |:------:|
| Wi-Fi                                              | ✅ |
| Keyboard                                           | ✅ |
| Trackpad                                           | ✅ |
| USB 2.0 and 3.0                                    | ✅ |
| USB-C                                              | ✅ |
| Port VGA                                           | ✅ |
| Port HDMI                                          | ✅ |
| Audio with AppleALC                                | ✅ |
| Microphone                                         | ✅ |
| Earphone                                           | ✅ |
| Intel HD Graphics 620 Video Acceleration           | ✅ |
| Porta de Rede Ethernet                             | ✅ |
| Battery Power Management                           | ✅ |
| Brightness adjustment by panel                     | ✅ |
| Keyboard Brightness Adjustment (FN+Left, FN Right) | ✅ |
| NVIDIA GeForce 940MX                    | ❌ No support |
| Card reader                             | ❌ No support |
| *Bluetooth                                         | ⚠️ |


*NOTE: Bluetooth for me, only works if I go into Windows 10, activate, reboot the machine and boot into macOS. According to Rehabman, it is a problem of managing the firmware of the notebook itself, however, it is recommended to use a 100% compatible BT dongle to avoid conflicts or stress of the user.