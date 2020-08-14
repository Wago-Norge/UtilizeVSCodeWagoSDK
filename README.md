# Utilize Visual Studio Code for Cross developement using Windows Subsystem for Linux (WSL)
Use Visual Studio Code to build C/C++ applications for Wago PFC
> Currently there is an issue with WSL so that building can not be done completely. Ptxdist go -q will throw an error. Pending.

<div align="left">
   <br>
  <img src="Img\VSCodeWSL.png"><br><br>
</div>

## Installation of WSL and Ubuntu distribution
Before installing any Linux distributions on Windows, you must enable the "Windows Subsystem for Linux" optional feature <br/>
[Install Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/install-win10)

> We will use the same Ubuntu version as proposed in the [WAGO-PFC-SDK installation](https://github.com/WAGO/pfc-firmware-sdk) <br/>
> Please note the difference between WSL version 1 and 2. We will here use version 2.

<div align="left">
   <br>
  <img src="Img\Powershell_wsl2.PNG"><br><br>
</div>


> Please note the settings found in 'Windows Features' and 'Turn Windows Features On Off'<br/>
> Hyper-V/Hypervisor platform is not needed for WSL. Only support for "Windows Subsystem" 

## Install the Software-Development-Kit (SDK) 
Fallow the steps in [WAGO-PFC-SDK installation](https://github.com/WAGO/pfc-firmware-sdk) <br/> 


```
Mycode
```


















