<h1 align="center">
    <img src="https://avatars.githubusercontent.com/u/114239186?s=100&v=4" alt="palera1n logo">
    <p>palera1n</p>
</h1>
<h3 align="center">An iOS 15.0-15.3.1 work-in-progress, tethered checkm8 jailbreak.</h3>
<p align="center">
    <strong><a href="CHANGELOG.md">Change Log</a></strong>
    •
    <strong><a href="https://dsc.gg/palera1n">Discord</a></strong>
    •
    <strong><a href="https://twitter.com/palera1n">Twitter</a></strong>
</p>

# How does it work?
It boots the device with AMFI patches. On first run, it'll boot a ramdisk which dumps your onboard blob, and installs Sileo and Substitute.

# Issues
### Need help?
If you need help, **please** join our Discord. We disabled issues due to the flood of spam, and difficulty to respond in general. We are much more comfortable on Discord.

Please, please, please, provide necessary info:

- iOS version and device (eg. iPhone 7+ 15.1, iPhone 6s 15.3.1)
- Computer's OS and version (eg. Ubuntu 22.04, macOS 13.0)
- The command you ran
- **Full log from the logs folder**

**DO NOT** harass tweak devs if tweaks don't work. Refer to [here](https://github.com/itsnebulalol/ios15-tweaks) for compatiblity.

You may join [here](https://dsc.gg/palera1n).

### Linux
- Linux has some weird usbmuxd issues. We have tried our best to fix them, but there still are issues. We highly recommend to compile and install usbmuxd2.
- Stop making issues about Linux not being able to connect, we are aware. This includes being stuck on waiting for ramdisk to finish booting.

### Warning
- We are **NOT** responsible for any data loss. The user of this program accepts responsibility should something happen to their device. While nothing should happen, jailbreaking has risks in itself. **If your device is stuck in recovery, please run one of the following:**
   - futurerestore --exit-recovery
   - irecovery -n
- Using this on iOS 16 has a higher chance of bootlooping you.

### A10 and A11 devices
- On A10 and A11, **you must disable your passcode while in the jailbroken state**.
  - On A10, this can be fixed in the future by implementing blackbird.
  - On A11, we don't have a SEP exploit yet.

# Prerequisites
#### Warning: You must install the Tips app from the App Store before running palera1n.
- A checkm8 vulnerable iOS device on iOS 15 (A8-A11)
  - The device must be on iOS 15.0-15.3.1
    - Currently, the best is iOS 15.1.
    - iOS 15.0-15.0.2 and 15.2-15.3.1 have **App Store app launching issues**.
- Linux or macOS computer
  - Python 3 must be installed.

# How to use?
1. Clone this repo with `git clone -b tweaks --recursive https://github.com/palera1n/palera1n && cd palera1n`
2. Run `./palera1n.sh --tweaks <your current iOS version>`
   - [A10 and A11] Before running, **you must disable your passcode**.
   - Put your device in DFU mode before running.
3. Follow the steps on your screen.

# Repos

### Tweaks mode
All repos work when using tweaks mode because it uses normal Procursus and not rootless.

### Rootless 
Repos need to be updated for rootless, here are some that work currently:

- [Mineek's repo](https://mineek.github.io/repo) contains rootless Procursus packages
- The official [palera1n repo](https://repo.palera.in) contains miscellaneous packages

If you want to make a rootless repo, use the official [palera1n repo](https://github.com/palera1n/repo) for reference. Every deb should use the `iphoneos-arm64` architecture, and *nothing* should be on the rootfs. Everything should be in /var/jb.

# Credits
- [Nathan](https://github.com/verygenericname)
    - The ramdisk that dumps blobs is a slimmed down version of SSHRD_Script
    - Also helped Mineek getting the kernel up and running and with the patches
    - Helping with adding multiple device support
- [Mineek](https://github.com/mineek)
    - For the patching and booting commands
    - Adding tweak support
- [Amy](https://github.com/elihwyma) for the Pogo app
- [checkra1n](https://github.com/checkra1n) for the base of the kpf
- [nyuszika7h](https://github.com/nyuszika7h) for the script to help get into DFU
- [the Procursus Team](https://github.com/ProcursusTeam) for the amazing bootstrap
- [F121](https://github.com/F121Live) for helping test
- [tihmstar](https://github.com/tihmstar) for pzb/original iBoot64Patcher/img4tool
- [xerub](https://github.com/xerub) for img4lib and restored_external in the ramdisk
- [Cryptic](https://github.com/Cryptiiiic) for iBoot64Patcher fork
