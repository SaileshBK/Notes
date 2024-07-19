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