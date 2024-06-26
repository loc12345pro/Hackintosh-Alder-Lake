# Versions

- macOS: Ventura (13.1)
- Windows: 11 Pro (22H2)
- Ubuntu: 22.04 LTS
- OpenCore: 0.9.0

# PC components

  - PSU: [ASUS TUF GAMING 750W Bronze](https://www.amazon.com/ASUS-TUF-Axial-tech-Technology-Certification/dp/B08SBY73C2)
    - Good price.
    - Recommended by [PSU Cultist](https://cultists.network/140/psu-tier-list/).
    - Able to handle the system.
  - Case: [TUF gaming GT301](https://dlcdnets.asus.com/pub/ASUS/ODD/DC/GT301/E15889_TUF_Gaming_GT301_Series_UM_WEB.pdf)
    - Good airflow.
    - Four pre-installed fans (120mm): 3 fans on the front and 1 fan on the back.
  - CPU: [Intel® Core™ i5-12400 Processor](https://ark.intel.com/content/www/us/en/ark/products/134586/intel-core-i512400-processor-18m-cache-up-to-4-40-ghz.html)
    - 6 Performance-cores, no Efficient-cores -> No need optimize Alder Lake's heterogeneous core configuration.
    - Integrated GPU: Intel® UHD Graphics 730 -> Not supported by macOS -> Need to be switched off.
  - CPU Fan: [Intel Stock Alder Lake Heatsink](https://www.tomshardware.com/news/new-alder-lake-stock-heatsink-tested)
    - Quiet and powerful enough to handle the GPU's temperature.
  - Mainboard: [MAG B660M Mortar DDR4](https://download.msi.com/archive/mnu_exe/mb/MAGB660MMORTARWIFIDDR4_MAGB660MMORTARDDR4.pdf)
    - Good price.
    - Hackintosh-able mainboard.
    - Chipset: B660M.
    - Audio codec: Realtek ALCS1200A.
    - Network controller: RTL8125 2.5GbE Controller.
  - RAM: 4x [Kingston Fury Beast Black 8GB 3200MHz DDR4](https://www.amazon.com/Kingston-Desktop-Memory-Single-KF432C16BB/dp/B097K5J1SB)
    - No RGB lighting.
    - Affordable price and compatible to the CPU.
  - SSD: [Kingston A400 2.5-Inch SATA 3 480GB](https://www.amazon.com/Kingston-480GB-Solid-SA400S37-480G/dp/B01N0TQPQB)
    - Good price.
    - Drive model: KINGSTON SA400S37480G.
  - GPU: [NITRO+ AMD Radeon™ RX 6600 XT](https://www.sapphiretech.com/en/consumer/nitro-radeon-rx-6600-xt-8g-gddr6)
    - Good price.
    - Able to do 1080p gaming.
    - It is supported since macOS Monterey (12.1).
  - NVME (for Windows 11 and Ubuntu 22.04 LTS): 2x [Sabrent Rocket 500GB M.2 NVMe PCIe Gen 4.0 x4](https://sabrent.com/products/sb-rocket-nvme4-500)
  - HDD (for storing games on Windows 11) (RAID0): 2x [WD Blue 2TB 3.5 inch SATA III 256MB Cache 7200RPM](https://www.amazon.com/Western-Digital-Blue-Hard-Drive/dp/B08VH8R94B)
    - I've always wanted to setup RAID.
  - USB Keyboard: [Logitech K120](https://www.amazon.com/Logitech-920-002478-K120-USB-Keyboard/dp/B003ELVLKU)
  - USB Mouse: [Logitech M100R](https://www.amazon.com/Logitech-M100R-Wired-Mouse-Black/dp/B0080W1X6U)
  - WiFi PCIe card: [Apple Broadcom BCM943602CDP – 802.11 a/b/g/n/ac with Bluetooth 4.2](https://www.osxwifi.com/product/pc-hackintosh-apple-broadcom-bcm943602cdp-802-11-a-b-g-n-ac-bluetooth-4-2-limited-edition/)
    - Pricy: Around 116.65 USD (Custom fees included) to ship it to Vietnam.
    - Despite the cost, it works out of the box: WiFi works, Airdrop works, send/receive file via Bluetooth OK!

<details>
  <summary>Where to buy in southern Vietnam?</summary>

  - PSU 750W: https://kccshop.vn/nguon-may-tinh-asus-tuf-gaming-750b-750w-bronze/
  - Case GT301: https://kccshop.vn/vo-case-asus-tuf-gaming-gt301-mid-tower-mau-den-led-argb/
  - CPU: https://tinhocngoisao.com/products/cpu-intel-core-i5-12400-box-chinh-hang-2-50-up-to-4-40ghz
  - Mainboard: https://tinhocngoisao.com/products/mainboard-msi-b660m-mag-mortar-ddr4
  - RAM: https://memoryzone.com.vn/ram-pc-kingston-fury-beast-black-8gb-3200mhz-ddr4-kf432c16bb-8 (x4)
  - SSD: https://memoryzone.com.vn/ssd-kingston-a400-sata-3-480gb-sa400s37-480g
  - GPU: https://kccshop.vn/vga-sapphire-nitro-radeon-rx-6600-xt-gaming-oc-8gb/
  - NVME: https://hoanghapc.vn/ssd-sabrent-rocket-500gb-m.2-nvme (x2)
  - HDD: https://memoryzone.com.vn/hdd-wd-blue-2tb-3-5-inch-sata-iii-256mb-cache-7200rpm-wd20ezbx (x2)
  - WiFi PCIe card: Ask https://fado.vn/ to buy [Apple Broadcom BCM943602CDP – 802.11 a/b/g/n/ac with Bluetooth 4.2](https://www.osxwifi.com/product/pc-hackintosh-apple-broadcom-bcm943602cdp-802-11-a-b-g-n-ac-bluetooth-4-2-limited-edition/) for you.
  
</details>

<details>
  <summary>Finding hardware</summary>
  
  ## CPU Model
  ![cpu-model](https://user-images.githubusercontent.com/12621111/229268715-0bad97f7-2f80-4b85-aa95-194a9f167fb0.png)

  ## GPU Model
  ![gpu-model](https://user-images.githubusercontent.com/12621111/229268771-59fc056f-1a37-429d-bf75-46c1e0cef894.png)

  ## Chipset Model
  ![chipset-model](https://user-images.githubusercontent.com/12621111/229268816-7c6f934a-8556-4892-b956-a894f0ad6b80.png)

  ## Audio Codec
  ```console
  locpham@Loc-Ubuntu-PC:~/Work/01_hackintosh$ head /proc/asound/card0/codec#0
  Codec: Realtek ALCS1200A
  Address: 0
  AFG Function Id: 0x1 (unsol 1)
  Vendor Id: 0x10ec0b00
  Subsystem Id: 0x14627d42
  Revision Id: 0x100001
  No Modem Function Group found
  Default PCM:
      rates [0x5f0]: 32000 44100 48000 88200 96000 192000
      bits [0xe]: 16 20 24
  ```

  # Ethernet Controller
  ```console
  locpham@Loc-Ubuntu-PC:~/Work/01_hackintosh$ lspci | grep -i Ethernet
  0000:05:00.0 Ethernet controller: Realtek Semiconductor Co., Ltd. RTL8125 2.5GbE Controller (rev 05)
  ```

  ## Disk Drives
  ![disk-drives](https://user-images.githubusercontent.com/12621111/229268825-fe8a0867-7b97-495e-b5e6-d3b21acccfcb.png)

</details>

# PC Wiring

![pc-wiring](https://user-images.githubusercontent.com/12621111/229279699-1e5a9796-53c1-4489-9c55-b75ed8690528.jpg)

# BIOS Settings

- Notes:
  - The guide is for MSI BIOS version E7D42IMS.1A0.
  - The BIOS should be updated via [MS Center](https://www.msi.com/Landing/MSI-Center).
  - After updating BIOS, all settings will be set to default.
  - There is search icon on the right corner of MSI BIOS.
- Enable the following:
  - Intel VT-d Tech
  - Intel Virtualization Tech (VT-x)
  - Re-Size Bar Support
  - Hyper-Threading
  - XHCI Hand-off
  - Wake on LAN:
    - This setting may interfere with [Sleep in macOS](https://dortania.github.io/OpenCore-Post-Install/universal/sleep.html).
    - Disable it if you do not want to remotely power on the computer.
    - In my case, I really want this feature because I do not want to use the power button.
  - Trusted Platform Module:
    - This is required for Windows 11.
    - OpenCore suggests to turn it off. However, with it enabled, macOS still boots just fine. 
- Disable the following:
  - Fast Boot 
  - MSI Fast Boot
  - Secure Boot
    - Note: Windows Security may complain if Secure Boot is turned off.
  - Thunderbolt
  - CFG Lock
- XMP: Profile 2
  - The games will crash when setting XMP to Profile 1.
- Trusted Model Platform: Enabled.
  - This is for Windows 11.
- BIOS CSM/UEFI Mode: UEFI
- Internal SATA Mode: Intel VMD
  - Intel VMD is for 2 2TB hard disks which are used to store games.
  - When setting the mode to Intel VMD, macOS will not recognize any drives in Internal SATA Controller.
- External SATA Mode: AHCI
- Integrated Graphics Shared Memory: 64M (default)
- NX Bit (Execute Disable Bit): Yes (read-only)
- Follow this video to setup RAID0 for 2 2TB HDD drives: https://youtu.be/INjFklUQ7lE

<details>
  <summary>Where to set?</summary>

  ## VT-D/VT-X/CFG Lock
  ![VT-D_and_VT-X](https://user-images.githubusercontent.com/12621111/229274669-934df35c-7d56-4c1f-8217-fd384c8d5bfb.png)

  ## Re-Size Bar support
  ![RESIZE-BAR-SUPPORT](https://user-images.githubusercontent.com/12621111/229274784-bbe0e7e9-03cd-4cf8-aa4d-30293026413b.png)

  ## Hyper-Threading
  ![HYPER-THREADING](https://user-images.githubusercontent.com/12621111/229274809-f87b2355-d2e4-408e-b90b-0d778708f4cd.png)

  ## XHCI Hand-off
  ![XHCI-HANDOFF](https://user-images.githubusercontent.com/12621111/229274845-d80d78a8-ad34-4d00-847b-7e7389b8911d.png)

  ## Fast Boot/MSI Fast Boot
  ![Fastboot_and_MSI-Fastboot](https://user-images.githubusercontent.com/12621111/229274610-455c2d87-c8ea-4727-8a57-eb11079e9234.png)

  ## Secure Boot
  ![Secure-Boot](https://user-images.githubusercontent.com/12621111/229274904-129b6ab6-ff82-42b6-98a4-2d3e6f49cadc.png)

  ## Thunderbolt
  ![THUNDERBOLT](https://user-images.githubusercontent.com/12621111/229274935-f980b3e8-149b-498e-aaa0-18aa71d1b5ba.png)

  ## BIOS CSM/UEFI Mode
  ![BIOS_UEFI](https://user-images.githubusercontent.com/12621111/229274984-57cb15c5-e0ef-4098-af9c-5cbed3b65b76.png)

  ## Internal/External SATA Controller
  ![SATA-MODE](https://user-images.githubusercontent.com/12621111/229275017-f1a37561-845a-4d02-bdb4-a58d189f4027.png)

  ## Integrated Graphics Shared Memory
  ![DVMT-PREALLOCATED](https://user-images.githubusercontent.com/12621111/229275046-0ff0ff39-93e2-41c8-a9c6-c5e72d29b45b.png)

  ## NX bit (Execute Disable Bit) (read-only)
  ![NX-BIT](https://user-images.githubusercontent.com/12621111/229275111-11179ce6-d9d3-4ba0-a24c-f95b2d8d1618.png)
  
</details>

# Test results

- All USB Type-A ports (front panel and rear panel) work.
- USB Type-C port (rear panel) is disabled because I do not need it.
- Ethernet 2.5G port works.
- CPU works, however the performance is not good because [it's missing CPUFriend](https://chriswayg.gitbook.io/opencore-visual-beginners-guide/advanced-topics/using-alder-lake#opencore-config.plist-configuration).
- GPU works.
- Audio output port (rear panel) works. However, I did not test audio in/out port at front-panel.
- Audio input port (rear panel) works.
- Sleep does not work. Root-cause may be related to [power management](https://dortania.github.io/OpenCore-Post-Install/universal/pm.html).
- [LauncherOption](https://dortania.github.io/OpenCore-Post-Install/multiboot/bootstrap.html) does not work as expected. It creates a boot entry in BIOS, but does not allow me to delete BOOTx64.efi

# Helper tools

- [Rufus](https://rufus.ie/en/): Create USB installer.
- [iasl](https://acpica.org/downloads/binary-tools): Dump DSDT, compile .dsl files, decompile .aml files.
- [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS): Generate SMBIOS info.
- [ProperTree](https://github.com/corpnewt/ProperTree): Edit .plist file.
  - ProperTree supports macOS, too. If it opens a black window on Ventura, please follow steps here: https://github.com/corpnewt/ProperTree#faq to fix.
- [SSDTTime](https://github.com/corpnewt/SSDTTime): Create SSDT automatically.
- [USBToolBox](https://github.com/USBToolBox/tool): For USB mapping.
- [RadeonGadget (macOS app)](https://github.com/aluveitie/RadeonSensor/tree/master/RadeonGadget): Show GPU's temperator (for post-install setup).
- [IORegistryExplorer (macOS app)](https://github.com/khronokernel/IORegistryClone/blob/master/ioreg-302.zip): For checking if Audio or Power Management is setup correctly?
- [MountEFI (macOS tool)](https://github.com/corpnewt/MountEFI): Mount EFI Paritition (in Hackintosh drive).
- [gfxutil (macOS tool)](https://github.com/acidanthera/gfxutil/releases): Find route for PCI, Audio...

# Making installer in Windows
- Follow steps here: https://dortania.github.io/OpenCore-Install-Guide/installer-guide/windows-install.html#downloading-macos
- Notes:
  - Remember to set Python3 environment variables in the Python3 installer.
  - Before downloading macOS recovery files, please note that the command is **python, not python3**:
    ```console
    python macrecovery.py -b Mac-4B682C642B45593E -m 00000000000000000 download
    ```
  - Create USB installer with Rufus 3.21:  
    ![rufus-3 21](https://user-images.githubusercontent.com/12621111/229291489-2236676e-9632-4d8b-82de-29d630985f4b.png)
  - Please use OpenCore debug version. Then, we can change it to release version after fixing all issues.

# Adding firmware drivers

- Follow steps here: https://dortania.github.io/OpenCore-Install-Guide/ktext.html#firmware-drivers
- HfsPlus.efi **(required)**: 
  - Needed for seeing HFS volumes(ie. macOS Installers and Recovery partitions/images).
  - Do not mix other HFS drivers, such as: OpenHfsPlus.efi
- OpenRuntime.efi **(required)**: Replacement for [AptioMemoryFix.efi](https://github.com/acidanthera/AptioFixPkg), used as an extension for OpenCore to help with patching boot.efi for NVRAM fixes and better memory management.
- ResetNvramEntry.efi (optional): Required to reset the system's NVRAM

# Adding OpenCore tools

- OpenShell.efi **(required)**: Recommended for easier debugging

# Adding kexts

- Follow steps here: https://dortania.github.io/OpenCore-Install-Guide/ktext.html#kexts
- Lilu **(required)**: A kext to patch many processes, required for AppleALC, WhateverGreen, VirtualSMC and many other kexts. Without Lilu, they will not work.
- VirtualSMC **(required)**: Emulates the SMC chip found on real macs, without this macOS will not boot.
- SMCProcessor.kext **(required)**: Used for monitoring Intel CPU temperature.
- RadeonSensor.kext (optional): Required to read the GPU temperature and requires Lilu.
- SMCRadeonGPU.kext (optional): Can be used optionally to export GPU temperature to VirtualSMC for monitoring tools to read and requires VirtualSMC.
- SMCSuperIO.kext **(required)**: Used for monitoring fan speed.
- WhateverGreen.kext **(required)**: Used for graphics patching, DRM fixes, board ID checks, framebuffer fixes, etc; all GPUs benefit from this kext.
- AppleALC.kext **(required)**: Used for AppleHDA patching, allowing support for the majority of on-board sound controllers.
- LucyRTL8125Ethernet **(required)**: For Realtek's 2.5Gb Ethernet.
- RestrictEvents.kext **(required)**: Patch various functions of macOS, see [the README](https://github.com/acidanthera/RestrictEvents#boot-arguments) (opens new window)for more info.
- USBToolBox.kext and UTBMap.kext **(required)**:
  - https://chriswayg.gitbook.io/opencore-visual-beginners-guide/alternatives/usb-mapping-on-windows
  - https://dortania.github.io/OpenCore-Post-Install/usb/intel-mapping/intel.html

# USBMap

- Download latest tool from [USBToolBox](https://github.com/USBToolBox/tool/releases) repository.
- Follow the below instructions in [USBToolBox](https://github.com/USBToolBox/kext?tab=readme-ov-file#usage):
  ```text
  This is gonna be a very basic guide for now. A fully-fleshed guide will be released in the future.

  Download the appropriate download for your OS.
  Open and adjust settings if necessary.
  Select Discover Ports and wait for the listing to populate.
  Plug in a USB device into each port. Wait for the listing to show your USB device before unplugging it and plugging it into another port.
  If on Windows, you only need to plug in 1 device to USB 3 ports (as companion detection should be working). If on macOS, you will have to plug in a USB 2 device and a USB 3 device into each USB 3 port.
  For old computers with OHCI/UHCI and EHCI controllers, you will need to plug in a mouse/keyboard to map the USB 1.1 personalities, as most USB 2 devices will end on the USB 2 personality.
  Once mapping is done, go to the Select Ports screen.
  Select your ports and adjust port types as neccesary.
  Press K to build the kext!
  Add the resulting USB map to your EFI/OC/Kexts folder, and make sure to update your config.plist.
  If building a map that uses the USBToolBox kext, make sure to grab the latest release of the kext too.
  Make sure to remove UTBDefault.kext , if you have it.
  Reboot and you should have your USB map working!
  ```
- Prepare one USB 2.0 device, such as: keyboard or mouse and one USB 3.0 device, such as: USB flash drive (Kingston DataTraveler 3.0).
- In "D.  Discover Ports" mode, plug in and out USB 2.0 and 3.0 devices. Then, go to "S.  Select Ports and Build Kext" mode to select the ports and **confirm its type**.
- Based on [the hardware as above](#pc-components), the selected port should be like this:
  ```text
  #######################################################
  #            Select Ports and Build Kext              #
  #######################################################
  
  Intel(R) USB 3.20 eXtensible Host Controller - 1.20 (Microsoft) | USB 3.0 (XHCI) | 12/25 ports
  [ ]  1.  Port 1 | USB 2.0 | Type C - with switch (guessed) | Companion to 17
  [#]  2.  Port 2 | USB 2.0 | Internal
            - MYSTIC LIGHT - operating at USB 1.1
  [#]  3.  Port 3 | USB 2.0 | Internal
            - USB2.1 Hub - operating at USB 2.0
              - Dell MS116 USB Optical Mouse - operating at USB 1.1
              - USB Keyboard - operating at USB 1.1
  [ ]  4.  Port 4 | USB 2.0 | Type C - with switch (guessed) | Companion to 19
  [#]  5.  Port 5 | USB 2.0 | Type A
            - USB Keyboard - operating at USB 1.1
            - DataTraveler 3.0 - operating at USB 2.0
            - Dell MS116 USB Optical Mouse - operating at USB 1.1
  [#]  6.  Port 6 | USB 2.0 | Type A
            - USB Keyboard - operating at USB 1.1
            - Dell MS116 USB Optical Mouse - operating at USB 1.1
            - DataTraveler 3.0 - operating at USB 2.0
  [#]  7.  Port 7 | USB 2.0 | Type A
            - USB Keyboard - operating at USB 1.1
            - DataTraveler 3.0 - operating at USB 2.0
  [#]  8.  Port 8 | USB 2.0 | Type A
            - USB Keyboard - operating at USB 1.1
            - DataTraveler 3.0 - operating at USB 2.0
            - Dell MS116 USB Optical Mouse - operating at USB 1.1
  [#]  9.  Port 9 | USB 2.0 | Type A | Companion to 24
            - Dell MS116 USB Optical Mouse - operating at USB 1.1
  [#]  10. Port 10 | USB 2.0 | Type A | Companion to 25
            - Dell MS116 USB Optical Mouse - operating at USB 1.1
  [#]  11. Port 11 | USB 2.0 | Internal
            - USB2.0 Hub - operating at USB 2.0
              - Bluetooth USB Host Controller - operating at USB 1.1
  [ ]  12. Port 12 | USB 2.0 | Internal (guessed)
  [ ]  13. Port 13 | USB 2.0 | Internal (guessed)
  [ ]  14. Port 14 | USB 2.0 | Internal (guessed)
  [ ]  15. Port 15 | USB 2.0 | Type A (guessed)
  [ ]  16. Port 16 | USB 2.0 | Type A (guessed)
  [ ]  17. Port 17 | USB 3.0 | Type C - with switch (guessed) | Companion to 1
  [#]  18. Port 18 | USB 3.0 | Internal
            - USB3.2 Hub - operating at USB 3.1 Gen 2
              - DataTraveler 3.0 - operating at USB 3.0
  [ ]  19. Port 19 | USB 3.0 | Type C - with switch (guessed) | Companion to 4
  [ ]  20. Port 20 | USB 3.0 | Internal (guessed)
  [ ]  21. Port 21 | USB 3.0 | Internal (guessed)
  [ ]  22. Port 22 | USB 3.0 | Internal (guessed)
  [ ]  23. Port 23 | USB 3.0 | Internal (guessed)
  [#]  24. Port 24 | USB 3.0 | Type A | Companion to 9
            - DataTraveler 3.0 - operating at USB 3.0
  [#]  25. Port 25 | USB 3.0 | Type A | Companion to 10
            - DataTraveler 3.0 - operating at USB 3.0
  ```
- The meaning of each port is as below:
  - Front case (see page 1 of document [User Manual - Case TUF Gaming GT301]( https://dlcdnets.asus.com/pub/ASUS/ODD/DC/GT301/E15889_TUF_Gaming_GT301_Series_UM_WEB.pdf): 
    - USB 3.2 Gen1 Type-A ports (these ports are connected to JUSB3 port on [MAG B660M MORTAR WIFI DDR4 motherboard](https://download.msi.com/archive/mnu_exe/mb/MAGB660MMORTARWIFIDDR4_MAGB660MMORTARDDR4.pdf)):
    ```text
    [#]  24. Port 24 | USB 3.0 | USB 3 Type A (guessed) | Companion to 9
              - DataTraveler 3.0 - operating at USB 3.0
    [#]  25. Port 25 | USB 3.0 | USB 3 Type A (guessed) | Companion to 10
              - DataTraveler 3.0 - operating at USB 3.0
    ```
    - USB 2.0 Type-A ports (companion ports of USB 3.2 Gen1 ports (above)):
    ```text
    [#]  9.  Port 9 | USB 2.0 | USB 3 Type A (guessed) | Companion to 24
              - Dell MS116 USB Optical Mouse - operating at USB 1.1
    [#]  10. Port 10 | USB 2.0 | USB 3 Type A (guessed) | Companion to 25
              - Dell MS116 USB Optical Mouse - operating at USB 1.1
    ```
  - Back case (see "Rear I/O Panel" section of document [User Guide - MAG B660M MORTAR WIFI DDR4 motherboard](https://download.msi.com/archive/mnu_exe/mb/MAGB660MMORTARWIFIDDR4_MAGB660MMORTARDDR4.pdf)) :
    - USB 2.0 Type-A port (4 black ports):
    ```text
    [#]  5.  Port 5 | USB 2.0 | Type A (guessed)
              - USB Keyboard - operating at USB 1.1
              - DataTraveler 3.0 - operating at USB 2.0
              - Dell MS116 USB Optical Mouse - operating at USB 1.1
    [#]  6.  Port 6 | USB 2.0 | Type A (guessed)
              - USB Keyboard - operating at USB 1.1
              - Dell MS116 USB Optical Mouse - operating at USB 1.1
              - DataTraveler 3.0 - operating at USB 2.0
    [#]  7.  Port 7 | USB 2.0 | Type A (guessed)
              - USB Keyboard - operating at USB 1.1
              - DataTraveler 3.0 - operating at USB 2.0
    [#]  8.  Port 8 | USB 2.0 | Type A (guessed)
              - USB Keyboard - operating at USB 1.1
              - DataTraveler 3.0 - operating at USB 2.0
              - Dell MS116 USB Optical Mouse - operating at USB 1.1
    ```
    - USB 3.2 Gen2 Type-A ports (3 red ports):
    ```text
    [#]  18. Port 18 | USB 3.0 | Internal (guessed)
              - USB3.2 Hub - operating at USB 3.1 Gen 2
              - DataTraveler 3.0 - operating at USB 3.0
    ```
    - USB 2.0 Type-A ports (companion ports of USB 3.2 Gen2 Type-A ports (above)):
    ```text
    [#]  3.  Port 3 | USB 2.0 | Internal (guessed)
              - USB2.1 Hub - operating at USB 2.0
              - Dell MS116 USB Optical Mouse - operating at USB 1.1
    ```

# ACPI

## Fixing Embedded Controller (SSDT-EC/USBX)

- Follow steps here: https://dortania.github.io/Getting-Started-With-ACPI/Universal/ec-fix.html

## Fixing Power Management (SSDT-PLUG)

- Use `SSDT-PLUG-ALT.dsl` instead of `SSDT-PLUG.dsl` because we are using Alder Lake CPU:
  - https://chriswayg.gitbook.io/opencore-visual-beginners-guide/advanced-topics/using-alder-lake#acpi-greater-than-add
  - https://github.com/tarbaII/OpenCore-Install-Guide/blob/alderlake/config.plist/alder-lake.md#add

## Fixing System Clocks (SSDT-AWAC/RTC0)

- Follow steps here: https://dortania.github.io/Getting-Started-With-ACPI/Universal/awac.html

## Fixing SMBus support (SSDT-SBUS-MCHC)

- Follow steps here: https://dortania.github.io/Getting-Started-With-ACPI/Universal/smbus.html

## Disabling iGPU

- Because macOS does not support integrated GPU `Intel® UHD Graphics 730`, we must disable it by following this guide: https://dortania.github.io/OpenCore-Install-Guide/extras/spoof.html#disabling-gpu

# config.plist setup

- For final result, please refer here: https://github.com/loc12345pro/config.plist
- Follow steps in:
  - Common: https://dortania.github.io/OpenCore-Install-Guide/config.plist/#creating-your-config-plist
  - For Commet Lake (also for Alder Lake): https://dortania.github.io/OpenCore-Install-Guide/config.plist/comet-lake.html#starting-point
- Notes:
  - **Always remember to update config.plist before adding/removing .aml, .efi, or .kext files**.
  - Do not add DSDT.aml to config.plist because it's already in your firmware.
  - Do not mix .aml files with .dsl files.
  - Just delete `PciRoot(0x0)/Pci(0x1b,0x0)` which is already exists in `Sample.plist`.
  - Do not add `PciRoot(0x0)/Pci(0x2,0x0)` because the macOS does not support iGPU UHD 730.
  - Just ignore parts related to Ethernet controller `Intel I225 NIC`. The mainboard does not have it.
  - We do not need `PciRoot(0x0)/Pci(0x1b,0x0)` to install macOS. Let's fix it later.
  - In `Kernel->Quirks`, just set `DisableIoMapper` to `Yes` to keep `VT-D` enabled. Without `VT-D`, virtual machines may be affected.
  - Set `Kernel->Emulate` as described in: https://chriswayg.gitbook.io/opencore-visual-beginners-guide/advanced-topics/using-alder-lake#kernel-greater-than-emulate
  - For GPU support, please add options: `agdpmod=pikera unfairgva=1` to `boot-args`
  - For setting up the SMBIOS info, just use `MacPro7,1`:
    - https://chriswayg.gitbook.io/opencore-visual-beginners-guide/advanced-topics/using-alder-lake#platforminfo-greater-than-generic
    - https://dortania.github.io/OpenCore-Install-Guide/config.plist/comet-lake.html#platforminfo
    - Note:
      - When you boot Windows via OpenCore, `MSI Center` will not allow you to use `Mystic Light` or update BIOS/Drivers because `Model Name` is set to `MacPro7,1` instead of `MAG B660M MORTAR DDR4`.
      - When it happens, just press F11 continuously until you see `Boot Options`. Then, choose `Windows Boot Manager` to boot Windows 11 directly without OpenCore.

# Installing macOS

- Follow steps here: https://dortania.github.io/OpenCore-Install-Guide/installation/installation-process.html
- Notes:
  - Please do not remove `BOOTx64.efi` from `EFI/BOOT`. Otherwise, OpenCore cannot load boot entries.
  - Press `Space` to show `USB Drive (External)` [(see Rufus)](https://github.com/loc12345pro/Hackintosh-Alder-Lake#making-installer-in-windows).
  - Because the `Internal SATA Controller` is set to `Intel VMD`, macOS cannot see 2 NVME drives or 2 2TB HDD drives, except for 480GB SSD drive (which is connected to `External SATA Controller`).
  - If stuck at `[EB|#LOG:EXITBS:START]`, make sure to set [Booter->Quirks->SetupVirtualMap](https://github.com/loc12345pro/config.plist/commit/93472875171c660fc3f5822fd1a281b081703260) (https://dortania.github.io/OpenCore-Install-Guide/troubleshooting/extended/kernel-issues.html#stuck-on-eb-log-exitbs-start) in config.plist.

# Post-Install

## Fixing slide values

- Just follow steps here: https://dortania.github.io/OpenCore-Install-Guide/extras/kaslr-fix.html#so-what-is-kaslr
- Refer here: https://github.com/loc12345pro/config.plist/tree/main/fixing-kaslr-slide-values for how to calculate slide value.

## Security

- The file https://github.com/loc12345pro/config.plist does not contain [FileVault](https://dortania.github.io/OpenCore-Post-Install/universal/security/filevault.html), [Vault](https://dortania.github.io/OpenCore-Post-Install/universal/security/vault.html), [OpenCore Password Setup](https://dortania.github.io/OpenCore-Post-Install/universal/security/password.html), or [Apple Secure Boot](https://dortania.github.io/OpenCore-Post-Install/universal/security/applesecureboot.html).

## Using LauncherOption

- Follow the steps here: https://dortania.github.io/OpenCore-Post-Install/multiboot/bootstrap.html
- The file https://github.com/loc12345pro/config.plist added support for it. However, it does not work as expected because the BIOS does not show boot entry of OpenCore when `BOOTx64.efi` is deleted.

## WiFi

![20240106_Broadcom-BCM943602CDP](https://github.com/loc12345pro/Hackintosh-Alder-Lake/assets/12621111/b94e84f5-bb72-492d-b1d0-42cef1ac07db) ![20240106_Broadcom-BCM943602CDP-2](https://github.com/loc12345pro/Hackintosh-Alder-Lake/assets/12621111/13608a6e-c3ee-4485-8322-dd9afa2e6201)

### Hardware setup

- Use USB 2.0 headers to connect the Bluetooth wiring!
- Compatible to PCI-E x4, PCI-E x8, PCI-E x16 slots.
- The bracket is compatible to ATX PC case.

### Software setup

- MacOS: Auto!
- Ubuntu: Auto!
- Arch Linux:
  - If your system uses [NetworkManager](https://wiki.archlinux.org/title/NetworkManager), follow steps in [2.1. nmcli examples](https://wiki.archlinux.org/title/NetworkManager#nmcli_examples).
  - If there is no network manager in your system, use [wpa_suppliant](https://wiki.archlinux.org/title/wpa_supplicant) to for configuration and connection.
- Windows 11:
  - For Bluetooth: Use [6.1.6700.0 (04-10-2016).zip](https://github.com/loc12345pro/Hackintosh-Alder-Lake/files/13850078/6.1.6700.0.04-10-2016.zip). The driver is not signed. Use at your own risks!
  - For Wifi: Use [PCIe Dongle (1.558.53.1 - 22.10.2017).zip](https://github.com/loc12345pro/Hackintosh-Alder-Lake/files/13850082/PCIe.Dongle.1.558.53.1.-.22.10.2017.zip). Again, the driver is not signed. Use at your own risks!

<details>
  <summary>How to manually add drivers on Windows 11?</summary>

  - Open Device Manager.
  - Click on Bluetooth or WiFi icon with warning sign. Then click Action > Add drivers.
  - Browse to the location of extracted drivers (see above). Then, click Next and Finish!
  - *Note:* The driver is not signed so Windows will raise warnings. If so, just ignore it!
  
</details>
