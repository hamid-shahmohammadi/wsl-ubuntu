# wsl-ubuntu
```
wsl.exe --install
wsl.exe --update
\\wsl$\Ubuntu\home\shah
```
# link for wsl1 to wsl 2
```
https://learn.microsoft.com/en-us/windows/wsl/basic-commands#set-wsl-version-to-1-or-2
https://learn.microsoft.com/en-us/windows/wsl/install-manual#step-2---check-requirements-for-running-wsl-2
```
# wsl 2
```
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
wsl --set-default-version 2
wsl.exe --set-version Ubuntu 2

wsl -l -v
```
