# Notes

---
## Git SSH Agent

#### One-Time Configuration

**WIN10**

    1. Configure SSH Agent Service
        Service: OpenSSH Authentication Agent
        Startup Type: Automatic Delayed
        Start Service

    2.  git config --global core.sshCommand C:/Windows/System32/OpenSSH/ssh.exe

**WS2012**

    1. Install OpenSSH (https://github.com/PowerShell/Win32-OpenSSH/releases)
    2. git config --global core.sshCommand ssh.exe

#### Add Passphrase to the SSH Agent

    ssh-add C:\Users\<username>\.ssh\<PrivateKey>

---
## POSH-Git

#### Install POSH-Git

    Set-ExecutionPolicy -Scope LocalMachine -ExecutionPolicy RemoteSigned -Force
    Install-Module posh-git -Scope CurrentUser -Force
    Install-Module PowerShellGet -Force -SkipPublisherCheck
    Import-Module posh-git
    Add-PoshGitToProfile -AllHosts
