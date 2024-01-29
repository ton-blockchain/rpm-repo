# TON installation packages for various operating systems

These packages are based on the latest binary artifacts https://github.com/ton-blockchain/ton/releases

### Install RPM (yum)
#### RedHat, Fedora, CentOS...
```
sudo bash -c 'cat > /etc/yum.repos.d/ton.repo << EOF
[ton]
name=TON
baseurl=https://ton-blockchain.github.io/packages/rpm
enabled=1
type=rpm
gpgcheck=0
EOF'

sudo yum install -y ton
```

### Install AUR (pamac)
#### Manjaro, RebornOS, Arch Linux... 
```
sudo pamac build -no-confirm ton-bin
```

### Install deb (apt)
#### Debian, Ubuntu, Linux Mint...
```
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys F6A649124520E5F3
sudo add-apt-repository ppa:ton-foundation/ppa
sudo apt update
sudo apt install ton
```

### Install via brew
#### macOS
```
brew tap ton-blockchain/ton
brew install ton

# upgrade
brew update
brew reinstall ton
```

### Install via Chocolatey
Please, be aware that multiple false positive alarms from various antivirus vendors may occur.
This is an expected behaviour and there is no reason to worry.
#### Windows x86-64
```
choco install ton
```