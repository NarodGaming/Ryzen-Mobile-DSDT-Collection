# The Ryzen Mobile DSDT Repository

The purpose of this Github repository is to provide different edited/patched dsdts for a hassle-free experience so you can just download-paste-boot and enjoy!  
This repo is still a work in progress, meaning it will be updated periodically to add new laptop models or remove some files which are obsolete, or giving issues. 

**Please read the notice below before scrolling any further.**

# NOTICE
**Carefully and thoroughly read this README before proceeding**, anything and everything that **happens to you** OR **your laptop is NOT my responsibility**. Continue at your own risk. **Do NOT** use a DSDT from other laptop models or even the same model with a different BIOS. If you do so, you will more than likely get a BSOD saying "ACPI error". This can be easily fixed by booting straight into Windows from the BIOS boot menu to avoid clover and from there you will need to delete the dsdt.aml.

Some DSDTs will have no BIOS number because I don't know the BIOS version for it. If I get those BIOS version numbers, I'll update it as soon as possible.

### What is a DSDT?

A [**DSDT**](https://wiki.archlinux.org/index.php/DSDT) (Differentiated System Description Table) is part of the ACPI specification. It supplies information about supported power events in a given system. ACPI tables are provided in firmware from the manufacturer.

### HOW TO 

1. Install [**Clover Bootloader**](https://drive.google.com/file/d/1RyMn8D_9jE3nce1-ebiNq6CMzyAqfPfW/view) and follow this guide as shown: https://www.youtube.com/watch?v=qhSciG2SKu4

2. Paste the downloaded **dsdt.aml** file to `\EFI\CLOVER\ACPI\WINDOWS\`. If you don't see a `WINDOWS` folder, create it and paste the DSDT inside the folder. Make sure the file is called `dsdt.aml`!

3. **Reboot to Clover and then into Windows to load the dsdt.aml (EVERYTIME YOU BOOT)**

### EDITING A DSDT ON YOUR OWN

Report your issues in our [**discord server**](https://discord.gg/qEAfkuA) or in the github itself if you know how to do that (under 'Issues').

Some dsdt.aml files are decompiled to .dsl files and the errors have been fixed so people can edit the .dsl and compile to .aml as shown in the [**video here**](https://www.youtube.com/watch?v=Oerq0w140EI) so you will see *"fixed dsdt dsl"* files - ignore them if you are just here for the .aml files.

What we are doing is editing the ACPI Tables (dsdt) to change the STAPM limit, TDP limit, Temperature limit or more that we want and injecting the patched dsdt with **CLOVER BOOTLOADER** on every boot, so if you reboot and go directly into Windows you will have the default values and not the edited values. *For the patched dsdt to load into Windows you have to first boot into Clover Bootloader and then to Windows*

[**Tutorial For STAPM/TDP**](https://www.youtube.com/watch?v=Jre0QfLdJ5A) 

<details>
  <summary>Tutorial for STAPM / TDP (Power limits)</summary>
  <iframe width="560" height="315" src="https://www.youtube.com/embed/Jre0QfLdJ5A" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</details>

[**Tutorial For Temperature**](https://www.youtube.com/watch?v=w_vV_xpwiho)

[**Tutorial For Ryzen Mobile Max GPU frequency BOOST**](https://www.reddit.com/r/Amd/comments/alp4zt/ryzen_mobile_max_gpu_frequency_boost/)

A text tutorial on how to edit your own values into your dsdt can be found [**here**](https://pastebin.com/3wB2k7Ei)  - it's recommended you watch the video alongside to get a better understanding though.

The DSDT files are all generally in the compiled format (.aml) which we can't edit without DECOMPILING them to .dsl which makes it easier to edit even with a notepad or some other text editor but we recommended a dsdt editor, one can be found above at the start of the how to section.

After editing and compiling the EDITED/PATCHED dsdt.aml, paste it as mentioned in the text tutorial or video and boot into clover then into windows and voila, enjoy your free performance!

### This is a work in progress. if you have any doubts/errors/ideas feel free to do contact us in the [Discord server](https://discord.gg/qEAfkuA)
