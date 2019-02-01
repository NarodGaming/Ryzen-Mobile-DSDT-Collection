# NOTICE
**Carefully read this README before proceeding**, whatever **happens to you** OR **your laptop is NOT my responsibility** and it is your own. **Do NOT** use a DSDT from other laptop models or even the same model with a different BIOS. If you do, you will get a BSOD because of an ACPI error. This can be easily fixed by selecting Windows in the boot menu to avoid clover and then you need to delete the dsdt.aml.

You will see some models without a BIOS number because it hasn’t been reported to me yet. When I have those BIOS version numbers, I'll update it as soon as possible.

### What is a DSDT?

[**DSDT**](https://wiki.archlinux.org/index.php/DSDT) (Differentiated System Description Table) is a part of the ACPI specification. It supplies information about supported power events in a given system. ACPI tables are provided in firmware from the manufacturer.

This repo is still a work in progress, meaning it will be updated periodically to add new laptop models or remove some files which are obsolete, or possibly giving issues. 

### HOW TO 

1. Install [**Clover Bootloader**](https://drive.google.com/file/d/1RyMn8D_9jE3nce1-ebiNq6CMzyAqfPfW/view) and follow this guide as shown: https://www.youtube.com/watch?v=qhSciG2SKu4

2. Paste the downloaded **dsdt.aml** file to `\EFI\CLOVER\ACPI\WINDOWS\`. If you don't see a Windows folder, create it and paste the DSDT inside the folder. **Reboot to Clover and then into Windows to load the dsdt.aml (EVERYTIME YOU BOOT)**

The purpose of this Github is to provide different edited/patched dsdts for a hassle-free experience so you can just download-paste-boot-enjoy  

**EDIT DSDT.AML ON YOUR OWN**  
Report Your issues in our discord server if you can or in the github itself if you know how to do that. If you don't, then communicate with me/us through our glorious [**Discord Server**](https://discord.gg/qEAfkuA)

Some dsdt.aml files are decompiled to .dsl files and the errors have been fixed so people can edit the dsl and compile to aml as shown in [**Video here**](https://www.youtube.com/watch?v=Oerq0w140EI) so you will see *"fixed dsdt dsl"* files - ignore them if you are just here for the .aml files.

What we are doing is editing the ACPI Tables(dsdt) to give us the STAPM limit, TDP limit or even Temperature limit we want and injecting the patched dsdt with **CLOVER BOOTLOADER** on every boot, so if you reboot and go directly into Windows you have the default values and not the edited values. *For the patched dsdt to load into Windows you have to first boot into Clover Bootloader and then to Windows*

[**Tutorial For STAPM/TDP**](https://www.youtube.com/watch?v=Jre0QfLdJ5A) 

[**Tutorial For Temperature**](https://www.youtube.com/watch?v=w_vV_xpwiho)

[**Tutorial For Ryzen Mobile Max GPU frequency BOOST**](https://www.reddit.com/r/Amd/comments/alp4zt/ryzen_mobile_max_gpu_frequency_boost/)

Text tutorial to edit your own values into your dsdt can be found [**here**](https://pastebin.com/3wB2k7Ei) it's recommended you watch the video alongside to get a better understanding though.

The DSDT files are all generally in Compiled format (.aml) which we can't edit without DECOMPILING them to .dsl which makes it easier to edit even with a notepad or some other text editor but we recommended a dsdt editor, one can be found above at the start of the how to section.

After editing and compiling the EDITED/PATCHED dsdt.aml, paste as mentioned in the text tutorial or video and boot into clover then into windows from there and voila, enjoy your free performance!

### This is a work in progress. if you have any doubts/errors/ideas feel free to do contact us in the [Discord server](https://discord.gg/qEAfkuA)
