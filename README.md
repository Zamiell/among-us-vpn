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

<img src="https://github.com/Zamiell/among-us-vpn/raw/master/settings.png">

- For reference, you need to enter the following fields:
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
- A message that says "Requesting an IP address ot the DHCP server in the VPN..." will appear. There is no DHCP server on this VPN, so just click "Close". (You can also just let the message sit for a few seconds and it will go away by itself.)

<br />

## Installation Instructions for MacOS

- You do not have to download anything. Just follow [these instructions](https://www.softether.org/4-docs/2-howto/9.L2TPIPsec_Setup_Guide_for_SoftEther_VPN_Server/5.Mac_OS_X_L2TP_Client_Setup).
- Additional notes:
  - Set the "Service Name" to "Among Us".
  - Set the "Server Address" to "amongus.ddns.net".
  - Set the "Account Name" to "amongus".
  - Set the "Password" to "amongus".
  - Set the "Shared Secret" to "amongus".
  - Do NOT check the box that says "Send all traffic over VPN connection" (or else your internet will not work when connected to the VPN).

<br />

## Installation Instructions for Linux

- TODO

<br />

## Post-Installation Instructions

- Once the VPN is connected, simply go into Among Us and choose "Local" from the main menu.
- You will be able to join other people's games (and even host your own if you want to).
