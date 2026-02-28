# Task 2: Disk Partitioning (Ubuntu – MBR & Windows – GPT)

## Simple Definition

Disk partitioning is the process of dividing a hard disk into separate logical sections. MBR (Master Boot Record) and GPT (GUID Partition Table) are two different methods used to manage disk partitions.

## Objective

To understand disk structure and learn how to create and manage partitions using MBR in Ubuntu and GPT in Windows.

## Steps

### Ubuntu – MBR Partition

1. Check available disks using lsblk.
2. Open secondary disk using sudo fdisk /dev/sdb.
3. Create a new DOS (MBR) partition table.
4. Create a primary partition.
5. Write and save changes.
6. Format partition using ext4.
7. Verify using fdisk -l and lsblk.

### Windows – GPT Partition

1. Open Disk Management using diskmgmt.msc.
2. Convert the disk to GPT.
3. Create a new simple volume.
4. Format with NTFS.
5. Verify partition style under disk properties.

## Verification

Ubuntu:
- sudo fdisk -l should show: Disklabel type: dos
- lsblk should show new partition /dev/sdb1

Windows:
- Disk Properties → Volumes
- Partition style should show: GUID Partition Table (GPT)

Screenshots Submitted:
1. Ubuntu terminal showing MBR partition.
2. Windows Disk Management showing GPT partition.

## Conclusion

Successfully created and verified MBR partition in Ubuntu and GPT partition in Windows. This demonstrates understanding of disk structure and partition management.