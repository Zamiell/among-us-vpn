# Zamiel's Among Us Private Server

<br />

## Introduction

- Normally, you click on the "Online" button from the main menu in order to play. However, we our group **does not** use the "Online" feature because the online servers are incredibly buggy and overloaded.
- Instead, we use a VPN (virtual private network) to connect to the same network. Then, we click on "Local" from the main menu. This completely bypasses the server instability!

<br />

## Installation Instructions for Windows

- Download and install the [SoftEther VPN Client](https://github.com/Zamiell/among-us-vpn/raw/master/softether-vpnclient-v4.34-9745-rtm-2020.04.05-windows-x86_x64-intel.exe).
- Open the program. (The window title will be "SoftEther VPN Client Manager".)
- Double click on "Add VPN Connection".
- It will ask you if you want to create a new Network Adapter. Click "Yes".
- After that part finishes, double click on "Add VPN Connection" again.
- Use the following settings:
  - Setting Name: **Zamiel's Server**
  - Host Name: **amongus.ddns.net**
  - Port Number: **443**
  - Virtual Hub Name: **DEFAULT**
  - Virtual Network Adapter to Use: **[whichever one you created in the previous step, but you have to click on it]**
  - Auth Type: **Standard Password Authentication**
  - User Name: **amongus**
  - Password: **amongus**
- Once you have finished entering these settings, click "OK".
- Double click on "Zamiel' Server" to connect.

<img src="https://github.com/Zamiell/among-us-vpn/raw/master/settings.png">

<br />

## Installation Instructions for MacOS

<!--
- You do not have to download anything. Just follow [these instructions](https://www.softether.org/4-docs/2-howto/9.L2TPIPsec_Setup_Guide_for_SoftEther_VPN_Server/5.Mac_OS_X_L2TP_Client_Setup).
- Additional notes:
  - Set the "Service Name" to "Among Us".
  - Set the "Server Address" to "amongus.ddns.net".
  - Set the "Account Name" to "amongus".
  - Set the "Password" to "amongus".
  - Set the "Shared Secret" to "amongus".
  - Do NOT check the box that says "Send all traffic over VPN connection" (or else your internet will not work when connected to the VPN).
-->

- Among Us is **only** released for Windows and phones (e.g. Android & iOS), so Mac users have to get creative if they want to play.
- On a Mac, it is possible to download [BlueStacks](https://www.bluestacks.com/) (which is an Android emulator) and play the game on MacOS that way.
- Unfortunately, BlueStacks will **not** be able to access the VPN and play local games.
- Instead, Mac users are recommended to dual-boot Windows on their Mac via [Boot Camp](https://support.apple.com/boot-camp). Boot Camp is a **free** thing provided by Apple for all of their users. It makes installing Windows extremely easy: just follow the wizard and press "Next" a bunch of times.
- Once Boot Camp is finished installing, restart your computer.
- When your Mac is turning on, hold the "Option" key on the keyboard, and then you will be able to choose between booting into MacOS (e.g. like normal) or booting into Windows.
- Once on Windows, download Chrome/Firefox, download Steam, download Among Us, download Discord, and set up the VPN using the above instructions for Windows.

<br />

## Installation Instructions for Linux

- This guide covers how to:
  - Install the game on Linux using Steam Play.
  - Install and set-up the VPN that we use.

### Installing Among Us on Linux using Steam Play

- Enable Steam Play for unverified titles:
  1. Open Steam settings.
  2. Go to the Steam Play section.
  3. Check "Enable Steam Play for all other titles."
- Afterwards, install Among Us in your Steam library

### Installing Softether on Linux

- Download and install the VPN client
  1. Navigate to https://www.softether-download.com/en.aspx?product=softether
  2. Download their tarball by selecting "Softether VPN Client" and the other obvious options at the dropdowns
  3. Unpack it somewhere
  4. Navigate inside the `vpnclient` folder and run the executable `.install.sh` (**not** as root)
- Configure the VPN client
  1. Start the VPN client with `sudo ./vpnclient start` (you can stop it afterwards with `sudo ./vpnclient stop`)
  2. Run `./vpncmd` (**not** as root)
  3. Enter `2` for "Management of VPN Client"
  4. Submit a blank line to default to using `localhost`
  5. Create a Virtual Network Adapter by entering the command `NicCreate`
  6. Enter an arbritary name for the device. This will show up in the output of commands like `ip a` and `ifconfig` in the future. We will use the placeholder `<nicname>` to refer to this name moving forward.
    - If this gives an error, then it's possible that you need to enable TUN/TAP on your Linux kernel. To do so, run this command `echo -e "tunnel4\nip_tunnel" | sudo tee -a /etc/modules`, reboot your computer, and go back to step 1. ([Source](https://github.com/SoftEtherVPN/SoftEtherVPN/issues/148#issuecomment-352407872))
  7. Enter `NicEnable <nicname>`
  8. Enter `AccountCreate`
  9. Enter `ZamielServer`
  10. Enter `amongus.ddns.net:443`
  11. Enter `DEFAULT`
  12. Enter `amongus`
  13. Enter `<nicname>`
  14. Enter `AccountPasswordSet`
  15. Enter `ZamielServer`
  16. Enter `amongus` twice
  17. Enter `standard`
  18. Enter `AccountConnect ZamielServer`
  19. Enter `exit`
  20. Run `ifconfig`
  21. Look for the device labeled `vpn_<nicname>`
  22. Pick a number between 0 and 255 to use as your IP suffix
  23. Run `sudo ifconfig vpn_<nicname> 169.254.39.<IP suffix> netmask 255.255.0.0`
  24. Check if it's working by trying to join an ongoing game, if it isn't repeat the above step with a different IP suffix until it does.

Reach out to timotree on the Discord if you have issues with this.
  

<br />

## Post-Installation Instructions

- Once the VPN is connected, simply go into Among Us and choose "Local" from the main menu.
- You will be able to join other people's games (and even host your own if you want to).
