# OpenStack Infrastructure Setup Guide

## Step 1: Install NetBird

1. Go-to https://vpn.hackucf.cloud/
![alt text](<../img/netbirdSignin.png>)

2. Select “Continue with Hack@UCF SSO”

3. Input the credentials the “**HackUCF Bot**” messaged you on discord *(from when you paid your dues)*. 
![alt text](<../img/SSOLogin.png>)

4. After signing in, you will be directed to https://vpn.hackucf.cloud/peers.
![alt text](<../img/netbirdInstall.png>)
Please follow the on-screen instructions for whichever device you plan to use to access the Hack@UCF Infrastructure.

Note: After you install the NetBird client, if you *don't* see the management URL field under the “*Advanced*” tab, go-to the “**Profiles**” tab, edit the default profile, select “**Self-Hosted**”, and input the “https://vpn.hackucf.cloud” URL. 

5. Press connect! 
![alt text](<../img/netbirdConnected.png>)
You should now be able to reach the Hack@UCF Infrastructure. 

## Step 2: Create SSH Key

1. Open a terminal.
2. Run `ssh-keygen -t rsa`.
3. Press Enter to save the key in the default location.
4. Press Enter for an empty passphrase.
5. Press Enter again to confirm.
![alt text](<../img/ssh KeyGen.png>)

## Step 3: Login With Keycloak
0. Navigate to [https://horizon.hackucf.cloud](https://horizon.hackucf.cloud)
1. Select login with Hack@UCF SSO
![alt text](<../img/OpenStack-Setup-Guide/Login-with-SSO.png>)
2. (These other steps are just for the first time)
3. Login with credentials emailed or dm by Hack@UCF bot
4. Agree to TOS
5. Change Password
6. Confirm Email

## Step 4: Horizon.hackucf.cloud Configuration

1. In OpenStack, navigate to "Compute" -> "Key Pairs".
2. Click "Import Public Key".
3. Name it something reasonable.
4. Set "Key Type" to "SSH Key".
5. Paste the contents of your id_rsa.pub file here, or use "Load Public Key from a file" to upload it.
![alt text](<../img/OpenStack-Setup-Guide/Key-pairs-Page.png>)

# Next Steps

- Go to [Security Groups](./Security Groups.md)
