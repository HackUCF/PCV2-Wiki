# OpenStack Infrastructure Setup Guide

## Step 1: Download OpenVPN Profile

1. Go to [join.hackucf.org](https://join.hackucf.org).
2. Click on "My Membership" and login with your Discord credentials.
3. Download the OpenVPN profile provided and save it for later use.

## Step 2: Reset Infrastructure Account

1. Visit [join.hackucf.org](https://join.hackucf.org).
2. Click on "My Membership" and login with your Discord credentials.
3. Click on "Reset Infra Account" (Note: This will reset all your data saved in OpenStack).
![alt text](<../img/Download Openvpn.png>)

## Step 3: Install OpenVPN Client

1. Go to [https://openvpn.net/client/](https://openvpn.net/client/).
2. Download the appropriate version of OpenVPN for your operating system and install it.
   
   ### For Windows:
   
   - Press the Windows key and search for OpenVPN.
   - Run OpenVPN.
   ![alt text](<../img/Run Openvpn.png>)
   - On the bottom right of your screen, open the overflow icon menu.
   - Right-click on the OpenVPN icon and select "Import Profile".
   ![alt text](<../img/Import profile.png>)
   - Click on the "FILE" tab.
   - Press "Browse" and navigate to where you downloaded the HackUCF OpenVPN profile.
   - Select the profile and press "Open".
   - Press "Connect".
   - In the future, navigate to the OpenVPN client and select the on switch labeled "vpn.hackucf.org".
   
   ### For Windows 10 Users:
   
   - If you don't already have the new Windows Terminal, download it from [https://aka.ms/terminal](https://aka.ms/terminal).

## Step 4: Create SSH Key

1. Open a terminal.
2. Run `ssh-keygen`.
3. Press Enter to save the key in the default location.
4. Press Enter for an empty passphrase.
5. Press Enter again to confirm.
![alt text](<../img/ssh KeyGen.png>)

## Step 5: Horizon.hackucf.org Configuration

1. In OpenStack, navigate to "Compute" -> "Key Pairs".
2. Click "Import Key Pair".
3. Name it something reasonable.
4. Set "Key Type" to "SSH Key".
5. Paste the contents of your id_rsa.pub file here, or use "Load Public Key from a file" to upload it.
![alt text](<../img/Key pairs Page.png>)