# Utilize Visual Studio Code for Cross developement using Windows Subsystem for Linux (WSL)
Use Visual Studio Code to build C/C++ applications for Wago PFC

<div align="left">
   <br>
  <img src="Img\VSCodeWSL.png"width="600" hight="500"> <br><br>
</div>

## Installation of WSL and Ubuntu distribution
Before installing any Linux distributions on Windows, you must enable the "Windows Subsystem for Linux" optional feature <br/>
[Install Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/install-win10)

> We will use the same Ubuntu version as proposed in the [WAGO-PFC-SDK installation](https://github.com/WAGO/pfc-firmware-sdk) <br/>
> Please note the difference between WSL version 1 and 2. We will use version 2.

> <div align="left">
>  <br>
>  <img src="Img\Powershell_wsl2.PNG" width="300" hight="300"> <br><br>
> </div>

> Hyper-V/Hypervisor platform is not needed for WSL. Only support for "Windows Subsystem" <br/>
> See 'Windows Features' and 'Turn Windows Features On Off'<br/>

## Install the Software-Development-Kit (SDK) 
Fallow the steps in [WAGO-PFC-SDK installation](https://github.com/WAGO/pfc-firmware-sdk) <br/> 
> ***************************************************************************************************************************** <br/>
> Currently there is an issue with WSL so that building can not be done completely. Ptxdist go -q will throw an error. Pending. <br/>
> ***************************************************************************************************************************** <br/>

## Install Visual Studio Code
Visit [Microsoft help page](https://docs.microsoft.com/en-us/windows/wsl/tutorials/wsl-vscode) to get started

## Install C/C++ extension for Visual Studio Code
Visit the 'Marketplace' inside VS Code and install the C/C++ extension that features GCC compiler etc. <br>
> We will not use this "toolchain" but rather the one provided by Wago SDK <br>

## Install sshpass
```
sudo apt-get install sshpass
```

## Example Hello World application
This example shows how to make, build/compile and debug/download a 'Hello World' application to PFC with Visual Studio Code

**Make a project folder and start Visual Studio Code project from here** <br>
```
mkdir vscode_projects && mkdir vscode_projects/helloworld
cd vscode_projects/helloworld/
code .
```
> The first time 'code .' is called it will install the Visual Studio Code server for Ubuntu <br/>
> After installing Visual Studio Code and the 'Remote WSL' extension you should be able to see 'Remote Host' in the borrom left corner <br/>
> <div align="left">
>  <br>
> <img src="Img\remotehost.PNG" width="300" hight="300"> <br><br>
> </div>

**Create a new c-file** <br>
Click 'new file' and create [helloword.c](HelloWorld/helloworld.c) with shown content <br/>

**Create task.json** <br>
Select 'Terminal' and 'Configure Tasks' to create [task.json](Json/tasks.json) with shown content <br>
> The folder '.vscode' is automatically created in current workspace with the newly created task.json file <br>

**Create launch.json** <br>
Select 'Run' and 'Add Configuration' to create [launch.json](Json/launch.json) with shown content <br>
Select 'C++ (GDB/LLDB)' from the installed extension pack (C/C++ extension) <br>
> This is only for creating the launch.json file and a "template" <br>






