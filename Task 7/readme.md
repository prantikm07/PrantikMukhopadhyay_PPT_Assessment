# Task 7: Create EFS and Connect to Multiple Ubuntu Instances

## Simple Definition

Amazon EFS (Elastic File System) is a scalable shared file system that can be mounted on multiple EC2 instances simultaneously.

## Objective

To create an EFS file system and mount it across multiple Ubuntu EC2 instances to enable shared storage.

## GUI Steps

### Step 1: Create EFS
1. Go to AWS Console → EFS.
2. Click Create File System.
3. Select default VPC.
4. Choose General Purpose performance mode.
5. Create file system.

### Step 2: Configure Mount Targets
1. Ensure mount targets exist in at least two Availability Zones.
2. Attach security group allowing NFS (Port 2049).

### Step 3: Connect to Ubuntu EC2
1. SSH into EC2 instance.
2. Install NFS client:
   sudo apt update
   sudo apt install nfs-common
3. Create mount directory:
   sudo mkdir /mnt/efs
4. Mount EFS:
   sudo mount -t nfs4 -o nfsvers=4.1 <EFS-DNS>:/ /mnt/efs

5. Repeat mount on second EC2 instance.

### Step 4: Test Shared Storage
1. Create a file on first instance inside /mnt/efs.
2. Verify same file appears on second instance.

## Verification

- EFS status: Available.
- Mount targets in multiple AZs.
- File created on one instance visible on another.

Screenshots Submitted:
1. EFS File System overview.
2. Mount targets configuration.
3. Shared file visible on 2nd EC2 instance.

## Conclusion

Successfully created and mounted an Amazon EFS file system across multiple Ubuntu EC2 instances, demonstrating scalable shared storage in AWS.