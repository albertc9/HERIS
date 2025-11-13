```
'     ██░ ██ ▓█████  ██▀███   ██▓  ██████ 
'    ▓██░ ██▒▓█   ▀ ▓██ ▒ ██▒▓██▒▒██    ▒ 
'    ▒██▀▀██░▒███   ▓██ ░▄█ ▒▒██▒░ ▓██▄   
'    ░▓█ ░██ ▒▓█  ▄ ▒██▀▀█▄  ░██░  ▒   ██▒
'    ░▓█▒░██▓░▒████▒░██▓ ▒██▒░██░▒██████▒▒
'     ▒ ░░▒░▒░░ ▒░ ░░ ▒▓ ░▒▓░░▓  ▒ ▒▓▒ ▒ ░
'     ▒ ░▒░ ░ ░ ░  ░  ░▒ ░ ▒░ ▒ ░░ ░▒  ░ ░
'     ░  ░░ ░   ░     ░░   ░  ▒ ░░  ░  ░  
'     ░  ░  ░   ░  ░   ░      ░        ░  
```
> *Happy Halloween!* 🎃

> 2025 Albert Lee-Khai Cheung, IHEP, MIT LICENSE
> albert.cheung@cernNOSPAMPLEASE.ch

# **WELCOME TO HERIS!**

## Environment Management

1. This repository uses submodules. You need the --recursive option to fetch the submodules automatically:
```
// Target Core: CV32E40P
$ git clone --recursive https://github.com/pulp-platform/riscv-gnu-toolchain.git
```

2. Prerequisites (Ubuntu):
```
// Target Core: CV32E40P
$ sudo apt-get install autoconf automake autotools-dev curl python3 libmpc-dev libmpfr-dev libgmp-dev gawk build-essential bison flex texinfo gperf libtool patchutils bc zlib1g-dev libexpat-dev
```

3. Installation

For Pulpissimo, we use `riscv-gnu-toolchain`.

To build the Newlib cross-compiler, pick an install path. If you choose, say, `/opt/riscv`, then add `/opt/riscv/bin` to your `PATH` now. Then, simply run the following command:

```
./configure --prefix=/opt/riscv --with-arch=rv32imfcxpulpv3 --with-abi=ilp32 --enable-multilib
make
```
You should now be able to use `riscv32-unknown-elf-gcc` and its cousins. You can `omit --enable-multilib` if you are only interested in the specific `-march`/`-mabi` combination.