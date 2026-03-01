# Task 3: Attach EBS Volume from Different AZ using Snapshot

## Simple Definition

An EBS snapshot is a backup of a volume stored in Amazon S3. It allows restoring the volume in another Availability Zone.

## Objective

To learn how to create an EBS snapshot and restore it in a different Availability Zone, then attach it to an EC2 instance.

## CLI Method Steps

1. Create volume in eu-north-1a.
2. Create snapshot from that volume.
3. Wait until snapshot is completed.
4. Create new volume from the snapshot in eu-north-1b.
5. Attach new volume to EC2 instance in eu-north-1b.

## GUI Method Steps (AWS Console)

1. Go to EC2 Dashboard.
2. Click Volumes → Create Volume in eu-north-1a.
3. Select the volume → Click Actions → Create Snapshot.
4. Go to Snapshots → Wait until status becomes Completed.
5. Select snapshot → Click Actions → Create Volume.
6. Choose Availability Zone eu-north-1b.
7. After volume creation, select volume → Click Actions → Attach Volume.
8. Select EC2 instance in eu-north-1b and attach as /dev/xvdf.

## Verification

CLI:
- Volume state should be "attached".
- Snapshot state should be "completed".

GUI:
- Snapshot visible in Snapshots section.
- Restored volume visible in different AZ.
- Volume attached to EC2 instance under Storage tab.

Screenshots Submitted:
1. Snapshot created and completed.
2. Restored volume in different Availability Zone.
3. Attached volume under EC2 instance storage.

## Conclusion

Successfully created an EBS snapshot and restored it into another Availability Zone, then attached it to an EC2 instance. This demonstrates cross-AZ storage handling in AWS.