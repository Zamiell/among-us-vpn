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
- Instead, Mac users are recommended to dual-boot Windows on their Mac via [Boot Camp](https://support.apple.com/boot-camp). Apple makes installing Windows with Boot Camp extremely easy: just follow the wizard and press "Next" a bunch of times.
- Once Boot Camp is installed, restart your computer.
- When your Mac is turning on, hold the "Option" key on the keyboard, and then you will be able to choose between booting into MacOS (e.g. like normal) or booting into Windows.
- Once on Windows, download Steam, download Among Us, and set up the VPN using the above instructions for Windows.

<br />

## Installation Instructions for Linux

- TODO

<br />

## Post-Installation Instructions

- Once the VPN is connected, simply go into Among Us and choose "Local" from the main menu.
- You will be able to join other people's games (and even host your own if you want to).
