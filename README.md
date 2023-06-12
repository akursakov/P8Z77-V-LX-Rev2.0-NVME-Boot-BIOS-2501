
# ASUS P8Z77-V-LX Rev 2.0 Custom Bios (ver 2501) with support for NVMe Boot

This repository contains a custom bios for for the ASUS P8Z77-V-LX Rev2.0 motherboard. Version 2501 supports reading from NVMe drives when an adapter is used, but does not support booting from them. This BIOS includes a driver from the Z87 line of motherboards for that functionality.  

## Features
 - Support for **NVMe Boot**
 - Costom splash screen

# DISCLAIMER

***I AM NOT RESPONSIBLE FOR ANY DAMANGE THAT MIGHT OCCUR DURING THIS PROCESS. FLASHING YOUR BIOS REGULARLY CAN BRICK YOUR PC, LET ALONE USING A CUSTOM ONE. MAKE SURE YOU UNDERSTAND ALL OF THIS BEFORE ATTEMPTING ANY SORT OF FLASH. BY USING THIS BIOS, YOU AGREE THAT YOU UNDERSTAND THE RISKS INVOLVED IN THIS PROCESS***

***THIS BIOS IS KNOWN TO WORK ON ASUS P8Z77-V-LX Rev2.0, DO NOT USE IT ON ANY OTHER MOTHERBOARD BESIDES THIS ONE, AS IT IS UNKNOWN HOW IT WILL AFFECT YOUR SYSTEM. YOU HAVE BEEN WARNED.***

***IF YOUR WILLING TO TRUST SOME GUY ON THE INTERNET WITH A CUSTOM BIOS FILE, YOU'RE WILLING TO DEAL WITH ANY CONSEQUENCES THAT OCCUR.***

## Requirements

 - **P8Z77-V-LX Rev2.0**
 - **PCIe to NVMe adapter**
 - **Any NVMe drive connected to said adapter**
 - **Windows 10 installation on another drive that you can boot to**

## How to flash

This repository contains all the tools that you will need to make this happen. Before attempting this, make sure to read the ***DISCLAIMER***, there is some really important info in there. 

First step is:

***MAKE SURE YOU HAVE THE CORRECT MOTHERBOARD (ASUS P8Z77-V-LX Rev2.0) AND THAT YOU HAVE READ THE DISCLAIMER***

Then, make sure your drive is properly connected. If you do not have a GPU connected to the top PCIE 3.0 slot, you should use that slot, as otherwise your READ/WRITE speeds will be limited. If you do have a GPU, connect it to the bottom PCIe2.0 slot. While your speeds will be limited, it will still be faster than a SATA SSD. The following picture demonstrates that, make sure to use the top slot if you can.

<p align="center"> <a href="(https://github.com/EdinZiga/P8Z77-V-LX-Rev2.0-NVME-Boot-BIOS-2501/blob/main/Screenshots/Motherboard.jpg)" target="_blank" rel="noreferrer"> <img src="https://github.com/EdinZiga/P8Z77-V-LX-Rev2.0-NVME-Boot-BIOS-2501/blob/main/Screenshots/Motherboard.jpg" alt="Motherboard Photo"/> </a> </p>


After connecting the adapter with the drive, download this repository to your machine. Extract it anywhere you prefer, I suggest using your desktop as it is the easiest. After extracting the repository, do the following

 - Extract and install the ***ASUS AI Suite II Software*** from ***AI_Suite_II_Win7_Z10215***. Just run and go through the setup.
 - After the installation, run open AI Suite II, and navigate to the BIOS Flash option.
 - ***FOR THE LAST TIME CONFIRM YOU HAVE THE RIGHT MOTHERBOARD AND THAT YOU ACCEPT THE RISH OF BRICKING YOUR PC. THIS IS THE POINT OF NO RETURN***
 - You will be given an option to select a file. Select the ***P8Z77-V-LX-Standard BIOS.CAP*** file. Not the modified version, the ***STANDARD*** version.
 - Upon selection, the program will freeze up, this is normal as it is checking the integrity of the file. Wait until you're given an option to continue with the flash, ***but do not press it yet***
 - After getting the option to continue, navigate to the location of the bios file you just selected and do the following
   - Copy the name of the unmodified standard file.
   - Move the file to any other folder on your PC
   - Rename the modified bios file to the name of the standard bios file. In doing this, you are tricking the software into believeing its flashing an unmodified file, as the integrity check was passed.
 - ***POINT OF NO RETURN***
 - Continue with the flash, let the software do its work. It should take a minute or two. 
 - After it finishes, you will be prompted to restart your PC. Upon the restart, the PC should boot cycle two to four times. If you have a motherboard speaker installed, you will hear a single beep that confirms the boot was successful.
 - Go into the BIOS and configure your settings. Under the boot section, there will be an option for PCIe boot. Enable it and set it to what you prefer.
 - And you're done. From here you can install WIndows on that NVMe drive and use your pc as normal. Hopefully you are not left with a brick after the process


 ## Sources

 - BIOS File From - [ASUS P8Z77-V LX NVMe modded BIOS Ver 2501](https://winraid.level1techs.com/t/offer-asus-p8z77-v-lx-nvme-modded-bios-ver-2501/34938).
 - Flashing method - [How to flash a modded AMI UEFI BIOS](https://winraid.level1techs.com/t/guide-how-to-flash-a-modded-ami-uefi-bios/30627)



