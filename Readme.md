# Author: Brice Mboudjeko
# Role: Sr DevOps Engineer
# Date: 5/13/23

=========================================================================================================================
#                                                       Task
=========================================================================================================================

1- Open the Amazon EC2 console and select the EC2 instance to which you want to add storage.

2- Click on the "Actions" button and select "Create Volume".

    In the "Create Volume" dialog box, enter the required details such as volume type, size, and availability zone. Make sure to select the same availability zone as your EC2 instance.

3- Click on the "Create" button to create the new volume.

    Once the volume is created, select it from the list of available volumes and click on the "Actions" button.

4- Select "Attach Volume" from the dropdown list.

    In the "Attach Volume" dialog box, select the instance to which you want to attach the volume and specify the device name, such as /dev/sdf.

5- Click on the "Attach" button to attach the volume to the instance.

6- Connect to your EC2 instance using SSH.

7- Run the command lsblk to view the newly attached volume. You should see the device listed with the name you specified during attachment.
    
#     lsblk

8- Format the volume using the appropriate file system using a command such as :
    
#    sudo mkfs -t ext4 /dev/xvdf.

9- Create a mount point directory for the volume using a command such as :
    
#    sudo mkdir /data.

10- Mount the volume to the mount point directory using a command such as:

#   sudo mount /dev/xvdf /data.

11- Verify that the volume is mounted by running the df -h command.

#   df -h

################################################################################################################
# "Practice Makes perfect"
#  Thanks!!!
################################################################################################################


