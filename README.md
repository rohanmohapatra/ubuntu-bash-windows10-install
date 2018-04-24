# ubuntu-bash-windows10-install


 ### Steps to install Ubuntu Bash on Windows 10 
 - Enable the "Windows Subsystem for Linux" optional feature by 
    - Open PowerShell as Administrator and run: ``` Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux ```
    - Restart Computer when prompted. 
 - Go to Windows Store and Download Ubuntu Application by Canonical
 - Launch the Application and follow the steps prompted.

 ### Want to make it look like Ubuntu Terminal?
 - Download the folder with the fonts and double click install.vbs to run the script.


 A VBs script that installs the fonts that are present in the current directory in Windows 10 
 with a PowerShell script that modifies the apperance of the 'Ubuntu on Windows' bash to look like 
 the original Ubuntu.
 
 
### To run gcc , you have to install the compiler

```
- sudo apt-get update         \\Fetches the list of available updates
- sudo apt-get upgrade        \\Strictly upgrades the current packages
- sudo apt-get dist-upgrade   \\Installs updates (new ones)
- sudo apt-get install gcc
```
### Mount USB Media (including FAT formated) and network shares with drvfs

Mount removable media: (e.g. F:)

```
- sudo mkdir /mnt/f
- sudo mount -t drvfs F: /mnt/f

```
To safely unmount

```
- sudo umount /mnt/f
```

You can also mount network shares without smbfs
```
- sudo mount -t drvfs '\\server\share' /mnt/share
```

To detach a busy device immediately (even if it is busy and cannot be unmounted forcefully).
```
- umount -l /PATH/OF/BUSY-DEVICE
- umount -f /PATH/OF/BUSY-NFS(NETWORK-FILE-SYSTEM)
```
##### -l is for unmounting device lazily, even if it is busy
##### -f is for unmounting device forcefully
