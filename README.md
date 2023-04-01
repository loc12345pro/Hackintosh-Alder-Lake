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
- Disable the following:
  - Fast Boot 
  - MSI Fast Boot
  - Secure Boot
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
