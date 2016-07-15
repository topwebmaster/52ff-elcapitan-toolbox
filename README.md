## Acer Aspire V3-371-52FF El Capitan toolbox

### Abilities:

 - Extract needed ACPI tables (DSDT, SSDT-3)
 - Decompile those tables into .DSL
 - Apply patches from directory
 - Compile patched tables back to .AML
 - Generate SSDT with ssdtPRGen.sh script by PikerAlpha
 - Compile patches with config for UsbInjectAll.kext
 - Install kexts from folder
 - Install additional VoodooPS2Controller files if this kext is present in kexts folder

### How to use

```
################################################################################
usage: toolbox.py [-h] [-e] [-p] [-c] [-u] [-k] [-a]

Acer Aspire V3-371-52FF El Capitan toolbox

optional arguments:
  -h, --help           show this help message and exit
  -e, --extract        extract needed ACPI tables and decompile it
  -p, --patch          apply patches located at `patches` subfolder
  -c, --compile        compile ACPI tables
  -u, --usb            compile USB ports config
  -k, --install-kexts  install kexts located at `kexts` subfolder
  -a, --all            run all actions

Credits: ssdtPRGen.sh by PikerAlpha, ACPI patches and kexts by RehabMan.
Project located at: https://github.com/Ty3uK/52ff-elcapitan-toolbox
################################################################################
```

 - Clone with git or download as [zip archive](https://github.com/Ty3uK/52ff-elcapitan-toolbox/archive/master.zip):
```bash
git clone https://github.com/Ty3uK/52ff-elcapitan-toolbox.git
```

 - Navigate to directory with terminal and run ```python toolbox.py``` or ```./toolbox.py``` for getting help

 - You can combine script arguments together. For example, ```-ep``` will extract ACPI and apply patches, ```-k``` install kexts. Use ```-a``` for all actions.

 - After script success, copy files from ```acpi``` folder into ```EFI\CLOVER\ACPI\patched``` and configurate Colver to drops OEM tables.

 - Reboot. Thats it!

 ### Credits

 - RehabMan: patches, kexts and greatest help on tonymacx86.com forum. Cheers!
 - PikerAlpha: ssdtPRGen.sh script and various information in internet, thanks!

 ### Changelog

 #### 15.07.2016
 - Initial release. Checked on El Capitan 10.11.5.

 &copy; Maksim Karelov aka Ty3uK, 2016