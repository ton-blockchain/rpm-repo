# TON installation packages for various operating systems

These packages are based on the latest binary artifacts which are available at https://github.com/ton-blockchain/ton/releases

### Install RPM (yum)
#### RedHat, Fedora, CentOS...
```
sudo bash -c 'cat > /etc/yum.repos.d/ton.repo << EOF
[ton]
name=Ton
baseurl=https://ton-blockchain.github.io/packages/rpm
enabled=1
type=rpm
gpgcheck=0
EOF'
```
```
yum install ton
```

### Install AUR (pamac)
#### Manjaro, RebornOS, Arch Linux... 
```
pamac build ton-bin
```
<!-- currently unavailable since still in the review at https://community.chocolatey.org/
### Install Windows binaries (choco)
```
choco install ton
```
-->

### Install deb (apt)
#### Debian, Ubuntu, Linux Mint...
```
sudo bash -c "echo 'deb [trusted=yes] https://github.com/ton-blockchain/packages/releases/latest/download ./' > /etc/apt/sources.list.d/10-ton.list"
sudo apt update
sudo apt install ton
```