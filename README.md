# Raspberry 3B+ Project



# * Spesifikasi Raspberry 3B+

## Prosesor dan Memori

SoC : Broadcom BCM2837B0, ARM Cortex-A53 (ARMv8) 64-bit
Kecepatan CPU: Quad-core 1.4 GHz
GPU : Broadcom VideoCore IV
RAM : 1 GB LPDDR2 SDRA

## Konektivitas & Jaringan

Wi-Fi: Dual-band 2.4GHz dan 5GHz IEEE 802.11.b/g/n/ac wireless LAN
Bluetooth: Bluetooth 4.2 dan Bluetooth Low Energy (BLE)
Ethernet: Gigabit Ethernet melalui USB 2.0 (kecepatan maksimal sekitar 300 Mbps

## Port & Antarmuka

Port USB: 4 buah port USB 2.0
Port HDMI: 1 buah port HDMI ukuran penuh (full-size)
Audio & Video: Jack audio 3.5 mm 4-pole untuk stereo dan video komposit
GPIO: Extended 40-pin GPIO header
Kamera (CSI): Port CSI untuk koneksi ke Raspberry Pi Camera
Layar (DSI): Port DSI untuk koneksi ke Raspberry Pi Touchscreen Display
Penyimpanan: Slot kartu Micro SD untuk sistem operasi dan penyimpanan data

## Daya & Fitur Tambahan

Catu Daya (Power Input): 5V / 2.5A DC via port micro-USB atau melalui pin GPIO
Power-over-Ethernet (PoE): Mendukung PoE melalui tambahan aksesori PoE HAT terpisah
Suhu Operasional: 0°C sampai 50°C

# * Project yang saya buat

1. Print Server, dengan CUPS
2. Obsidian Server, dengan

## 1. Print Server

Tahapan :

1. Install CUPS sebagai print server via dietpi-software
2. Printer yang saya gunakan adalah HP Smart Tank 520, sehingga saya perlu menambahkan librari HP dengan perintah
   " apt install -y hplip printer-driver-hpcups avahi-daemon"
3. Saya kesulitan saat koneksi via web, sehingga memerlukan perintah tambahan :
   "sudo /usr/lib/cups/backend/usb"
   dimana hasilnya
   " DEBUG: Loading USB quirks from "/usr/share/cups/usb".
   DEBUG: Loaded 120 quirks.
   DEBUG: list_devices
   DEBUG: libusb_get_device_list=5
   DEBUG2: iSerialNumber="TH53A4T42G"
   DEBUG2: Printer found with device ID: MFG:HP;MDL:Smart Tank 520_540 series;CMD:PCL3GUI,PJL,Automatic,JPEG,DW-PCL,802.11,DESKJET,DYN;CLS:PRINTER;DES:1F3W2A;CID:HPIJCCAV1;CDMDIS:/cdm/servicesDiscovery;SN:TH53A4T42G;S:038800C480000001006c24000fec14000fe04400064054000640640006401400064;Z:05000008000008000001000001000001000001,12000,17000000000000000000000000000000000000,180; Device URI: usb://HP/Smart%20Tank%20520_540%20series?serial=TH53A4T42G&interface=1
   direct usb://HP/Smart%20Tank%20520_540%20series?serial=TH53A4T42G&interface=1 "HP Smart Tank 520_540 series" "HP Smart Tank 520_540 series" "MFG:HP;MDL:Smart Tank 520_540 series;CMD:PCL3GUI,PJL,Automatic,JPEG,DW-PCL,802.11,DESKJET,DYN;CLS:PRINTER;DES:1F3W2A;CID:HPIJCCAV1;CDMDIS:/cdm/servicesDiscovery;SN:TH53A4T42G;S:038800C480000001006c24000fec14000fe04400064054000640640006401400064;Z:05000008000008000001000001000001000001,12000,17000000000000000000000000000000000000,180;" ""
   Ambil Device URI dari " usb://HP/Smart%20Tank%20520_540%20series?serial=TH53A4T42G&interface=1"
