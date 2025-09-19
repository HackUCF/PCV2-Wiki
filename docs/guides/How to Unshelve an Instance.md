# How To Unshelve Instances On Openstack #

When you leave a machine shutdown for a long time in openstack, it will eventually be shelved. 
Simply put, you need to unshelve the instance before you can turn it back on. This tutorial covers how to unshelve an instance so you can use it again.

## Prerequisites ##

* Access to openstack via OpenVPN or Cyberlab WiFi
* One or more shelved instances (more on this later)

### Why can't I turn on my instance? (if you don't care and just want to turn it on skip this text) ###

If you leave your instance unattended for too long, it will eventually be shelved. Shelving an instance is like shutting it down even further than just turning it off. When you shut down an instance, Its associated resources like RAM and Disk Space are still assigned to the instance even if they are not in use. So if you leave a shut down instance on openstack it's essentially wasting space, which we don't like. To fix this issue, after a certain amount of time the instance will get **SHELVED**. This means that openstack will save the needed **details** to run the instance and then delete the instance so others can use its resources. Essentially, openstack saves what we need to rebuild the instance and deletes it so we can rebuild it later, this rebuilding is called **UNSHELVING**. Once rebuilt you can turn your machine back on and do as you wish.

## TLDR of above paragraph ##

You can't turn it on because it's temporarilly deleted but you can rebuild it to its former glory by unshelving it. Here's How!

## Step 1: Is my instance shelved? ##

If you've had it shutdown and untouched for a long time, most likely **yes**. Here's how you can tell.

**FIRST**, to turn on a shut down machine, select it, click the **"More Actions"** drop down, and click **"Start Instances"**.
If the instance is shelved you'll get an error as shown below.

![step1](..\img\Unshelve-instance\unshelving-step1.png)
