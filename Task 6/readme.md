# Task 6: S3 Replication and Lifecycle Policy

## Simple Definition

S3 Replication automatically copies objects from one bucket to another for backup. Lifecycle rules automatically move or delete objects to optimize storage cost.

## Objective

To configure versioning, replication, and lifecycle policies in Amazon S3 to understand backup strategy and cost optimization.

## GUI Steps

### Step 1: Create Two Buckets
1. Go to AWS Console → S3.
2. Create source bucket.
3. Create destination bucket.
4. Ensure both are in region eu-north-1.

### Step 2: Enable Versioning
1. Open source bucket → Properties.
2. Enable Versioning.
3. Repeat for destination bucket.

### Step 3: Configure Replication
1. Open source bucket → Management tab.
2. Click Replication rules → Create rule.
3. Select entire bucket.
4. Choose destination bucket.
5. Create IAM role automatically.
6. Enable rule.

### Step 4: Configure Lifecycle Policy
1. Open source bucket → Management tab.
2. Click Lifecycle rules → Create rule.
3. Apply to entire bucket.
4. Add transition rule:
   - Move to Standard-IA after 30 days.
5. Save rule.

## Verification

- Versioning shows Enabled.
- Replication rule shows Enabled.
- Lifecycle rule shows transition after 30 days.
- Upload a test file and confirm replication in destination bucket.

Screenshots Submitted:
1. Versioning enabled.
2. Replication rule configuration.

## Conclusion

Successfully configured S3 replication and lifecycle policy. This demonstrates backup strategy and cost optimization using Amazon S3.