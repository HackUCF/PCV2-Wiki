# SSH Key Setup Guide

This guide walks you through generating an SSH key pair and importing the public key into OpenStack so it can be injected into the instances you launch.

Before you start, make sure you are connected to the VPN — see the [NetBird Setup Guide](./NetBird Setup Guide.md).

## Step 1: Create SSH Key

1. Open a terminal.
2. Run `ssh-keygen -t rsa`.
3. Press Enter to save the key in the default location.
4. Press Enter for an empty passphrase.
5. Press Enter again to confirm.
![alt text](<../img/ssh KeyGen.png>)

## Step 2: Login With Keycloak
0. Navigate to [https://horizon.hackucf.cloud](https://horizon.hackucf.cloud)
1. Select login with Hack@UCF SSO
![alt text](<../img/OpenStack-Setup-Guide/Login-with-SSO.png>)
2. (These other steps are just for the first time)
3. Login with credentials emailed or dm by Hack@UCF bot
4. Agree to TOS
5. Change Password
6. Confirm Email

## Step 3: Horizon.hackucf.cloud Configuration

1. In OpenStack, navigate to "Compute" -> "Key Pairs".
2. Click "Import Public Key".
3. Name it something reasonable.
4. Set "Key Type" to "SSH Key".
5. Paste the contents of your id_rsa.pub file here, or use "Load Public Key from a file" to upload it.
![alt text](<../img/OpenStack-Setup-Guide/Key-pairs-Page.png>)

# Next Steps

That is the last step of the [OpenStack Setup Guide](./OpenStack Setup Guide.md).

- Go to [Security Groups](./Security Groups.md)
