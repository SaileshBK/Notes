## Reference
[[https://fireship.io/lessons/windows-10-for-web-dev/]]

## Enable Windows-Subsystem-Linux (WSL)

From the start menu, search for PowerShell and run it as an administrator. Run the command below. It will require a full reboot of your system.

```
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

## Update the Linux

```
sudo apt update
sudo apt upgrade -y
```


## WSL From Terminal

You have to download the Linux distributions as it is not pre-installed in windows

```
wsl --list --online 
```

Gives you list of valid distribution that you can be installed. Command to install any one distribution from list. 

```
wsl --install -d <Distro> 
```


Note : - Using Linux or Kali Linux by this method is not as same as running Kali Linux on a virtual machine (VMWare or VirtualBox).