# ESE 519 Embedded system Lab2 Set-up guide

Name: Qiao Xu
Student ID:697405
Computer Processor:11th Gen Intel(R) Core(TM).
i5-11300H @ 3.10GHz, 2611 Mhz, 4 Core(s), 8 Logical Processor(s).
System Model	Inspiron 14 5410. x64-based PC.
OS Name	Microsoft Windows 11 Pro

------------
## Prelab
### Installation for subsystem of Windows
#### Download Ubuntu
The instruction can be accessed at the [website](https://www.onmsft.com/how-to/install-ubuntu-on-windows-10-or-windows-11)
![1](https://user-images.githubusercontent.com/113159375/195965167-4148e6e9-61e6-413b-8a5d-5936f4db8426.jpg)

*Problem:* I could not start the Ubuntu virtual machine because the home version of my computer did not meet Hyper-V system requirements. 
(https://learn.microsoft.com/en-us/windows/wsl/troubleshooting#error-0x80370102-the-virtual-machine-could-not-be-started-because-a-required-feature-is-not-installed)
*Solution:* Check the system requirement for Hyper-V.---Find my computer version did not meet the requirement--upgrade my computer to Windows11 Pro, with $99
#### Download VIM on the Windows
The instruction can be found at https://www.vim.org/download.php
https://www.freecodecamp.org/news/vim-windows-install-powershell/ 

I did not use the Ubuntu as the subsystem when I am going through the lab, but it is a great exprience to set it up.


------------
## Lab2A set-up guide

### Download VS studio editor
link： https://code.visualstudio.com/docs/?dv=win64user  
#### Build code for RP2040 on MS windows
with reference to the Chapter 9 in the provided link https://datasheets.raspberrypi.com/pico/getting-started-with-pico.pdf 
![2](https://user-images.githubusercontent.com/113159375/195965255-099b52fd-0579-49b9-84a3-901f6e57ec08.jpg)
#### Download Arm GNU Toolchain
Link: https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/downloads 
![3](https://user-images.githubusercontent.com/113159375/195965258-634a8acb-a6bc-4b4b-a29c-8252dcc1a353.jpg)
#### Download Cmake
Link: https://cmake.org/download/ —> choose windows installer
![4](https://user-images.githubusercontent.com/113159375/195965292-1c85f1d1-8cf4-4458-8fd0-c4745229b7da.jpg)
#### Build Toolds for VS Studuio 2022
Link: https://visualstudio.microsoft.com/downloads/#build-tools-for-visual-studio-2022 
#### Download Python 3.10
Link: https://www.python.org/downloads/windows/ 
Because I have downloaded the 3.10.5 before, so I upgrade it to the latest version 3.10.8
#### Download Git
Link: https://git-scm.com/download/win 

### Get the pico SDK and pico examples
Tips：If you do not know how to use cmd, I found a website that might be useful for you to learn some basic commands. At [](Link： https://www.earthdatascience.org/courses/intro-to-earth-data-science/open-reproducible-science/bash/bash-commands-to-manage-directories-files/)
#### Open Developer Command Prompt Window for VS 2022 
#### type the three commands shown below to create a pico directory to keep all pico related checkouts in.
![5](https://user-images.githubusercontent.com/113159375/195965472-59aa9262-17c5-457a-9c34-8ff3b17b344a.jpg)
*Problems*: If you do not use as administrator, the access will be denied. This happens when I use the system Command Prompt Window and also the Developer command prompt window for VS 2022.
![6](https://user-images.githubusercontent.com/113159375/195965478-1d9a039b-92f9-494b-81c1-076a7038e267.jpg)
*Solutions*: Open the command prompt window as administrator!
![7](https://user-images.githubusercontent.com/113159375/195965481-ff1b4a8b-543f-4bb8-9143-af57a49f4368.jpg)
When first opening the Prompt as administrator, you may need to type : cd/ to return to the hope page and then reenter the User directory under the home directory.
![8](https://user-images.githubusercontent.com/113159375/195965488-fe7340ed-854a-450a-a059-fb45000bb2b1.jpg)
#### clone the pico-sdk and pico-examples git repositories
![9](https://user-images.githubusercontent.com/113159375/195965736-38687434-c689-4f53-a592-9c2d77e571b9.jpg)

### Build “Hello World” from the command line
![10](https://user-images.githubusercontent.com/113159375/195965788-ef04ddc4-80ff-410a-a12d-7e56105698ff.jpg)
(so far there is no need to attach the RP2040 board to the computer using USB.)

### Flash the board and run “Hello World”
![11](https://user-images.githubusercontent.com/113159375/195965812-936fa735-0cfb-45c2-bcf7-63a0668797e9.jpg)
#### Download the app Putty, which can be done following the instructions on the website
![12](https://user-images.githubusercontent.com/113159375/195965846-a9fa303e-610b-403a-a30d-20ba3b233e9b.jpg)
Link: https://learn.adafruit.com/welcome-to-circuitpython/advanced-serial-console-on-windows 
#### Hold down the Boot button, and click the Reset button, then you will see the board appear as an external drive. The result is shown below.
***Notice:*** You have to choose the first one. If you drag the UF2 file into the second one, the external drive will disappear too, but you won’t find the serial port number, which means the Putty could not run successfully.
#### Drag the UF2 file to the external drive.
#### Check the device manager again to see the port serial number
***Notice:*** The port might be different compared to the circuitpythonUF2 profile we used in lab 1. The one in my computer changed from COM3 to COM6. So if you use the same one as before, it may not work.
![13](https://user-images.githubusercontent.com/113159375/195965879-73edc80f-1a2f-457a-9db1-519bf7482cc5.jpg)



