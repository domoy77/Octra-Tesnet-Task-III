[![GitHub stars](https://img.shields.io/github/stars/domoy77/system-monitor-pro-desktop?style=social)](https://github.com/domoy77/system-monitor-pro-desktop/stargazers)
![Platform](https://img.shields.io/badge/Platform-Linux-success)
[![Buy Me A Coffee](https://img.shields.io/badge/Donate-Buy%20Me%20A%20Coffee-yellow.svg)](https://buymeacoffee.com/domoy77)

Tesnet Task III For linux : Ubuntu/Debian, Fedora/RHEL, Arch

1. Install Update
* Ubuntu/Debian
```bash
sudo apt update
sudo apt install pkg-config libssl-dev
```
```bash
pkg-config --version  
pkg-config --modversion openssl  
```
** Fedora/RHEL
```bash
sudo dnf install pkg-config openssl-devel
```
*** Arch
```bash
sudo pacman -S pkgconf openssl
```
2. Install Rust (if not installed)
```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source $HOME/.cargo/env
```
3. Build from Source
```bash
git clone https://github.com/octra-labs/ocs01-test.git
cd ocs01-test
cargo build --release
```
4. Setup
```bash
# copy contract interface
cp EI/exec_interface.json .
```
5. Create Wallet
```bash
nano wallet.json
```
```bash
{
  "priv": "private‑key‑format B64",
  "addr": "octra‑address dimulai dengan oct…",
  "rpc": "https://octra.network"
}
```
Replace:

"priv" → Your Base64-encoded private key

"addr" → Your Octra testnet address

6. Run
```bash
./target/release/ocs01-test
```
Or
```bash
./ocs01-test
```


