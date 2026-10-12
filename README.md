# Raspberry 3B+ Project

## Spesifikasi Raspberry 3B+
CPU :
Memory :

## Project yang saya buat
1. Print Server
2. Obsidian Server


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
