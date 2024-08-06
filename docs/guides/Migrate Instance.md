# 2024 Instance Migration Guide
This guide provides steps to migrate between the old 2023 infra accounts and the new 2024 accounts. 

# Transferring Instances  
0. Login to the account you want to transfer **from**
1. Start by shutting down any instances you would like to transfer. Take note of the instance size, security groups, and networking configuration as those will not transfer. 

2. Navigate to Volumes > Volumes on the side bar. Notice the column labeled Attached to. 
![alt text](../img/migrate-instance/volumes-screen.png)
3. Consider renaming volumes so you can remember which instance they were attached to. Select edit volume and name the volume.  
![alt text](../img/migrate-instance/edit-volume.png)
4. Delete the instance associated with the volume
6. Create a Transfer request 
![alt text](../img/migrate-instance/image-4.png)
7. **MAKE SURE YOU SAVE THE TRANSFER ID AND KEY**
![alt text](../img/migrate-instance/image-5.png)
8. Login to the receiving account and navigate to Volumes > Volumes
9. Select Accept Transfer
![alt text](../img/migrate-instance/image-7.png)
10. Enter the ID and Key
![alt text](../img/migrate-instance/image-6.png)
11. To recreate instance follow the standard creation steps except at source. On the Select Boot Source dropdown select volume. Then select your volume.
![alt text](../img/migrate-instance/image-8.png)

