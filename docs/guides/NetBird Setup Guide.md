# NetBird Setup Guide

NetBird is the VPN used to reach the Hack@UCF Infrastructure. You must be connected to NetBird before you can access [horizon.hackucf.cloud](https://horizon.hackucf.cloud) or SSH into any instance.

## Step 1: Sign in to NetBird

1. Go-to [https://vpn.hackucf.cloud/](https://vpn.hackucf.cloud/)

![alt text](<../img/netbirdSignin.png>)

2. Select “Continue with Hack@UCF SSO”

3. Input the credentials the “**HackUCF Bot**” messaged you on discord *(from when you paid your dues)*.
![alt text](<../img/SSOLogin.png>)

## Step 2: Install the NetBird Client

1. After signing in, you will be directed to [https://vpn.hackucf.cloud/peers](https://vpn.hackucf.cloud/peers).

![alt text](<../img/netbirdInstall.png>)
Please follow the on-screen instructions for whichever device you plan to use to access the Hack@UCF Infrastructure.

Note: After you install the NetBird client, if you *don't* see the management URL field under the “*Advanced*” tab, go-to the “**Profiles**” tab, edit the default profile, select “**Self-Hosted**”, and input the “https://vpn.hackucf.cloud” URL.
![alt text](<../img/netbirdConfigURL.png>)

### Linux

On Linux you can skip the on-screen instructions and install from the command line instead:

1. Install NetBird:

```bash
curl -fsSL https://pkgs.netbird.io/install.sh | sh
```

2. Run NetBird and log in through the browser:

```bash
netbird up --management-url https://vpn.hackucf.cloud
```

This connects you as well, so you can skip Step 3.

## Step 3: Connect

1. Press connect!

![alt text](<../img/netbirdConnected1.png>)

You should now be able to reach the Hack@UCF Infrastructure.

# Next Steps

If you are working through the [OpenStack Setup Guide](./OpenStack Setup Guide.md), continue with Step 2: [SSH Key Setup Guide](./SSH Key Setup Guide.md).
