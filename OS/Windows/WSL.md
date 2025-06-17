# Using WSL
## Navigate to windows directories

cd /mnt/c/Users/{USERNAME}

ln -s /mnt/c/Users/{USERNAME} ~/temp


# Managing WSL
## Install packages
```
sudo apt update

sudo apt install --no-install-recommends apt-transport-https ca-certificates curl gnupg2
sudo apt install net-tool
sudo apt install curl
sudo apt install iputils-ping
sudo apt install dos2unix

sudo apt install openjdk-8-jdk-headless
sudo apt install openjdk-11-jdk-headless
sudo apt install openjdk-17-jdk-headless
```

### Search for versions to install
```
apt search openjdk-8
apt search openjdk-11
apt search openjdk-17
```

### list installed
```
sudo apt list --installed "*jdk*"
```

or use:
```
update-alternatives --list java
```

### Switching versions
```
update-alternatives --version
update-alternatives --list java
update-alternatives --config editor
```

## Stopping the service
Probably a good idea to stop the instances at end of day:
```
wsl --shutdown
```

## Maven repository link
```
ln -s /mnt/c/Users/lreynolds/.m2 ~/.m2
```

## Set up JDK
### trying with windows java installs
Find windows Java locations in intellij project structure:


### Use wsl specific installs
```
sudo apt update

sudo apt install openjdk-8-jdk-headless
sudo apt install openjdk-11-jdk-headless
sudo apt install openjdk-17-jdk-headless
```

### Switch versions
```
sudo update-alternatives --config java
```

## Fixing issues
### Network connectivity
NOTE: internet connectivity doesn't work with the VPN running. You have to stop it and then start it again when finished.

__NOTE: RUN WITH AN ADMIN POWERSHELL!__
To fix the internet connection:
```
Get-NetAdapter | Where-Object {$_.InterfaceDescription -Match "Cisco AnyConnect"} | Set-NetIPInterface -InterfaceMetric 4000
Get-NetIPInterface -InterfaceAlias "vEthernet (WSL*" | Set-NetIPInterface -InterfaceMetric 1
```

__In WSL__
```
echo "search wnet.local" | sudo tee -a /etc/resolv.conf
```
(Should allow the dns lookup to work without fully qualified hostnames i.e. no need for wnet.local on the end of everything)

This adds "search wnet.local" to the resolv.conf file. Check with:
```
cat /etc/resolv.conf
```


**After performing the above, re-start or re-create any docker images**


### Restart WSL
__in admin powershell:__
```
wsl --shutdown
```

Wait for it to finish.
