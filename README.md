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
  - RAM: [Kingston Fury Beast Black 8GB 3200MHz DDR4](https://www.amazon.com/Kingston-Desktop-Memory-Single-KF432C16BB/dp/B097K5J1SB)
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
