# Lenovo Ideapad Flex 5 (15IIL05) Hackintosh
This is a hackintosh project for the Lenovo Ideapad Flex 5, which uses OpenCore v0.7.8. Currently, it runs perfectly fine using an external SSD (I'm using the Samsung Portable T7). When trying to install MacOS on the internal SSD, the installer will freeze completely after a couple of minutes.

Things that are not working (yet)
- External video output (such as HDMI)
- Internal trackpad
- Internal microphone
- Internal SSD

For now, I have only tested my EFI folder in combination with Catalina. However, you should be able to boot all MacOS versions between 10.15.4 and 11.2.3 (>= 11.3 requires USB mapping, which I have not done) just fine.

## Setup
1. Format your USB as FAT32, and create a folder on it named com.apple.recovery.boot
2. Generate SMBIOS for MacbookAir9,1 and change the values accordingly in the config.plist with ProperTree
3. Paste the EFI folder with the updated SMBIOS onto the root of your freshly formatted USB
4. Use macrecovery.py to download the BaseSystem DMG and chunklist file
5. Place the downloaded BaseSystem files under the com.apple.recovery.boot folder you created earlier
6. Boot using the USB, press the spacebar to show all bootable drives, and select the name of your USB
7. Go to the Disk Utility section, click on View on the top and then click on "Show all drives"
8. Erase/format the external SSD as APFS with a GUID partition scheme, after that is done; quit the Disk Utility
9. Connect to a WiFi network, and follow the instructions to install MacOS
10. Follow this YouTube tutorial starting at 9:01 to boot from SSD in the future: https://youtu.be/IP7crXa-5lo?t=541

I am NOT responsible and can NOT be held liable for anything that happens as a result of any actions you take. Make sure to backup your data as you will be formatting a USB and an external SSD.
